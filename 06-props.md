# Props

Props merupakan argumen yang dikirim dari component, dia didefinisikan seperti artibut HTML namun digunakan di component.

``` javascript
.....
function Book(props) {
  return (
    <>
      <h1>Koleksi Buku</h1>
      <p>Kategori : {props.kategori}</p>
      <p>Bahasa : {props.bahasa}</p>
    </>
  );
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Book kategori="Novel" bahasa="Indonesia" />);
```

Atau bisa juga mengirim file dalam bentuk object

``` javascript
.....
function Book(props) {
  return (
    <>
      <h1>Koleksi Buku</h1>
      <p>Kategori : {props.info.kategori}</p>
      <p>Bahasa : {props.info.bahasa}</p>
    </>
  );
}

const infoBuku = {
  kategori: "Novel",
  bahasa: "Indonesia"
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Book info={infoBuku} />);
```