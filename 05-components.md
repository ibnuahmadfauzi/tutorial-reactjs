# Components

Component itu seperti Function yang mengembalikan elemen HTML.

Component adalah kode yang bisa digunakan kembali dengan memanggil nama dari component nya. Sama seperti function, namun bedanya dia mengembalikan elemen HTML.

Ada 2 tipe component:

- Class Component
- Function Component

Namun dalam tutorial ini kita hanya akan membahas Function Component.

## Membuat Component Pertama

``` javascript
.....
function Book() {
  return <h1>Koleksi Buku</h1>;
}
.....
```

Sama seperti membuat function, namun untuk component pembuatan namanya harus dimulai dengan huruf besar.

## Merender Component

Untuk merender kita bisa memanggil nama componentnya dengan penulisan seperti elemen HTML

``` javascript
.....
function Book() {
  return <h1>Koleksi Buku</h1>;
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Book />);
```

## Nested Component

Kita juga bisa menggunakan component di dalam component lain

``` javascript
.....
function DaftarBuku() {
  return (
    <table border={1} cellPadding={8} cellSpacing={0}>
      <thead>
        <tr>
          <th>Judul</th>
          <th>Tahun</th>
          <th>Penulis</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Belajar React Dasar</td>
          <td>2022</td>
          <td>Ibnu Ahmad Fauzi</td>
        </tr>
        <tr>
          <td>Pemrograman JavaScript Modern</td>
          <td>2021</td>
          <td>Andi Pratama</td>
        </tr>
        <tr>
          <td>Dasar-dasar HTML & CSS</td>
          <td>2020</td>
          <td>Siti Rahmawati</td>
        </tr>
        <tr>
          <td>Fullstack Web Developer</td>
          <td>2023</td>
          <td>Budi Santoso</td>
        </tr>
        <tr>
          <td>Mastering Node.js</td>
          <td>2024</td>
          <td>Ade Firmansyah</td>
        </tr>
      </tbody>
    </table>
  );
}

function Book() {
  return (
    <>
      <h1>Koleksi Buku</h1>
      <DaftarBuku />
    </>
  );
}
.....
```
