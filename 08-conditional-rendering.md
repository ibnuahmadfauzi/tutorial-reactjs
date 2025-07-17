# Conditional Rendering

Dalam React kita bisa merender component melalui kondisi tertentu.

## IF Statement

``` javascript
.....
function BukuTersedia() {
  return <h1>Buku Tersedia</h1>;
}

function BukuTidakTersedia() {
  return <h1>Buku Tidak Tersedia</h1>;
}

function Book(props) {
  if (props.info.status === "Tersedia") {
      return (
        <>
          <h1>Koleksi Buku</h1>
          <p>Kategori : {props.info.kategori}</p>
          <p>Bahasa : {props.info.bahasa}</p>
          <BukuTersedia />
        </>
      );
  } else {
      return (
        <>
          <h1>Koleksi Buku</h1>
          <p>Kategori : {props.info.kategori}</p>
          <p>Bahasa : {props.info.bahasa}</p>
          <BukuTidakTersedia />
        </>
      )
  }
}

const infoBuku = {
  kategori: "Novel",
  bahasa: "Indonesia",
  status: "Tersedia"
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Book info={infoBuku} />);
```