# Getting Started

> Untuk menggunakan Ract dalam production, kita membutuhkan <code>npm</code> yang didapatkan ketika menginstal <code>NodeJS</code>

Untuk mendapat gambaran umum tentang React, kita bisa memasukkan kode React ke dalam dokumen HTML, namun untuk proses produksi kita perlu menyiapkan React Environment menggunakan npm dan NodeJS.

## Memasukkan React ke Dokumen HTML

Buat file dengan nama <code>index.html</code> lalu isi dengan script berikut:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script
      src="https://unpkg.com/react@18/umd/react.development.js"
      crossorigin
    ></script>
    <script
      src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"
      crossorigin
    ></script>
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
