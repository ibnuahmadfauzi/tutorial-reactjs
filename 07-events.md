# Events

Sama seperti Document Object Model, React bisa bereaksi dengan aksi yang dilakukan oleh user, seperti melakukan click, change, mouseover, dan sebagainya.

## Menambahkan Event

Penulisan nama event di React menggunakan penulisan camelCase, contohnya <code>onClick</code>. Berikut contoh membuat event di dalam function

``` javascript
.....
function Book(props) {
  const download = () => {
    alert("Download buku berhasil!");
  }
  return (
    <>
      <h1>Koleksi Buku</h1>
      <p>Kategori : {props.info.kategori}</p>
      <p>Bahasa : {props.info.bahasa}</p>
      <button onClick={download}>Download File</button>
    </>
  );
}
.....
```

## Mengirim Argument

Selain melakukan aksi, event juga bisa digunakan untuk mengirimkan suatu argumen ketika user melakukan aksi tersebut

``` javascript
.....
function Book(props) {
  const download = (kategori) => {
    alert(`Buku dengan kategori ${kategori} berhasil di download!`);
  }
  return (
    <>
      <h1>Koleksi Buku</h1>
      <p>Kategori : {props.info.kategori}</p>
      <p>Bahasa : {props.info.bahasa}</p>
      <button onClick={() => download(props.info.kategori)}>Download File</button>
    </>
  );
}
.....
```