# glowup-store
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GlowUp Accesorios</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        .product { display: inline-block; margin: 20px; }
        .cart { position: fixed; top: 10px; right: 10px; background: #fff; padding: 10px; border: 1px solid #ddd; }
    </style>
</head>
<body>
    <h1>Bienvenido a GlowUp Accesorios</h1>
    <div id="products">
        <div class="product">
            <img src="producto1.jpg" width="150" alt="Producto 1">
            <p>Collar Elegante - $200</p>
            <button onclick="addToCart('Collar Elegante', 200)">Agregar al Carrito</button>
        </div>
        <div class="product">
            <img src="producto2.jpg" width="150" alt="Producto 2">
            <p>Pulsera de Plata - $150</p>
            <button onclick="addToCart('Pulsera de Plata', 150)">Agregar al Carrito</button>
        </div>
    </div>
    <div class="cart">
        <h2>Carrito</h2>
        <ul id="cart-list"></ul>
        <p>Total: $<span id="total">0</span></p>
    </div>
    <script>
        let total = 0;
        function addToCart(product, price) {
            let cartList = document.getElementById('cart-list');
            let item = document.createElement('li');
            item.textContent = `${product} - $${price}`;
            cartList.appendChild(item);
            total += price;
            document.getElementById('total').textContent = total;
        }
    </script>
</body>
</html>
