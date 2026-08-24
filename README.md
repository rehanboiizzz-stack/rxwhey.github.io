<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>RXHN GETS | Premium Fitness Supplements</title>

  <meta name="description"
        content="RXHN GETS - Discover premium fitness supplements and nutrition products.">

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #080808;
      --bg-light: #111111;
      --card: #151515;
      --yellow: #ffb800;
      --yellow-light: #ffca45;
      --white: #ffffff;
      --gray: #a0a0a0;
      --border: rgba(255,255,255,0.09);
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: "Montserrat", Arial, sans-serif;
      overflow-x: hidden;
    }

    /* ================= NAVBAR ================= */

    nav {
      height: 76px;
      padding: 0 7%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: rgba(8,8,8,0.96);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 1000;
      backdrop-filter: blur(15px);
    }

    .logo {
      font-size: 1.6rem;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--yellow);
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 30px;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--white);
      font-size: 0.8rem;
      font-weight: 700;
      opacity: 0.7;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: var(--yellow);
      opacity: 1;
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 18px;
    }

    .cart {
      background: var(--yellow);
      color: black;
      padding: 10px 15px;
      border-radius: 8px;
      font-size: 0.8rem;
      font-weight: 800;
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 620px;
      padding: 80px 8%;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(
          circle at 85% 50%,
          rgba(255,184,0,0.16),
          transparent 28%
        ),
        linear-gradient(135deg,#080808,#101010);
    }

    .hero-content {
      width: 60%;
      position: relative;
      z-index: 2;
    }

    .hero-tag {
      display: inline-block;
      padding: 9px 15px;
      border-radius: 30px;
      color: var(--yellow);
      border: 1px solid rgba(255,184,0,0.3);
      background: rgba(255,184,0,0.07);
      font-size: 0.7rem;
      font-weight: 800;
      letter-spacing: 1px;
      margin-bottom: 25px;
    }

    .hero h1 {
      font-size: clamp(3rem,7vw,7rem);
      font-weight: 900;
      line-height: 0.88;
      letter-spacing: -5px;
    }

    .hero h1 span {
      color: var(--yellow);
    }

    .hero p {
      max-width: 560px;
      color: var(--gray);
      line-height: 1.8;
      margin-top: 25px;
      font-size: 0.95rem;
    }

    .hero-buttons {
      display: flex;
      gap: 15px;
      margin-top: 35px;
    }

    .btn {
      text-decoration: none;
      padding: 15px 25px;
      border-radius: 8px;
      font-size: 0.8rem;
      font-weight: 800;
      transition: 0.3s;
    }

    .btn-primary {
      background: var(--yellow);
      color: black;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: var(--yellow-light);
      box-shadow: 0 15px 35px rgba(255,184,0,0.25);
    }

    .btn-secondary {
      border: 1px solid var(--border);
      color: white;
    }

    .btn-secondary:hover {
      border-color: var(--yellow);
    }

    /* ================= HERO PRODUCT ================= */

    .hero-product {
      position: absolute;
      right: 10%;
      width: 420px;
      height: 520px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-product::before {
      content: "";
      width: 450px;
      height: 450px;
      border-radius: 50%;
      background: rgba(255,184,0,0.1);
      filter: blur(40px);
      position: absolute;
    }

    .hero-product img {
      position: relative;
      width: 100%;
      height: 100%;
      object-fit: contain;
      filter: drop-shadow(0 30px 30px rgba(0,0,0,0.7));
      transition: 0.4s;
    }

    .hero-product img:hover {
      transform: scale(1.04);
    }

    /* ================= TRUST BAR ================= */

    .trust-bar {
      display: grid;
      grid-template-columns: repeat(4,1fr);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .trust-item {
      padding: 25px;
      text-align: center;
      border-right: 1px solid var(--border);
    }

    .trust-item:last-child {
      border-right: none;
    }

    .trust-item h3 {
      font-size: 0.8rem;
      margin-bottom: 7px;
    }

    .trust-item p {
      color: var(--gray);
      font-size: 0.7rem;
    }

    /* ================= PRODUCTS ================= */

    .products-section {
      padding: 100px 8%;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 30px;
      margin-bottom: 40px;
    }

    .section-header small {
      color: var(--yellow);
      font-size: 0.7rem;
      letter-spacing: 2px;
      font-weight: 800;
    }

    .section-header h2 {
      margin-top: 10px;
      font-size: clamp(2.2rem,4vw,4rem);
      font-weight: 900;
      letter-spacing: -2px;
    }

    .section-header p {
      color: var(--gray);
      font-size: 0.85rem;
      max-width: 380px;
      line-height: 1.7;
    }

    /* ================= SEARCH ================= */

    .search-container {
      display: flex;
      max-width: 550px;
      margin-bottom: 40px;
    }

    .search-container input {
      width: 100%;
      height: 50px;
      padding: 0 18px;
      border: 1px solid var(--border);
      background: #121212;
      color: white;
      outline: none;
      border-radius: 9px 0 0 9px;
      font-family: inherit;
    }

    .search-container button {
      border: none;
      background: var(--yellow);
      color: black;
      padding: 0 22px;
      font-weight: 800;
      cursor: pointer;
      border-radius: 0 9px 9px 0;
    }

    /* ================= PRODUCT GRID ================= */

    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
      gap: 22px;
    }

    .product-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 18px;
      overflow: hidden;
      transition: 0.3s;
    }

    .product-card:hover {
      transform: translateY(-8px);
      border-color: rgba(255,184,0,0.5);
      box-shadow: 0 25px 60px rgba(0,0,0,0.5);
    }

    .product-image {
      height: 310px;
      background: white;
      padding: 20px;
      position: relative;
    }

    .product-image img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      display: block;
      transition: 0.3s;
    }

    .product-card:hover .product-image img {
      transform: scale(1.06);
    }

    .badge {
      position: absolute;
      top: 14px;
      left: 14px;
      z-index: 2;
      background: var(--yellow);
      color: black;
      padding: 7px 10px;
      border-radius: 6px;
      font-size: 0.6rem;
      font-weight: 900;
    }

    .product-info {
      padding: 20px;
    }

    .brand {
      color: var(--yellow);
      font-size: 0.65rem;
      font-weight: 800;
      letter-spacing: 1px;
    }

    .product-info h3 {
      margin-top: 8px;
      font-size: 1rem;
      line-height: 1.5;
      min-height: 48px;
    }

    .rating {
      margin-top: 10px;
      color: var(--yellow);
      font-size: 0.75rem;
    }

    .product-footer {
      margin-top: 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
    }

    .price {
      font-size: 1.3rem;
      font-weight: 900;
    }

    .view-btn {
      text-decoration: none;
      background: var(--yellow);
      color: black;
      padding: 11px 15px;
      border-radius: 8px;
      font-size: 0.7rem;
      font-weight: 900;
      transition: 0.3s;
    }

    .view-btn:hover {
      transform: scale(1.05);
    }

    /* ================= CTA ================= */

    .cta {
      margin: 0 8% 100px;
      padding: 80px;
      border-radius: 25px;
      background:
        radial-gradient(
          circle at 85% 30%,
          rgba(255,184,0,0.25),
          transparent 30%
        ),
        #151515;

      border: 1px solid var(--border);
    }

    .cta small {
      color: var(--yellow);
      font-weight: 800;
      letter-spacing: 2px;
    }

    .cta h2 {
      margin-top: 15px;
      font-size: clamp(2.5rem,5vw,5rem);
      line-height: 0.95;
      letter-spacing: -3px;
      max-width: 800px;
    }

    .cta h2 span {
      color: var(--yellow);
    }

    .cta p {
      color: var(--gray);
      margin-top: 25px;
      max-width: 550px;
      line-height: 1.7;
      font-size: 0.9rem;
    }

    /* ================= FOOTER ================= */

    footer {
      border-top: 1px solid var(--border);
      padding: 60px 20px;
      text-align: center;
    }

    footer h2 {
      font-size: 2rem;
      font-weight: 900;
    }

    footer h2 span {
      color: var(--yellow);
    }

    footer p {
      margin-top: 12px;
      color: var(--gray);
      font-size: 0.75rem;
    }

    /* ================= MOBILE ================= */

    @media (max-width: 850px) {

      nav {
        padding: 0 20px;
      }

      .nav-links {
        display: none;
      }

      .hero {
        padding: 70px 25px;
        min-height: 700px;
      }

      .hero-content {
        width: 100%;
        z-index: 3;
      }

      .hero-product {
        width: 100%;
        right: 0;
        opacity: 0.22;
      }

      .trust-bar {
        grid-template-columns: repeat(2,1fr);
      }

      .trust-item {
        border-bottom: 1px solid var(--border);
      }

      .products-section {
        padding: 70px 20px;
      }

      .section-header {
        display: block;
      }

      .section-header p {
        margin-top: 20px;
      }

      .cta {
        margin: 0 20px 70px;
        padding: 50px 25px;
      }

    }

    @media (max-width: 500px) {

      .logo {
        font-size: 1.2rem;
      }

      .cart {
        padding: 8px 10px;
      }

      .hero h1 {
        font-size: 3.5rem;
      }

      .hero-buttons {
        flex-direction: column;
      }

      .btn {
        text-align: center;
      }

      .product-grid {
        grid-template-columns: 1fr 1fr;
        gap: 10px;
      }

      .product-image {
        height: 200px;
        padding: 10px;
      }

      .product-info {
        padding: 12px;
      }

      .product-info h3 {
        font-size: 0.75rem;
        min-height: 60px;
      }

      .product-footer {
        flex-direction: column;
        align-items: stretch;
      }

      .price {
        font-size: 1rem;
      }

      .view-btn {
        text-align: center;
      }

    }

  </style>
