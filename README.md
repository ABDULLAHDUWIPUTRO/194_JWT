# Praktikum 8 - Implementasi Password Hashing & JWT Authentication

Repository ini berisi project REST API berbasis **Node.js**, **Express**, **Sequelize**, dan **PostgreSQL** yang menerapkan keamanan autentikasi menggunakan **bcrypt** (password hashing) dan **JSON Web Token (JWT)** untuk manajemen data Komik.

## Identitas Mahasiswa
* **Nama:** Abdullah Duwiputro
* **NIM:** 20240140194
* **Kelas:** D
* **Mata Kuliah:** Pengembangan Web Service (PWS)

---

## Teknologi yang Digunakan
* **Runtime:** Node.js
* **Framework:** Express.js
* **Database & ORM:** PostgreSQL, Sequelize, Sequelize CLI
* **Security & Auth:** `bcrypt` & `jsonwebtoken` (JWT)
* **Environment & Dev Tools:** `dotenv`, `nodemon`, Postman

---

## Struktur Folder
```text
├── config/
│   ├── config.js
│   └── db.js
├── controller/
│   ├── komikController.js
│   └── userController.js
├── middleware/
│   └── authMiddleware.js
├── migrations/
├── models/
│   ├── index.js
│   ├── komik.js
│   └── user.js
├── routes/
│   └── api.js
├── seeders/
├── .env
├── .gitignore
├── .sequelizerc
├── index.js
├── package.json
└── README.md
```

---

## Daftar Endpoint API

| Method | Endpoint | Akses | Deskripsi |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/register` | Public | Registrasi akun baru dengan hashing password (`bcrypt`) |
| `POST` | `/api/login` | Public | Login akun dan menghasilkan token JWT |
| `GET` | `/api/komik` | Public | Menampilkan seluruh data komik |
| `GET` | `/api/komik/:id` | Public | Menampilkan detail data komik berdasarkan ID |
| `POST` | `/api/komik` | Protected (Bearer Token) | Menambahkan data komik baru |
| `PUT` | `/api/komik/:id` | Protected (Bearer Token) | Memperbarui data komik berdasarkan ID |
| `DELETE` | `/api/komik/:id` | Protected (Bearer Token) | Menghapus data komik berdasarkan ID |

---

## Hasil Testing Postman

### 1. Register (`POST /api/register`)

<img width="1747" height="730" alt="image" src="https://github.com/user-attachments/assets/d1763b7d-2b68-46e6-a32c-521b10344812" />

---

### 2. Login (`POST /api/login`)

<img width="1737" height="681" alt="image" src="https://github.com/user-attachments/assets/4946b564-c673-49b4-afba-3f571761e9ee" />


---

### 3. Create Komik (`POST /api/komik`)

<img width="1733" height="731" alt="image" src="https://github.com/user-attachments/assets/b1e175e8-6da1-4031-8f1e-a874d4a80e44" />


---

### 4. Get All Komik (`GET /api/komik`)

<img width="1738" height="771" alt="image" src="https://github.com/user-attachments/assets/b044d429-6230-4401-a398-93b3d4fb2f9e" />


---

### 5. Get Komik by ID (`GET /api/komik/:id`)

<img width="1742" height="666" alt="image" src="https://github.com/user-attachments/assets/ac901fc3-dd29-43ff-ac4b-7bfb600b8cce" />


---

### 6. Update Komik (`PUT /api/komik/:id`)

<img width="1738" height="730" alt="image" src="https://github.com/user-attachments/assets/0da4dd11-799b-4ddf-a384-f0fb1b862c4b" />


---

### 6. Delete Komik (`DELETE /api/komik/:id`)
<img width="1740" height="641" alt="image" src="https://github.com/user-attachments/assets/8e7196c6-8c79-4619-93fd-eb1eadf91840" />


### 7. Delete Komik (`DELETE /api/komik/:id`)

<img width="1741" height="658" alt="image" src="https://github.com/user-attachments/assets/311a18a2-1db8-4414-a42f-bf46f86c4716" />

