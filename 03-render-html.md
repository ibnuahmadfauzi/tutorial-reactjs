# Render HTML

Tujuan utama React adalah merender HTML ke dalam halaman web. Proses render menggunakan function <code>createRoot()</code> dan method <code>render()</code>.

## createRoot Function

Function ini menerima 1 argumen dalam parameternya, yaitu elemen HTML.

## render Method

Method ini digunakan untuk mendefinisikan React component yang akan di render.

Lalu component tersebut dirender dimana ?

Jika melihat struktur utama dari aplikasi ini maka kita akan menemukan file <code>/public/index.html</code> dengan elemen <code>div</code> yang memiliki atribut <code>id="root"</code>. Ditempat tersebutlah React component dirender.

``` html
.....
<noscript>You need to enable JavaScript to run this app.</noscript>
<div id="root"></div>
.....
```

Berikut contoh render dari file <code>index.js</code>

``` javascript
const myFirstElement = <h1>Hello, World!</h1>;
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myFirstElement);
```

> Nilai <code>id</code> yang digunakan tidak selalu root, ini hanya standard convention saja.

## Kode HTML

Dalam menggunakan React untuk penulisan kode HTML disarankan menggunakan penulisan JSX yang mana memungkinkan kita menulis HTML ke dalam kode JavaScript dengan mudah. Berikut contohnya

``` javascript
import React from "react";
import ReactDOM from "react-dom/client";

const myFirstElement = (
  <table border={1} cellPadding={8} cellSpacing={0}>
    <thead>
      <tr>
        <th>Nama</th>
        <th>Jurusan</th>
        <th>Universitas</th>
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
root.render(myFirstElement);
```
