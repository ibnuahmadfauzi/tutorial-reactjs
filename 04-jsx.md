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