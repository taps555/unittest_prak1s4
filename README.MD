# Praktikum 1 - Unit Testing dengan Jest

## Tujuan Praktikum

Pada praktikum ini mahasiswa diharapkan mampu:

- Membuat project Node.js sederhana
- Menggunakan Jest sebagai framework pengujian
- Membuat unit test
- Menjalankan pengujian menggunakan Jest
- Menganalisis hasil coverage

---

## Persiapan

Buat folder dengan format:

```
NBI_Nama
```

Contoh:

```
14622000071_TrioAdhiPamungkas
```

Masuk ke folder project kemudian jalankan:

```bash
npm init -y
npm install --save-dev jest
```

Tambahkan script berikut pada file `package.json`:

```json
"scripts": {
  "test": "jest"
}
```

---

## Struktur Folder

```
|---- src
|      |
|      └── nilai.js
|
|---- test
|      |
|      └── nilai.test.js
|
└── package.json
```

---

# Soal

Buat sebuah fungsi bernama `konversiNilai()` pada file `nilai.js`.

Fungsi menerima sebuah parameter berupa nilai angka dan mengembalikan grade huruf sesuai ketentuan berikut:

| Rentang Nilai | Grade |
| ------------- | ----- |
| 85 - 100      | A     |
| 70 - 84       | B     |
| 60 - 69       | C     |
| 0 - 59        | D     |
| < 0 atau >100 | Tidak Valid |

---

## Contoh Penggunaan

```javascript
konversiNilai(90);
```

Output:

```text
A
```

---

```javascript
konversiNilai(75);
```

Output:

```text
B
```

---

```javascript
konversiNilai(65);
```

Output:

```text
C
```

---

```javascript
konversiNilai(50);
```

Output:

```text
D
```

---

```javascript
konversiNilai(-1);
```

Output:

```text
Tidak Valid
```

---

```javascript
konversiNilai(120);
```

Output:

```text
Tidak Valid
```

---

## Tugas

### 1. File `src/nilai.js`

Lengkapi fungsi berikut:

```javascript
function konversiNilai(nilai) {
  // TODO
}

module.exports = {
  konversiNilai,
};
```

---

### 2. File `test/nilai.test.js`

Buat unit test untuk menguji kondisi berikut:

- Nilai 90 menghasilkan A
- Nilai 75 menghasilkan B
- Nilai 65 menghasilkan C
- Nilai 50 menghasilkan D
- Nilai -1 menghasilkan Tidak Valid
- Nilai 120 menghasilkan Tidak Valid

---

## Menjalankan Pengujian

```bash
npm test
```

---

## Menampilkan Coverage

```bash
npx jest --coverage
```

---

## Ekspektasi Hasil Testing

```text
PASS test/nilai.test.js

✓ nilai 90 menghasilkan A
✓ nilai 75 menghasilkan B
✓ nilai 65 menghasilkan C
✓ nilai 50 menghasilkan D
✓ nilai -1 menghasilkan Tidak Valid
✓ nilai 120 menghasilkan Tidak Valid

Test Suites: 1 passed, 1 total
Tests:       6 passed, 6 total
```

---

## Ekspektasi Coverage

```text
------------------|---------|----------|---------|---------|
File              | % Stmts | % Branch | % Funcs | % Lines |
------------------|---------|----------|---------|---------|
All files         |   100   |   100    |   100   |   100   |
nilai.js          |   100   |   100    |   100   |   100   |
------------------|---------|----------|---------|---------|
```

---

## Ketentuan Pengumpulan

1. Push project ke GitHub.
2. Sertakan file source code dan unit test.
3. Sertakan screenshot hasil:

```bash
npm test
```

dan

```bash
npx jest --coverage
```

4. Upload link repository pada LMS.