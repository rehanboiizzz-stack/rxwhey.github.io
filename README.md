<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>RXHN GETS | Premium Fitness Supplements</title>

  <meta
    name="description"
    content="RXHN GETS - Discover premium fitness supplements, whey protein, creatine and more."
  >

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #090909;
      --card: #121212;
      --card2: #181818;
      --yellow: #ffb800;
      --white: #ffffff;
      --gray: #a3a3a3;
      --border: rgba(255,255,255,.09);
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

    /* NAVBAR */

    nav {
      height: 75px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 7%;
      border-bottom: 1px solid var(--border);
      background: rgba(9,9,9,.95);
      position: sticky;
      top: 0;
      z-index: 1000;
      backdrop-filter: blur(10px);
    }

    .logo {
      font-size: 1.5rem;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--yellow);
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 30px;
    }

    .nav-links a {
      color: var(--white);
      text-decoration: none;
      font-size: .85rem;
      font-weight: 600;
      opacity: .75;
      transition: .2s;
    }

    .nav-links a:hover {
      color: var(--yellow);
      opacity: 1;
    }

    .nav-icons {
      display: flex;
      gap: 18px;
      font-size: 1.2rem;
    }

    /* HERO */

    .hero {
      min-height: 650px;
      padding: 80px 8%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: relative;
      overflow: hidden;

      background:
        radial-gradient(
          circle at 75% 50%,
          rgba(255,184,0,.16),
          transparent 30%
        ),
        linear-gradient(
          90deg,
          #090909 30%,
          #101010
        );
    }

    .hero-text {
      width: 55%;
      z-index: 2;
    }

    .hero-tag {
      display: inline-block;
      color: var(--yellow);
      border: 1px solid rgba(255,184,0,.3);
      background: rgba(255,184,0,.08);
      padding: 8px 14px;
      border-radius: 50px;
      font-size: .75rem;
      font-weight: 700;
      margin-bottom: 22px;
    }

    .hero h1 {
      font-size: clamp(3rem,7vw,7rem);
      line-height: .9;
      font-weight: 900;
      letter-spacing: -5px;
    }

    .hero h1 span {
      color: var(--yellow);
    }

    .hero p {
      margin-top: 25px;
      max-width: 550px;
      color: var(--gray);
      line-height: 1.8;
      font-size: 1rem;
    }

    .hero-buttons {
      display: flex;
      gap: 15px;
      margin-top: 35px;
    }

    .btn {
      display: inline-block;
      padding: 15px 28px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 800;
      transition: .25s;
    }

    .btn-primary {
      background: var(--yellow);
      color: black;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 35px rgba(255,184,0,.25);
    }

    .btn-dark {
      border: 1px solid var(--border);
      color: white;
    }

    .btn-dark:hover {
      border-color: var(--yellow);
    }

    .hero-image {
      position: absolute;
      right: 5%;
      bottom: 0;
      width: 45%;
      height: 100%;
      display: flex;
      align-items: end;
      justify-content: center;
    }

    .hero-image img {
      width: 100%;
      max-width: 600px;
      height: 100%;
      object-fit: cover;
      object-position: center;
      filter: contrast(1.05);
      mask-image: linear-gradient(
        to bottom,
        black 75%,
        transparent 100%
      );
    }

    /* TRUST BAR */

    .trust {
      display: grid;
      grid-template-columns: repeat(4,1fr);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .trust-item {
      padding: 28px;
      text-align: center;
      border-right: 1px solid var(--border);
    }

    .trust-item:last-child {
      border-right: none;
    }

    .trust-item h3 {
      font-size: .9rem;
    }

    .trust-item p {
      margin-top: 7px;
      color: var(--gray);
      font-size: .75rem;
    }

    /* SECTION */

    section.products-section {
      padding: 100px 8%;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: end;
      margin-bottom: 45px;
    }

    .section-header small {
      color: var(--yellow);
      font-weight: 700;
      letter-spacing: 2px;
    }

    .section-header h2 {
      margin-top: 10px;
      font-size: clamp(2rem,4vw,3.5rem);
      letter-spacing: -2px;
    }

    .section-header p {
      color: var(--gray);
      max-width: 350px;
      line-height: 1.6;
      font-size: .85rem;
    }

    /* SEARCH */

    .search-box {
      display: flex;
      margin-bottom: 40px;
      max-width: 500px;
    }

    .search-box input {
      width: 100%;
      padding: 15px;
      border: 1px solid var(--border);
      background: #151515;
      color: white;
      outline: none;
      border-radius: 8px 0 0 8px;
    }

    .search-box button {
      padding: 0 22px;
      background: var(--yellow);
      border: none;
      cursor: pointer;
      font-weight: bold;
      border-radius: 0 8px 8px 0;
    }

    /* PRODUCTS */

    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
      gap: 22px;
    }

    .product-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      overflow: hidden;
      transition: .3s;
    }

    .product-card:hover {
      transform: translateY(-8px);
      border-color: rgba(255,184,0,.5);
      box-shadow: 0 25px 60px rgba(0,0,0,.4);
    }

    .product-image {
      height: 270px;
      background: white;
      padding: 15px;
      position: relative;
      overflow: hidden;
    }

    .product-image img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      transition: .4s;
    }

    .product-card:hover .product-image img {
      transform: scale(1.07);
    }

    .badge-product {
      position: absolute;
      top: 12px;
      left: 12px;
      background: var(--yellow);
      color: black;
      padding: 6px 10px;
      font-size: .65rem;
      font-weight: 800;
      border-radius: 5px;
    }

    .product-info {
      padding: 20px;
    }

    .product-brand {
      color: var(--yellow);
      font-size: .7rem;
      font-weight: 800;
      letter-spacing: 1px;
    }

    .product-info h3 {
      margin-top: 8px;
      font-size: 1rem;
      line-height: 1.5;
    }

    .rating {
      margin-top: 10px;
      color: var(--yellow);
      font-size: .75rem;
    }

    .price-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 18px;
    }

    .price {
      font-size: 1.25rem;
      font-weight: 800;
    }

    .buy {
      background: var(--yellow);
      color: black;
      text-decoration: none;
      padding: 10px 15px;
      border-radius: 7px;
      font-size: .75rem;
      font-weight: 800;
    }

    /* CTA */

    .cta {
      margin: 40px 8% 100px;
      padding: 70px 8%;
      border-radius: 25px;
      background:
        radial-gradient(
          circle at 80% 30%,
          rgba(255,184,0,.25),
          transparent 35%
        ),
        #151515;
      border: 1px solid var(--border);
    }

    .cta h2 {
      font-size: clamp(2rem,5vw,4rem);
      max-width: 700px;
      letter-spacing: -2px;
    }

    .cta h2 span {
      color: var(--yellow);
    }

    .cta p {
      margin-top: 20px;
      color: var(--gray);
      max-width: 500px;
      line-height: 1.7;
    }

    /* FOOTER */

    footer {
      padding: 50px 8%;
      border-top: 1px solid var(--border);
      text-align: center;
    }

    footer h2 {
      font-size: 1.8rem;
      font-weight: 900;
    }

    footer h2 span {
      color: var(--yellow);
    }

    footer p {
      margin-top: 12px;
      color: var(--gray);
      font-size: .8rem;
    }

    /* MOBILE */

    @media(max-width:800px) {

      nav {
        padding: 0 20px;
      }

      .nav-links {
        display: none;
      }

      .hero {
        min-height: 700px;
        padding: 80px 25px;
        align-items: flex-start;
      }

      .hero-text {
        width: 100%;
      }

      .hero h1 {
        letter-spacing: -3px;
      }

      .hero-image {
        opacity: .3;
        width: 100%;
        right: 0;
      }

      .trust {
        grid-template-columns: repeat(2,1fr);
      }

      .trust-item {
        border-bottom: 1px solid var(--border);
      }

      .section-header {
        display: block;
      }

      .section-header p {
        margin-top: 20px;
      }

      section.products-section {
        padding: 70px 20px;
      }

      .products {
        grid-template-columns: repeat(2,1fr);
        gap: 12px;
      }

      .product-image {
        height: 190px;
      }

      .product-info {
        padding: 14px;
      }

      .product-info h3 {
        font-size: .8rem;
      }

      .price-row {
        display: block;
      }

      .buy {
        display: block;
        text-align: center;
        margin-top: 12px;
      }

    }

  </style>
