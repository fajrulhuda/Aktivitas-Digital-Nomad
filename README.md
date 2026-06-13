# aktivitas_nomad

# Repository Pattern Project

## Deskripsi Proyek

Proyek ini merupakan implementasi **Repository Pattern** pada aplikasi Flutter dengan tujuan memisahkan logika bisnis dari sumber data sehingga kode menjadi lebih terstruktur, mudah dipelajari, mudah diuji (testable), dan mudah dikembangkan.

Dalam proyek ini, tim menerapkan beberapa komponen utama yaitu:

* Remote Data Source
* Local Data Source
* Repository Implementation
* Dio Auth Interceptor

Setiap komponen dikerjakan pada branch terpisah oleh anggota tim dan digabungkan melalui mekanisme Pull Request serta Code Review menggunakan GitHub.

---

# Alasan Memilih Repository Pattern

Repository Pattern dipilih karena merupakan salah satu arsitektur yang banyak digunakan dalam pengembangan aplikasi modern, terutama pada Flutter.

### Keuntungan Repository Pattern

#### 1. Separation of Concerns

Memisahkan tanggung jawab setiap layer sehingga kode lebih terorganisir.

* UI hanya menangani tampilan.
* Repository menangani logika pengambilan data.
* Data Source menangani komunikasi dengan API atau database.

#### 2. Mudah Dikembangkan

Ketika sumber data berubah, misalnya dari REST API ke GraphQL atau Firebase, perubahan hanya dilakukan pada Data Source tanpa memengaruhi layer lain.

#### 3. Mudah Diuji (Testing)

Repository dapat menggunakan mock data sehingga pengujian unit test menjadi lebih mudah dilakukan.

#### 4. Mengurangi Duplikasi Kode

Seluruh akses data dipusatkan pada Repository sehingga tidak terjadi pengulangan pemanggilan API pada banyak halaman.

#### 5. Mempermudah Pemeliharaan

Struktur proyek menjadi lebih jelas dan memudahkan pengembang lain untuk memahami alur aplikasi.

---

### Alur Sistem

1. User melakukan aksi pada UI.
2. UI memanggil Repository.
3. Repository menentukan sumber data yang digunakan.
4. Remote Data Source mengambil data dari API.
5. Local Data Source menyimpan atau mengambil data dari penyimpanan lokal.
6. Dio Auth Interceptor secara otomatis menambahkan token autentikasi pada setiap request API.
7. Data dikembalikan ke Repository lalu diteruskan ke UI.

---

# Pembagian Tugas Anggota

| Nama Anggota | Tugas                     | Branch                            |
| ------------ | ------------------------- | --------------------------------- |
| Fajrul       | Remote Data Source        | feature/remote-datasource         |
| Fakhrul      | Local Data Source         | feature/local-datasource          |
| Fhandy       | Repository Implementation | feature/repository-implementation |
| Gema         | Dio Auth Interceptor      | feature/dio-auth-interceptor      |

---

# Manajemen Proyek GitHub

## GitHub Issues

Setiap komponen dibuat sebagai Issue terpisah:

| Issue                     | Penanggung Jawab |
| ------------------------- | ---------------- |
| Remote Data Source        | Fajrul           |
| Local Data Source         | Fakhrul          |
| Repository Implementation | Fhandy           |
| Dio Auth Interceptor      | Gema             |




# Kesimpulan

Implementasi Repository Pattern membantu memisahkan logika aplikasi dari sumber data sehingga struktur proyek menjadi lebih modular, mudah dipelihara, mudah diuji, dan lebih siap untuk pengembangan skala besar. Penggunaan GitHub Issues, Project Board, Pull Request, dan Code Review juga mendukung kolaborasi tim yang lebih terorganisir dan profesional.

