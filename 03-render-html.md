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