</head>

<body>

  <!-- NAVBAR -->

  <nav>
    <div class="logo">
      RXHN <span>GETS</span>
    </div>

    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Supplements</a></li>
      <li><a href="#featured">Featured</a></li>
    </ul>

    <div class="nav-icons">
      🔍 🛒
    </div>
  </nav>


  <!-- HERO -->

  <section class="hero" id="home">

    <div class="hero-text">

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
          Shop Products
        </a>

        <a href="#featured" class="btn btn-dark">
          Explore
        </a>
      </div>

    </div>

    <div class="hero-image">
      <img
        src="https://images.unsplash.com/photo-1581009146145-b5ef050c2e1e?auto=format&fit=crop&w=1000&q=90"
        alt="Fitness Athlete"
      >
    </div>

  </section>


  <!-- TRUST -->

  <div class="trust">

    <div class="trust-item">
      <h3>✓ PREMIUM PICKS</h3>
      <p>Selected fitness products</p>
    </div>

    <div class="trust-item">
      <h3>⚡ FAST DISCOVERY</h3>
      <p>Find what fits your goals</p>
    </div>

    <div class="trust-item">
      <h3>💪 FITNESS FOCUSED</h3>
      <p>Built for serious training</p>
    </div>

    <div class="trust-item">
      <h3>★ QUALITY BRANDS</h3>
      <p>Popular supplement brands</p>
    </div>

  </div>


  <!-- PRODUCTS -->

  <section class="products-section" id="products">

    <div class="section-header">

      <div>
        <small>RXHN COLLECTION</small>
        <h2>SHOP SUPPLEMENTS</h2>
      </div>

      <p>
        Explore popular protein, creatine and fitness nutrition products.
      </p>

    </div>


    <!-- SEARCH -->

    <div class="search-box">

      <input
        type="text"
        id="searchInput"
        placeholder="Search products..."
      >

      <button onclick="searchProducts()">
        SEARCH
      </button>

    </div>


    <div class="products" id="productGrid">


      <!-- PRODUCT 1 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            BESTSELLER
          </span>

          <img
            src="https://images.unsplash.com/photo-1593095948071-474c5cc2989d?auto=format&fit=crop&w=700&q=90"
            alt="Avvatar Alpha Whey Protein"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            AVVATAR
          </div>

          <h3>
            Alpha Whey Protein 1 KG
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹1,599
            </div>

            <a
              href="https://avataarindia.com/"
              target="_blank"
              class="buy"
            >
              VIEW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 2 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            VALUE PACK
          </span>

          <img
            src="https://images.unsplash.com/photo-1622484212850-eb596e0c5a32?auto=format&fit=crop&w=700&q=90"
            alt="Whey Protein"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            AVVATAR
          </div>

          <h3>
            Alpha Whey Protein 2 KG
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹3,113
            </div>

            <a
              href="https://avataarindia.com/"
              target="_blank"
              class="buy"
            >
              VIEW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 3 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            POWER
          </span>

          <img
            src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?auto=format&fit=crop&w=700&q=90"
            alt="Creatine Supplement"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            CREATINE
          </div>

          <h3>
            Creatine Monohydrate
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹899
            </div>

            <a href="#" class="buy">
              VIEW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 4 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            RECOVERY
          </span>

          <img
            src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?auto=format&fit=crop&w=700&q=90"
            alt="Protein Supplement"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            PROTEIN
          </div>

          <h3>
            High Protein Supplement
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹1,299
            </div>

            <a href="#" class="buy">
              VIEW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 5 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            PRE WORKOUT
          </span>

          <img
            src="https://images.unsplash.com/photo-1599058917212-d750089bc07e?auto=format&fit=crop&w=700&q=90"
            alt="Pre Workout"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            ENERGY
          </div>

          <h3>
            Advanced Pre Workout
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹1,099
            </div>

            <a href="#" class="buy">
              VIEW →
            </a>

          </div>

        </div>

      </article>


      <!-- PRODUCT 6 -->

      <article class="product-card product">

        <div class="product-image">

          <span class="badge-product">
            DAILY USE
          </span>

          <img
            src="https://images.unsplash.com/photo-1550345332-09e3ac987658?auto=format&fit=crop&w=700&q=90"
            alt="Fitness Nutrition"
          >

        </div>

        <div class="product-info">

          <div class="product-brand">
            FITNESS
          </div>

          <h3>
            Essential Fitness Nutrition
          </h3>

          <div class="rating">
            ★★★★★
          </div>

          <div class="price-row">

            <div class="price">
              ₹799
            </div>

            <a href="#" class="buy">
              VIEW →
            </a>

          </div>

        </div>

      </article>


    </div>

  </section>


  <!-- CTA -->

  <section class="cta" id="featured">

    <h2>
      TRAIN HARDER.<br>
      <span>CHOOSE BETTER.</span>
    </h2>

    <p>
      RXHN GETS brings your favourite fitness products together
      in one powerful place.
    </p>

    <br>

    <a href="#products" class="btn btn-primary">
      Explore Products →
    </a>

  </section>


  <!-- FOOTER -->

  <footer>

    <h2>
      RXHN <span>GETS</span>
    </h2>

    <p>
      Your destination for fitness products and supplement discovery.
    </p>

    <p style="margin-top:25px;">
      © 2026 RXHN GETS. All Rights Reserved.
    </p>

  </footer>


  <!-- JAVASCRIPT -->

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
      .addEventListener("keyup", searchProducts);

  </script>

</body>
</html>
