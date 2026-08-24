<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RXHN GETS — Supplement Store</title>
<style>
:root{
  --ink:#111827;
  --muted:#6b7280;
  --paper:#f5f7fb;
  --white:#ffffff;
  --blue:#2563eb;
  --blue2:#06b6d4;
  --lime:#c6ff00;
  --line:#e6eaf0;
  --shadow:0 18px 45px rgba(15,23,42,.10);
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;background:var(--paper);color:var(--ink);
  font-family:Arial,Helvetica,sans-serif;
}
a{text-decoration:none;color:inherit}
.topline{height:5px;background:linear-gradient(90deg,var(--blue),var(--blue2),var(--lime))}
header{background:#fff;border-bottom:1px solid var(--line);position:sticky;top:0;z-index:20}
nav{
  max-width:1320px;margin:auto;padding:18px 24px;
  display:flex;align-items:center;justify-content:space-between;gap:24px;
}
.logo{font-size:27px;font-weight:1000;letter-spacing:-1.4px}
.logo b{color:var(--blue)}
.logo span{background:var(--lime);padding:3px 7px;border-radius:7px;font-size:17px;margin-left:4px}
.links{display:flex;gap:28px;font-weight:800;color:#475569}
.links a:hover{color:var(--blue)}
.search{
  border:1px solid var(--line);background:#f8fafc;border-radius:14px;
  padding:13px 16px;width:270px;outline:none;font-size:14px;
}
.hero{
  max-width:1320px;margin:auto;padding:70px 24px 44px;
  display:grid;grid-template-columns:1.15fr .85fr;gap:40px;align-items:center;
}
.eyebrow{
  display:inline-flex;background:#e0f2fe;color:#0369a1;border-radius:999px;
  padding:9px 13px;font-size:11px;font-weight:1000;letter-spacing:1.2px;
}
h1{font-size:clamp(48px,7vw,92px);line-height:.9;letter-spacing:-5px;margin:18px 0}
h1 em{font-style:normal;color:var(--blue)}
.hero p{font-size:18px;line-height:1.7;color:var(--muted);max-width:650px}
.hero-card{
  min-height:360px;border-radius:32px;padding:34px;position:relative;overflow:hidden;
  background:linear-gradient(135deg,#111827,#1e40af 58%,#06b6d4);
  color:#fff;box-shadow:var(--shadow);
}
.hero-card:before{
  content:"";position:absolute;width:260px;height:260px;border-radius:50%;
  background:var(--lime);right:-80px;top:-75px;opacity:.95;
}
.hero-card:after{
  content:"RXHN";position:absolute;right:-18px;bottom:-30px;font-size:125px;
  font-weight:1000;color:rgba(255,255,255,.08);letter-spacing:-12px;
}
.hero-card small{position:relative;z-index:1;color:#a5f3fc;font-weight:900;letter-spacing:2px}
.hero-card h2{position:relative;z-index:1;font-size:42px;line-height:1;margin:18px 0;max-width:420px}
.hero-card p{position:relative;z-index:1;color:#cbd5e1;font-size:15px;max-width:380px}
.filters{
  max-width:1320px;margin:0 auto 30px;padding:0 24px;
  display:flex;gap:10px;flex-wrap:wrap;
}
.filter{
  border:1px solid var(--line);background:#fff;padding:12px 17px;border-radius:12px;
  font-weight:900;cursor:pointer;color:#475569;
}
.filter.active,.filter:hover{background:var(--ink);color:#fff;border-color:var(--ink)}
.section-head{
  max-width:1320px;margin:0 auto;padding:0 24px 22px;
  display:flex;justify-content:space-between;align-items:end;
}
.section-head h2{margin:0;font-size:34px;letter-spacing:-1.5px}
.section-head p{margin:7px 0 0;color:var(--muted)}
.count{font-weight:900;color:var(--blue)}
.grid{
  max-width:1320px;margin:auto;padding:0 24px 70px;
  display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:18px;
}
.card{
  background:#fff;border:1px solid var(--line);border-radius:24px;overflow:hidden;
  box-shadow:0 6px 22px rgba(15,23,42,.04);transition:.25s ease;
  display:flex;flex-direction:column;
}
.card:hover{transform:translateY(-7px);box-shadow:var(--shadow)}
.image-wrap{
  height:270px;background:#f7f8fa;display:flex;align-items:center;justify-content:center;
  position:relative;padding:22px;overflow:hidden;
}
.image-wrap:before{
  content:"";position:absolute;width:160px;height:160px;border-radius:50%;
  background:linear-gradient(135deg,#dbeafe,#ecfeff);z-index:0;
}
.image-wrap img{width:100%;height:100%;object-fit:contain;position:relative;z-index:1;mix-blend-mode:multiply}
.badge{
  position:absolute;top:14px;left:14px;z-index:3;background:var(--lime);color:#111827;
  padding:7px 10px;border-radius:8px;font-size:10px;font-weight:1000;letter-spacing:.8px;
}
.info{padding:18px;display:flex;flex-direction:column;flex:1}
.brand{font-size:11px;letter-spacing:1.8px;font-weight:1000;color:var(--blue);margin-bottom:8px}
.info h3{margin:0;font-size:18px;line-height:1.3;min-height:48px}
.meta{font-size:13px;color:var(--muted);margin:8px 0 15px}
.bottom{margin-top:auto;display:flex;align-items:center;justify-content:space-between;gap:10px}
.price{font-size:21px;font-weight:1000}
.view{
  background:var(--blue);color:#fff;padding:11px 13px;border-radius:10px;
  font-size:11px;font-weight:1000;letter-spacing:.5px;
}
.view:hover{background:#1d4ed8}
.empty{grid-column:1/-1;background:#fff;border:1px dashed #cbd5e1;padding:50px;text-align:center;border-radius:20px;color:var(--muted)}
footer{background:#111827;color:#94a3b8;padding:32px 24px;text-align:center}
@media(max-width:1050px){.grid{grid-template-columns:repeat(3,1fr)}}
@media(max-width:820px){
  .hero{grid-template-columns:1fr}.links{display:none}.grid{grid-template-columns:repeat(2,1fr)}
  .search{width:180px}h1{letter-spacing:-3px}
}
@media(max-width:520px){
  nav{padding:15px}.search{display:none}.hero{padding:45px 18px 30px}.filters,.section-head,.grid{padding-left:18px;padding-right:18px}
  .grid{grid-template-columns:1fr}.image-wrap{height:300px}.hero-card{min-height:290px}.hero-card h2{font-size:34px}
}
</style>
</head>
<body>

<div class="topline"></div>

<header>
  <nav>
    <a href="#" class="logo">RXHN<b>GETS</b><span>+</span></a>
    <div class="links">
      <a href="#">Home</a>
      <a href="#shop">Shop</a>
      <a href="#shop">Popular</a>
    </div>
    <input id="search" class="search" type="search" placeholder="Search supplements...">
  </nav>
</header>

<section class="hero">
  <div>
    <div class="eyebrow">REAL PRODUCT PACKAGING • NO STOCK GYM PHOTOS</div>
    <h1>YOUR NEXT<br><em>STACK.</em></h1>
    <p>A redesigned RXHN GETS theme with individual supplement product photos. No repeated fallback image is used — if an external host blocks an image, the card shows an unavailable state instead of duplicating another product.</p>
  </div>
  <div class="hero-card">
    <small>RXHN GETS / 2026</small>
    <h2>SUPPLEMENTS THAT LOOK AS GOOD AS YOUR SETUP.</h2>
    <p>Fresh electric-blue theme. Cleaner cards. Actual tubs, pouches and supplement packaging.</p>
  </div>
</section>

<section id="shop">
  <div class="filters">
    <button class="filter active" data-filter="All">All</button>
    <button class="filter" data-filter="Whey">Whey</button>
    <button class="filter" data-filter="Isolate">Isolate</button>
    <button class="filter" data-filter="Creatine">Creatine</button>
    <button class="filter" data-filter="Premium">Premium</button>
  </div>

  <div class="section-head">
    <div>
      <h2>SUPPLEMENT DROP</h2>
      <p><span id="count" class="count"></span> different products in this collection</p>
    </div>
  </div>

  <main id="grid" class="grid"></main>
</section>

<footer>© 2026 RXHN GETS • PRODUCT SHOWCASE</footer>

<script>
const products = [
  {
    brand:"AVVATAR", name:"Alpha Whey Protein", meta:"Belgian Chocolate • 1 KG", price:"₹2,669", tag:"WHEY", cat:"Whey",
    img:"https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg",
    link:"https://www.avvatarindia.com/"
  },
  {
    brand:"RULE 1", name:"R1 Whey Blend", meta:"Chocolate Fudge • 5.1 LB", price:"₹6,499", tag:"ATHLETE PICK", cat:"Whey",
    img:"https://dms.mydukaan.io/original/jpeg/media/14b0c5d0-35e9-4cfc-ad4a-1d20316386a9.jpg",
    link:"https://ruleoneproteins.com/"
  },
  {
    brand:"AVVATAR", name:"Fuel Whey", meta:"Belgian Chocolate • 2 KG", price:"₹4,699", tag:"VALUE", cat:"Whey",
    img:"https://nutriride.com/cdn/shop/files/Avvatar_Fuel_whey_-_belgian_chocolate_2kg_webp.jpg?v=1755155910",
    link:"https://www.avvatarindia.com/"
  },
  {
    brand:"BIGMUSCLES", name:"Premium Gold Whey", meta:"Belgian Chocolate • 2 KG", price:"₹4,399", tag:"MUSCLE GAIN", cat:"Whey",
    img:"https://supplemust.in/cdn/shop/files/shopping_0b729cf7-7f5a-456d-93d3-c7916cb147cd.webp?v=1723549606",
    link:"https://www.bigmusclesnutrition.com/"
  },
  {
    brand:"OPTIMUM NUTRITION", name:"Gold Standard 100% Whey", meta:"Double Rich Chocolate", price:"₹5,079", tag:"GLOBAL", cat:"Premium",
    img:"https://m.media-amazon.com/images/I/81W7G4nP5nL._SL1500_.jpg",
    link:"https://www.optimumnutrition.co.in/"
  },
  {
    brand:"DYMATIZE", name:"ISO100 Hydrolyzed", meta:"Gourmet Chocolate", price:"₹7,499", tag:"ISOLATE", cat:"Isolate",
    img:"https://m.media-amazon.com/images/I/71ZXK7k1Q5L._SL1500_.jpg",
    link:"https://www.dymatize.com/"
  },
  {
    brand:"MYPROTEIN", name:"Impact Whey Protein", meta:"Chocolate Smooth", price:"₹2,599", tag:"IMPACT", cat:"Whey",
    img:"https://m.media-amazon.com/images/I/71d5D6lBfFL._SL1500_.jpg",
    link:"https://www.myprotein.co.in/"
  },
  {
    brand:"LABRADA", name:"Lean Body Protein", meta:"Vanilla • Premium Formula", price:"₹4,299", tag:"LEAN MUSCLE", cat:"Premium",
    img:"https://m.media-amazon.com/images/I/71tV4QfNQKL._SL1500_.jpg",
    link:"https://www.labrada.com/"
  },
  {
    brand:"AS-IT-IS", name:"ATOM Whey Protein", meta:"Choco Hazel Fusion", price:"₹3,269", tag:"INDIAN BRAND", cat:"Whey",
    img:"https://m.media-amazon.com/images/I/71ZVw9f1s-L._SL1500_.jpg",
    link:"https://asitisnutrition.com/"
  },
  {
    brand:"MUSCLETECH", name:"Nitro-Tech Whey Protein", meta:"Milk Chocolate • 1.81 KG", price:"₹7,999", tag:"30G PROTEIN", cat:"Premium",
    img:"https://media.drnutrition.com/media/ArVycel93721Z9ulgXWi4ftWxB3C1CoIIKJX28S3.jpg",
    link:"https://www.muscletech.in/"
  },
  {
    brand:"MUSCLEBLAZE", name:"Creatine Monohydrate", meta:"Unflavoured • 400 G", price:"₹1,199", tag:"CREATINE", cat:"Creatine",
    img:"https://cdn.shopify.com/s/files/1/0735/3794/5897/files/612rGWh-JTL._SL1500.jpg?v=1742606471",
    link:"https://www.muscleblaze.com/"
  },
  {
    brand:"NAKPRO", name:"Impact Whey Protein", meta:"Chocolate • 1 KG", price:"₹2,499", tag:"BUDGET PICK", cat:"Whey",
    img:"https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTllXLlDWFLkI47OmssZN0lam4g3PEDO8YIRKjWcWwxe-p_TB5G7GVBtR4_MS2j51-nU03SaEr8-tPeiQ-1XLSxX2OKOjGPv5drFssFFUImV2GzzjidSALawg",
    link:"https://nakpro.com/"
  },
  {
    brand:"AVVATAR", name:"Alpha Whey Protein", meta:"Cold Coffee • 1 KG", price:"₹2,669", tag:"COLD COFFEE", cat:"Whey",
    img:"https://www.avvatarindia.com/cdn/shop/files/alpha-whey-1kg_belgian-chocolate_1_1800x1800.jpg?v=1689723456",
    link:"https://www.avvatarindia.com/"
  },
  {
    brand:"BIGMUSCLES", name:"Gold Whey Isolate", meta:"Rich Chocolate • 2 KG", price:"₹5,999", tag:"ISOLATE", cat:"Isolate",
    img:"https://m.media-amazon.com/images/I/71rF2mA9o1L._SL1500_.jpg",
    link:"https://www.bigmusclesnutrition.com/"
  }
];

const grid = document.getElementById("grid");
const search = document.getElementById("search");
const count = document.getElementById("count");
let filter = "All";

function render(){
  const term = search.value.toLowerCase().trim();
  const shown = products.filter(p => {
    const matchFilter = filter === "All" || p.cat === filter;
    const text = `${p.brand} ${p.name} ${p.meta} ${p.tag}`.toLowerCase();
    return matchFilter && text.includes(term);
  });

  count.textContent = shown.length;

  grid.innerHTML = shown.length ? shown.map(p => `
    <article class="card">
      <div class="image-wrap">
        <span class="badge">${p.tag}</span>
        <img src="${p.img}" alt="${p.brand} ${p.name}" loading="lazy"
          onerror="this.style.display='none';this.parentElement.classList.add('broken');">
      </div>
      <div class="info">
        <div class="brand">${p.brand}</div>
        <h3>${p.name}</h3>
        <div class="meta">${p.meta}</div>
        <div class="bottom">
          <div class="price">${p.price}</div>
          <a class="view" href="${p.link}" target="_blank" rel="noopener">VIEW →</a>
        </div>
      </div>
    </article>
  `).join("") : `<div class="empty">No product found.</div>`;

  document.querySelectorAll(".broken").forEach(el => {
    el.innerHTML += `<div style="position:absolute;z-index:2;text-align:center;font-weight:900;color:#64748b;font-size:13px;padding:20px">IMAGE HOST UNAVAILABLE<br><span style="font-weight:700;font-size:11px">No repeated fallback used</span></div>`;
  });
}

document.querySelectorAll(".filter").forEach(btn => {
  btn.addEventListener("click", () => {
    document.querySelectorAll(".filter").forEach(x => x.classList.remove("active"));
    btn.classList.add("active");
    filter = btn.dataset.filter;
    render();
  });
});
search.addEventListener("input", render);
render();
</script>
</body>
</html>
