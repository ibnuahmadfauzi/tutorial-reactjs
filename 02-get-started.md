# Getting Started

> Untuk menggunakan Ract dalam production, kita membutuhkan <code>npm</code> yang didapatkan ketika menginstal <code>NodeJS</code>

Untuk mendapat gambaran umum tentang React, kita bisa memasukkan kode React ke dalam dokumen HTML, namun untuk proses produksi kita perlu menyiapkan React Environment menggunakan npm dan NodeJS.

## Memasukkan React ke Dokumen HTML

Buat file dengan nama <code>index.html</code> lalu isi dengan script berikut:

```html
<!DOCTYPE html>
<html lang="en">

<head>
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Document</title>

  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
</head>

<body>
  <div id="mydiv"></div>

  <script type="text/babel">
    function Hello() {
      return <h1>Hello World!</h1>;
    }

    const container = document.getElementById("mydiv");
    const root = ReactDOM.createRoot(container);
    root.render(<Hello />);
  </script>
</body>

</html>
```

Untuk menggunakan React di dokumen HTML, sertakan 3 script untuk melakukan embed library React nya, 2 script untuk memasukkan kode React, dan 1 untuk memasukkan <code>Babel</code> yang digunakan untuk memungkinkan menulis <code>JSX</code> dan <code>ES6</code> di browser lama.

Cara ini cocok untuk sekedar menguji beberapa kode Ract, namun untuk produksi kita memerlukan React Environment.

## Installasi React Environment

Ketika menginstall NodeJS, kita juga mendapatkan npm dan npx. Dengan ini kita bisa membuat aplikasi React menggunakan <code>create-react-app</code>.

> Pastikan tidak menggunakan installasi global, agar ketika membuat project baru selalu mendapat versi yang terbaru.

Berikut kita buat project dengan nama <code>my-app</code>, tulis perintah berikut di Command Line / Terminal

```
npx create-react-app my-app
```

<code>create-react-app</code> akan menyiapkan semua yang kita butuhkan untuk menjalankan aplikasi React.

## Menjalankan React Application

Sekarang aplikasi sudah siap dijalankan. Masuk ke folder aplikasinya

```
cd my-react-app
```

Jalankan dengan perintah

```
npm start
```

Biasanya halaman browser akan otomatis terbuka jika proses menjalankan servernya sudah selesai. Jika tidak, silahkan kunjungi alamat <code>localhost:3000</code> di addrss bar.