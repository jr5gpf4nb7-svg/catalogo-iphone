<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Importadora Xiaomi S.A.S – Catálogo iPhone</title>

<style>
    body {
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial;
        margin: 0;
        background: #f5f5f7;
        color: #333;
    }

    header {
        background: #000;
        padding: 20px;
        display: flex;
        align-items: center;
        gap: 15px;
        color: white;
        border-bottom: 1px solid #222;
    }

    header img {
        height: 60px;
    }

    header h1 {
        font-size: 24px;
        margin: 0;
        font-weight: 600;
    }

    .catalogo {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 22px;
        padding: 20px;
    }

    .card {
        background: white;
        padding: 18px;
        border-radius: 14px;
        box-shadow: 0 4px 16px rgba(0,0,0,0.08);
        text-align: center;
        transition: 0.25s ease;
    }

    .card:hover {
        transform: translateY(-4px);
    }

    .card img {
        width: 100%;
        border-radius: 12px;
        margin-bottom: 12px;
    }

    .btn-ws {
        margin-top:15px;
        background:#25D366;
        color:white;
        padding:10px;
        border-radius:10px;
        text-align:center;
        text-decoration:none;
        font-size:15px;
        font-weight:600;
        display:flex;
        align-items:center;
        justify-content:center;
        gap:8px;
        transition:0.35s ease;
        box-shadow:0 3px 8px rgba(0,0,0,0.10);
    }

    .btn-ws img {
        width:20px;
        height:20px;
        transition:0.35s ease;
    }

    .btn-ws:hover {
        transform:translateY(-2px) scale(1.03);
        box-shadow:0 6px 14px rgba(0,0,0,0.13);
        background:#23c65f;
    }

    .btn-ws:hover img {
        transform:scale(1.08);
    }

    .ws-floating {
        position: fixed;
        bottom: 22px;
        right: 20px;
        background: #25D366;
        padding: 14px;
        border-radius: 50%;
        box-shadow: 0 4px 14px rgba(0,0,0,0.25);
        z-index: 999;
        transition: 0.35s ease;
    }

    .ws-floating img {
        width: 34px;
    }

    .ws-floating:hover {
        transform: scale(1.08);
        background: #23c65f;
    }

    footer {
        text-align:center;
        padding:25px;
        margin-top:40px;
        background:#fff;
        font-size:18px;
        font-weight:600;
        color:#333;
        border-top:1px solid #ddd;
    }
</style>

</head>
<body>

<header>
    <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABAAAAAQACAYAAAB/HSuDAAAAAXNSR0IArs4c6QA... (RECORTADO) ...">
    <h1>IMPORTADORA XIAOMI S.A.S.</h1>
</header>

<div class="catalogo" id="catalogo"></div>

<!-- Botón flotante WhatsApp -->
<a class="ws-floating" href="https://wa.me/message/65PQF2H7MSY3P1" target="_blank">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg">
</a>

<footer>
    🚚 Ofrecemos envíos a nivel nacional seguros y confiables al 100%
</footer>

<script>
const modelos = [
    { nombre:"iPhone 8 Plus", precio:"$100", img:"https://images.unsplash.com/photo-1511707171634-5f897ff02aa9" },

    { nombre:"iPhone X", precio:"$120", img:"https://images.unsplash.com/photo-1517336714731-489689fd1ca8" },
    { nombre:"iPhone XR", precio:"$180", img:"https://images.unsplash.com/photo-1542751110-97427bbecf20" },
    { nombre:"iPhone XS", precio:"$140", img:"https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f" },

    { nombre:"iPhone 11", precio:"$170", img:"https://images.unsplash.com/photo-1591337676887-a217a6970a8e" },
    { nombre:"iPhone 11 Pro", precio:"$190", img:"https://images.unsplash.com/photo-1573497161157-9ba1e5faba3a" },
    { nombre:"iPhone 11 Pro Max", precio:"$220", img:"https://images.unsplash.com/photo-1573497491208-6b1acb260f5e" },

    { nombre:"iPhone 12", precio:"$250", img:"https://images.unsplash.com/photo-1603899122705-1c3a37b04e20" },
    { nombre:"iPhone 12 Pro", precio:"$275", img:"https://images.unsplash.com/photo-1603791452906-b9abcfb4c0aa" },
    { nombre:"iPhone 12 Pro Max", precio:"$300", img:"https://images.unsplash.com/photo-1604429532361-251c9eac6472" },

    { nombre:"iPhone 13", precio:"$330", img:"https://images.unsplash.com/photo-1632661678599-8661c7d34d77" },
    { nombre:"iPhone 13 Pro", precio:"$399", img:"https://images.unsplash.com/photo-1632606926706-b692d2dfc5c9" },
    { nombre:"iPhone 13 Pro Max", precio:"$470", img:"https://images.unsplash.com/photo-1632606926706-b692d2dfc5c9" },

    { nombre:"iPhone 14", precio:"$350", img:"https://images.unsplash.com/photo-1663494956746-5ef0a2a0d3d3" },
    { nombre:"iPhone 14 Plus", precio:"$380", img:"https://images.unsplash.com/photo-1663494956746-5ef0a2a0d3d3" },
    { nombre:"iPhone 14 Pro Max", precio:"$580", img:"https://images.unsplash.com/photo-1663494956723-ce8df40add21" },

    { nombre:"iPhone 15", precio:"$999", img:"https://images.unsplash.com/photo-1694899429779-375008651675" },
    { nombre:"iPhone 15 Pro Max", precio:"$700", img:"https://images.unsplash.com/photo-1694901446804-bd46c4c21c25" },

    { nombre:"iPhone 16", precio:"$600", img:"https://images.unsplash.com/photo-1523206489230-c012c64b2b48" },
    { nombre:"iPhone 16 Pro", precio:"$830", img:"https://images.unsplash.com/photo-1523206489230-c012c64b2b48" },
    { nombre:"iPhone 16 Pro Max", precio:"$980", img:"https://images.unsplash.com/photo-1517336714731-489689fd1ca8" },

    { nombre:"iPhone 17", precio:"$700", img:"https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f" },
    { nombre:"iPhone 17 Pro", precio:"$780", img:"https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f" },
    { nombre:"iPhone 17 Pro Max", precio:"$999", img:"https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f" }
];

let html = "";
modelos.forEach(m => {
    html += `
        <div class="card">
            <img src="${m.img}" alt="${m.nombre}">
            <h2>${m.nombre}</h2>
            <p><strong>Precio:</strong> ${m.precio}</p>

            <a class="btn-ws" 
                href="https://wa.me/message/65PQF2H7MSY3P1?text=Hola,%20quiero%20información%20del%20${encodeURIComponent(m.nombre)}"
                target="_blank">
                <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg">
                WhatsApp
            </a>
        </div>
    `;
});

document.getElementById("catalogo").innerHTML = html;
</script>

</body>
</html>