</head>

<body>


  <!-- ================= NAVBAR ================= -->

  <nav>

    <div class="logo">
      RXHN <span>GETS</span>
    </div>

    <ul class="nav-links">
      <li><a href="#home">HOME</a></li>
      <li><a href="#products">PRODUCTS</a></li>
      <li><a href="#about">ABOUT</a></li>
    </ul>

    <div class="nav-right">
      <div class="cart">🛒 SHOP</div>
    </div>

  </nav>


  <!-- ================= HERO ================= -->

  <section class="hero" id="home">

    <div class="hero-content">

      <div class="hero-tag">
        PREMIUM FITNESS NUTRITION
      </div>

      <h1>
        FUEL YOUR<br>
        <span>NEXT LEVEL.</span>
      </h1>

      <p>
        Discover premium fitness supplements and nutrition products
        selected for serious training, muscle growth and recovery.
      </p>

      <div class="hero-buttons">

        <a href="#products" class="btn btn-primary">
          SHOP PRODUCTS →
        </a>

        <a href="#about" class="btn btn-secondary">
          EXPLORE
        </a>

      </div>

    </div>


    <!-- YOUR REAL PRODUCT IMAGE -->

    <div class="hero-product">

      <img
        src="https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg"
        alt="Avvatar Whey Protein"
      >

    </div>

  </section>


  <!-- ================= TRUST BAR ================= -->

  <section class="trust-bar">

    <div class="trust-item">
      <h3>✓ PREMIUM PICKS</h3>
      <p>Quality fitness products</p>
    </div>

    <div class="trust-item">
      <h3>💪 FITNESS FOCUSED</h3>
      <p>For your training goals</p>
    </div>

    <div class="trust-item">
      <h3>⚡ TOP SUPPLEMENTS</h3>
      <p>Popular nutrition choices</p>
    </div>

    <div class="trust-item">
      <h3>★ BEST BRANDS</h3>
      <p>Discover trusted products</p>
    </div>

  </section>


  <!-- ================= PRODUCTS ================= -->

  <section class="products-section" id="products">

    <div class="section-header">

      <div>

        <small>RXHN COLLECTION</small>

        <h2>
          FEATURED PRODUCTS
        </h2>

      </div>

      <p>
        Explore popular fitness supplements and discover products
        that match your training goals.
      </p>

    </div>


    <!-- SEARCH -->

    <div class="search-container">

      <input
        type="text"
        id="searchInput"
        placeholder="Search supplements..."
      >

      <button onclick="searchProducts()">
        SEARCH
      </button>

    </div>


    <!-- PRODUCT GRID -->

    <div class="product-grid" id="productGrid">


      <!-- PRODUCT 1 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge">
            BESTSELLER
          </span>

          <img
            src="https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg"
            alt="Avvatar Whey Protein Belgian Chocolate"
          >

        </div>

        <div class="product-info">

          <div class="brand">
            AVVATAR
          </div>

          <h3>
            Avvatar Alpha Whey Protein 1 KG
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="product-footer">

            <div class="price">
              ₹1,599
            </div>

            <a
              href="https://avataarindia.com/product/alpha-whey-belgian-chocolate-flavour-1-kg-2509104129-263"
              target="_blank"
              class="view-btn"
            >
              BUY NOW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 2 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge">
            2 KG PACK
          </span>

          <!-- SAME REAL AVVATAR IMAGE -->

          <img
            src="https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg"
            alt="Avvatar Whey Protein 2 KG"
          >

        </div>

        <div class="product-info">

          <div class="brand">
            AVVATAR
          </div>

          <h3>
            Avvatar Alpha Whey Protein 2 KG
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="product-footer">

            <div class="price">
              ₹3,113
            </div>

            <a
              href="https://avataarindia.com/"
              target="_blank"
              class="view-btn"
            >
              BUY NOW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 3 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge">
            CREATINE
          </span>

          <img
            src="https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg"
            alt="Creatine Supplement"
          >

        </div>

        <div class="product-info">

          <div class="brand">
            FITNESS
          </div>

          <h3>
            Creatine Monohydrate
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="product-footer">

            <div class="price">
              ₹899
            </div>

            <a href="#" class="view-btn">
              BUY NOW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 4 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge">
            PROTEIN
          </span>

          <img
            src="https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg"
            alt="Premium Protein"
          >

        </div>

        <div class="product-info">

          <div class="brand">
            RXHN PICKS
          </div>

          <h3>
            Premium Whey Protein
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="product-footer">

            <div class="price">
              ₹1,299
            </div>

            <a href="#" class="view-btn">
              BUY NOW →
            </a>

          </div>

        </div>

      </article>


    </div>

  </section>


  <!-- ================= ABOUT / CTA ================= -->

  <section class="cta" id="about">

    <small>
      RXHN GETS
    </small>

    <h2>
      TRAIN HARDER.<br>
      <span>CHOOSE BETTER.</span>
    </h2>

    <p>
      A clean place to discover premium fitness supplements
      and nutrition products for your next level.
    </p>

    <br>

    <a href="#products" class="btn btn-primary">
      EXPLORE PRODUCTS →
    </a>

  </section>


  <!-- ================= FOOTER ================= -->

  <footer>

    <h2>
      RXHN <span>GETS</span>
    </h2>

    <p>
      Premium Fitness & Nutrition Products
    </p>

    <p style="margin-top:25px;">
      © 2026 RXHN GETS. All Rights Reserved.
    </p>

  </footer>


  <!-- ================= JAVASCRIPT ================= -->

  <script>

    function searchProducts() {

      const input =
        document
          .getElementById("searchInput")
          .value
          .toLowerCase();

      const products =
        document.querySelectorAll(".product");

      products.forEach(product => {

        const text =
          product.innerText.toLowerCase();

        if (text.includes(input)) {

          product.style.display = "block";

        } else {

          product.style.display = "none";

        }

      });

    }


    document
      .getElementById("searchInput")
      .addEventListener(
        "keyup",
        searchProducts
      );

  </script>

</body>
</html>
