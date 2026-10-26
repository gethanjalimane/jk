
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NOVA | Clothing Brand</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background: #f5f5f0;
      color: #171717;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 22px 8%;
      background: #111;
      color: white;
    }

    .logo {
      font-size: 28px;
      font-weight: bold;
      letter-spacing: 3px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      font-size: 14px;
    }

    .hero {
      min-height: 500px;
      display: flex;
      align-items: center;
      padding: 60px 8%;
      background: #d9d8cf;
    }

    .hero-content {
      max-width: 550px;
    }

    .hero h1 {
      font-size: clamp(45px, 8vw, 85px);
      line-height: 0.95;
      margin: 20px 0;
    }

    .hero p {
      line-height: 1.8;
      margin-bottom: 25px;
    }

    .btn {
      display: inline-block;
      padding: 14px 25px;
      background: #111;
      color: white;
      text-decoration: none;
      border: none;
      cursor: pointer;
    }

    .collection {
      padding: 65px 8%;
    }

    .collection h2 {
      font-size: 35px;
      margin-bottom: 30px;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .product {
      background: white;
      padding-bottom: 20px;
    }

    .product img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      display: block;
    }

    .product h3,
    .product p {
      margin: 14px 15px;
    }

    .product button {
      margin: 0 15px;
      padding: 10px 16px;
      background: #111;
      color: white;
      border: none;
      cursor: pointer;
    }

    .about {
      padding: 65px 8%;
      background: #d9d8cf;
      text-align: center;
    }

    .about h2 {
      margin-bottom: 20px;
      font-size: 35px;
    }

    .about p {
      max-width: 650px;
      margin: auto;
      line-height: 1.8;
    }

    footer {
      background: #111;
      color: white;
      text-align: center;
      padding: 30px 15px;
      line-height: 2;
    }

    @media (max-width: 700px) {
      header {
        padding: 20px 5%;
        flex-wrap: wrap;
        gap: 15px;
      }

      nav a {
        margin-left: 10px;
      }

      .hero {
        padding: 50px 6%;
      }

      .products {
        grid-template-columns: 1fr;
      }

      .product img {
        height: 350px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="logo">NOVA®</div>
    <nav>
      <a href="#home">Home</a>
      <a href="#shop">Shop</a>
      <a href="#about">About</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <div class="hero-content">
      <p>NEW COLLECTION 2026</p>
      <h1>WEAR YOUR<br>IDENTITY.</h1>
      <p>
        Discover premium everyday fashion.
        Made for comfort, confidence and your own style.
      </p>
      <a href="#shop" class="btn">SHOP COLLECTION</a>
    </div>
  </section>

  <section class="collection" id="shop">
    <h2>OUR COLLECTION</h2>

    <div class="products">

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=700&q=80"
          alt="White T-shirt">
        <h3>Classic T-Shirt</h3>
        <p>₹799</p>
        <button onclick="addToCart('Classic T-Shirt', 799)">
          Add to Cart
        </button>
      </div>

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1551028719-00167b16eac5?auto=format&fit=crop&w=700&q=80"
          alt="Fashion jacket">
        <h3>Premium Jacket</h3>
        <p>₹1,999</p>
        <button onclick="addToCart('Premium Jacket', 1999)">
          Add to Cart
        </button>
      </div>

      <div class="product">
        <img
          src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=crop&w=700&q=80"
          alt="Casual fashion">
        <h3>Casual Wear</h3>
        <p>₹1,199</p>
        <button onclick="addToCart('Casual Wear', 1199)">
          Add to Cart
        </button>
      </div>

    </div>
  </section>

  <section class="about" id="about">
    <h2>ABOUT OUR BRAND</h2>
    <p>
      NOVA is a modern clothing brand built for people
      who want to express themselves through fashion.
      We believe in simple designs, quality clothing
      and a style that belongs to you.
    </p>
  </section>

  <footer>
    <h2>NOVA®</h2>
    <p>Wear Your Identity.</p>
    <p id="cart">Your cart: 0 items</p>
    <p>&copy; 2026 NOVA Clothing. All rights reserved.</p>
  </footer>

  <script>
    let cart = [];
    
    function addToCart(name, price) {
      cart.push({ name: name, price: price });

      document.getElementById("cart").textContent =
        "Your cart: " + cart.length +
        " items | Total: ₹" +
        cart.reduce((sum, item) => sum + item.price, 0)
          .toLocaleString("en-IN");

      alert(name + " added to your cart!");
    }
  </script>

</body>
</html>
