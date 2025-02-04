<!DOCTYPE html>
<html lang="sk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fotografický Web</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 1em 0;
            text-align: center;
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        .gallery-item {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .gallery-item img {
            width: 100%;
            height: auto;
            display: block;
        }
        .item-info {
            padding: 10px;
            text-align: center;
        }
        .buy-button {
            background-color: #4CAF50;
            border: none;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Moje Fotografie</h1>
    </header>
    <div class="container">
        <section class="gallery">
            <div class="gallery-item">
                <img src="path/to/your/image1.jpg" alt="Fotografia 1">
                <div class="item-info">
                    <h3>Názov fotografie 1</h3>
                    <p>Popis fotografie 1</p>
                    <button onclick="addToCart('Fotografia 1', 10)" class="buy-button">Pridať do košíka</button>
                </div>
            </div>
            <!-- Pridajte viacero takýchto blokov pre ďalšie fotografie -->
        </section>
    </div>
    <script>
        let cart = [];

        function addToCart(name, price) {
            cart.push({name, price});
            alert(`Produkt ${name} bol pridaný do košíka.`);
            // V skutočnom prostredí by ste sem pridali kód pre integráciu s e-shopom alebo localStorage pre dočasnú úschovu
        }

        // Tento príklad je veľmi základný; pre plnú funkcionalitu potrebujete integrovať externé riešenia
    </script>
</body>
</html>
