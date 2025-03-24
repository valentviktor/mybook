# Panduan Lengkap Python & PyMySQL untuk Flask

## 1. Dasar-Dasar Python

### 1.1 Variabel dan Tipe Data
```python
nama = "Viktor"  # String
umur = 22  # Integer
tinggi = 1.75  # Float
is_mahasiswa = True  # Boolean
duit = None  # None or Null at another language
```

### 1.2 Percabangan dan Perulangan
#### Percabangan (if-elif-else)
```python
nilai = 85
if nilai >= 90:
    print("A")
elif nilai >= 80:
    print("B")
else:
    print("C")
```

#### Perulangan (`for` & `while`)
```python
# Looping dengan for
for i in range(5):
    print("Perulangan ke-", i)

# Looping dengan while
angka = 1
while angka <= 3:
    print("Angka:", angka)
    angka += 1
```

### 1.3 Fungsi
```python
def luas_persegi(sisi):
    return sisi * sisi

print(luas_persegi(4))  # Output: 16
```

### 1.4 List, Tuple, dan Dictionary
```python
# List (mutable)
mahasiswa = ["Viktor", "Valentino"]
mahasiswa.append("Budi")
print(mahasiswa)

# Tuple (immutable)
data = ("Python", "Flask")

# Dictionary
mhs = {"nama": "Viktor", "nim": "123456"}
print(mhs["nama"])
```

---

## 2. PyMySQL: Koneksi Python dengan MySQL

### 2.1 Instalasi PyMySQL
```bash
pip install pymysql
```

### 2.2 Koneksi ke MySQL
```python
import pymysql

db = pymysql.connect(
    host="localhost",
    user="root",
    password="",
    database="penelitian_mahasiswa"
)

cursor = db.cursor()
cursor.execute("SELECT VERSION()")
data = cursor.fetchone()
print("Versi MySQL:", data)

db.close()
```

### 2.3 Membuat Tabel di MySQL
```python
cursor.execute("""
    CREATE TABLE IF NOT EXISTS mahasiswa (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nama VARCHAR(100),
        nim VARCHAR(20) UNIQUE
    )
""")
db.commit()
```

### 2.4 Menambahkan Data ke Database
```python
sql = "INSERT INTO mahasiswa (nama, nim) VALUES (%s, %s)"
data = ("Viktor", "123456")
cursor.execute(sql, data)
db.commit()
print("Data berhasil ditambahkan")
```

### 2.5 Menampilkan Data dari Database
```python
cursor.execute("SELECT * FROM mahasiswa")
result = cursor.fetchall()
for row in result:
    print(row)
```

---

## 3. Flask: Membuat Website Pemantauan

### 3.1 Instalasi Flask
```bash
pip install flask
```

### 3.2 Struktur Folder Flask
```
/projek-penelitian
│── /static        # File CSS, JS
│── /templates     # HTML
│── app.py         # Main Flask App
│── database.py    # Koneksi Database
```

### 3.3 Membuat Flask App
Buat file **`app.py`**:
```python
from flask import Flask
import pymysql

app = Flask(__name__)

def get_db_connection():
    return pymysql.connect(
        host="localhost",
        user="root",
        password="",
        database="penelitian_mahasiswa",
        cursorclass=pymysql.cursors.DictCursor
    )

@app.route('/')
def home():
    return "Selamat datang bree!"

if __name__ == '__main__':
    app.run(debug=True)
```

Jalankan dengan:
```bash
python app.py # Auto hot reload

# atau

flask run # Tidak hot reload
```
Akses di browser: `http://127.0.0.1:5000/`

---

## 4. Flask dengan PyMySQL

### 4.1 Menampilkan Data di Halaman Web
```python
from flask import Flask, render_template
import pymysql

app = Flask(__name__)

def get_db_connection():
    return pymysql.connect(
        host="localhost",
        user="root",
        password="",
        database="penelitian_mahasiswa",
        cursorclass=pymysql.cursors.DictCursor
    )

@app.route('/mahasiswa')
def mahasiswa():
    db = get_db_connection()
    cursor = db.cursor()
    cursor.execute("SELECT * FROM mahasiswa")
    data = cursor.fetchall()
    db.close()
    return render_template('mahasiswa.html', mahasiswa=data)

if __name__ == '__main__':
    app.run(debug=True)
```

Buat file **`templates/mahasiswa.html`**:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Data Mahasiswa</title>
</head>
<body>
    <h1>Data Mahasiswa</h1>
    <table border="1">
        <tr>
            <th>ID</th>
            <th>Nama</th>
            <th>NIM</th>
        </tr>
        {% for mhs in mahasiswa %}
        <tr>
            <td>{{ mhs.id }}</td>
            <td>{{ mhs.nama }}</td>
            <td>{{ mhs.nim }}</td>
        </tr>
        {% endfor %}
    </table>
</body>
</html>
```

Akses di browser: `http://127.0.0.1:5000/mahasiswa`

---

## 5. Menyajikan Data sebagai API JSON

Tambahkan route di `app.py`:
```python
from flask import jsonify

@app.route('/api/mahasiswa', methods=['GET'])
def api_mahasiswa():
    db = get_db_connection()
    cursor = db.cursor()
    cursor.execute("SELECT * FROM mahasiswa")
    data = cursor.fetchall()
    db.close()
    return jsonify(data)
```

Cek di browser: `http://127.0.0.1:5000/api/mahasiswa`

---

## Kesimpulan
✅ **Python Dasar** (Variabel, Fungsi, Looping, dll).  
✅ **PyMySQL untuk koneksi MySQL**.  
✅ **Flask untuk web framework**.  
✅ **Menampilkan, menambah, menghapus data**.  
✅ **Menyediakan API JSON**.  

**Catatan:** Simple Flask ini cocok untuk aplikasi kecil yang hanya untuk sistem pemantauan sederhana. Jika aplikasi berkembang lebih kompleks, disarankan menggunakan framework yang lebih scalable seperti FastAPI atau Django.

Gass! 🚀
