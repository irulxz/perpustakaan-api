# Perpustakaan API

REST API Laravel 12 dengan login Sanctum, CRUD buku, dan dokumentasi OpenAPI (Swagger).

## Stack
- Laravel 12, PHP 8.3
- Laravel Sanctum (token API)
- L5-Swagger (OpenAPI 3)
- MySQL

## Instalasi
```bash
git clone https://github.com/irulxz/perpustakaan-api.git
cd perpustakaan-api
composer install
cp .env.example .env
php artisan key:generate
# atur DB_DATABASE di .env, lalu:
php artisan migrate:fresh --seed
php artisan l5-swagger:generate
php artisan serve
```

## Dokumentasi Swagger
http://localhost:8000/api/documentation

## Akun demo
admin@example.com / password

## Endpoint
| Method | Endpoint | Fungsi | Login? |
|---|---|---|---|
| POST | /api/register | Daftar akun | Tidak |
| POST | /api/login | Login, dapat token | Tidak |
| GET | /api/me | Profil user | Ya |
| POST | /api/logout | Hapus token | Ya |
| GET | /api/books | Daftar buku (paginasi + pencarian) | Ya |
| POST | /api/books | Tambah buku | Ya |
| GET | /api/books/{id} | Detail buku | Ya |
| PUT/PATCH | /api/books/{id} | Ubah buku | Ya |
| DELETE | /api/books/{id} | Hapus buku | Ya |

## Video penjelasan
(tempel link YouTube di sini)