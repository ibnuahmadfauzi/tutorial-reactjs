# JSX

## Apa Itu JSX ?

- Singkatan dari JavaScript XML
- Memungkinkan menulis HTML ke dalam React
- Membuat penulisan HTML ke dalam React menjadi lebih mudah

# Coding JSX

JSX memungkinkan kita menuliskan elemen HTML ke dalam JavaScript dan membuat DOM tanpa method <code>createElement()</code> atau <code>appendChild()</code>. 

> Sebenarnya kita tidak wajib menggunakan JSX, namun dengan JSX sangat dimudahkan dalam banyak proses pengembangan aplikasi React.

Contoh tanpa JSX

``` javascript
.....
const myElement = React.createElement('h1', {}, 'Kode Tanpa JSX!');
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

Dengan menggunakan JSX

``` javascript
..... 
const myElement = <h1>Kode Menggunakan JSX!</h1>;
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

Seperti yang kalian lihat, dengan JSX kita bisa langsung memasukkan elemen HTMLnya tanpa method tambahan. JSX merupakan ekstensi dari bahasa JavaScript dengan basis ES6 yang diterjemahka ke dalam JavaScript ketika runtime.

## Expressions

Kita bisa menempatkan expression seperti operasi matematika, pemanggilan variabel, pemanggilan function, dsb. ke dalam kode JSX menggunakan curly braces <code>{ }</code>

``` javascript
.....
const dataMahasiswa = [
  {
    nama: "Fauziyah Meitaya",
    jurusan: "Pendidikan Matematika"
  }
];
const myElement = <h3>Nama : {dataMahasiswa[0].nama}</h3>;
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

## Memasukkan Banyak Elemen HTML

Untuk menulis lebih dari satu elmen, pastikan ada satu elemen yang digunakan sebagai parent

``` javascript
.....
const myElement = (
  <table border={1} cellPadding={8} cellSpacing={0}>
    <thead>
      <tr>
        <th>Nama</th>
        <th>Jurusan</th>
        <th>Kampus</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Ibnu Ahmad Fauzi</td>
        <td>Teknik Informatika</td>
        <td>Universitas Islam Balitar</td>
      </tr>
      <tr>
        <td>Fauziyah Meitaya</td>
        <td>Pendidikan Matematika</td>
        <td>Universitas Negeri Malang</td>
      </tr>
    </tbody>
  </table>
);
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

Pada kasus di atas kita punya elemen paling atas yaitu <code>table</code> Jika tidak punya elemen lain untuk menjadi parent, gunakan elemen <code>div</code> atau <code>fragmen</code> yaitu menggunakan elemen kosongan <code><> ... </></code>

``` javascript
.....
const myElement = (
  <>
    <h3>Daftar Mahasiswa</h3>
    <table border={1} cellPadding={8} cellSpacing={0}>
      <thead>
        <tr>
          <th>Nama</th>
          <th>Jurusan</th>
          <th>Kampus</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Ibnu Ahmad Fauzi</td>
          <td>Teknik Informatika</td>
          <td>Universitas Islam Balitar</td>
        </tr>
        <tr>
          <td>Fauziyah Meitaya</td>
          <td>Pendidikan Matematika</td>
          <td>Universitas Negeri Malang</td>
        </tr>
      </tbody>
    </table>
  </>
);
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```

## Atribut class

Karena keyword <code>class</code> dalam JavaScript sudah digunakan, untuk menuliskan atribut dalam elemen HTML yang ada di JSX diganti menggunakan <code>className</code>

``` javascript
.....
<h3 className="judul">Daftar Mahasiswa</h3>
.....
```
