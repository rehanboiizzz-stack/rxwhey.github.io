from pathlib import Path

products = [
    ("AVVATAR","Alpha Whey Protein","Belgian Chocolate • 1 KG","₹2,669","WHEY","Whey","https://cdn.zeptonow.com/production/ik-seo/cms/product_variant/89f731fa-0d67-41f0-a949-cd33ca67db0c/Avvatar-Whey-Protein-Belgian-Chocolate.jpeg","https://www.avvatarindia.com/"),
    ("RULE 1","R1 Whey Blend","Chocolate Fudge • 5.1 LB","₹6,499","TRENDING","Whey","https://dms.mydukaan.io/original/jpeg/media/14b0c5d0-35e9-4cfc-ad4a-1d20316386a9.jpg","https://ruleoneproteins.com/"),
    ("AVVATAR","Fuel Whey","Belgian Chocolate • 2 KG","₹4,699","VALUE","Whey","https://nutriride.com/cdn/shop/files/Avvatar_Fuel_whey_-_belgian_chocolate_2kg_webp.jpg?v=1755155910","https://www.avvatarindia.com/"),
    ("BIGMUSCLES","Premium Gold Whey","Belgian Chocolate • 2 KG","₹4,399","MUSCLE GAIN","Whey","https://supplemust.in/cdn/shop/files/shopping_0b729cf7-7f5a-456d-93d3-c7916cb147cd.webp?v=1723549606","https://www.bigmusclesnutrition.com/"),
    ("OPTIMUM NUTRITION","Gold Standard 100% Whey","Double Rich Chocolate","₹5,079","GLOBAL","Premium","https://m.media-amazon.com/images/I/81W7G4nP5nL._SL1500_.jpg","https://www.optimumnutrition.co.in/"),
    ("DYMATIZE","ISO100 Hydrolyzed","Gourmet Chocolate","₹7,499","ISOLATE","Isolate","https://m.media-amazon.com/images/I/71ZXK7k1Q5L._SL1500_.jpg","https://www.dymatize.com/"),
    ("MYPROTEIN","Impact Whey Protein","Chocolate Smooth","₹2,599","IMPACT","Whey","https://m.media-amazon.com/images/I/71d5D6lBfFL._SL1500_.jpg","https://www.myprotein.co.in/"),
    ("LABRADA","Lean Body Protein","Vanilla • Premium Formula","₹4,299","LEAN","Premium","https://m.media-amazon.com/images/I/71tV4QfNQKL._SL1500_.jpg","https://www.labrada.com/"),
    ("AS-IT-IS","ATOM Whey Protein","Choco Hazel Fusion","₹3,269","INDIAN","Whey","https://m.media-amazon.com/images/I/71ZVw9f1s-L._SL1500_.jpg","https://asitisnutrition.com/"),
    ("MUSCLETECH","Nitro-Tech Whey Protein","Milk Chocolate • 1.81 KG","₹7,999","30G PROTEIN","Premium","https://media.drnutrition.com/media/ArVycel93721Z9ulgXWi4ftWxB3C1CoIIKJX28S3.jpg","https://www.muscletech.in/"),
    ("MUSCLEBLAZE","Creatine Monohydrate","Unflavoured • 400 G","₹1,199","CREATINE","Creatine","https://cdn.shopify.com/s/files/1/0735/3794/5897/files/612rGWh-JTL._SL1500.jpg?v=1742606471","https://www.muscleblaze.com/"),
    ("NAKPRO","Impact Whey Protein","Chocolate • 1 KG","₹2,499","BUDGET","Whey","https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTllXLlDWFLkI47OmssZN0lam4g3PEDO8YIRKjWcWwxe-p_TB5G7GVBtR4_MS2j51-nU03SaEr8-tPeiQ-1XLSxX2OKOjGPv5drFssFFUImV2GzzjidSALawg","https://nakpro.com/"),
    ("MUSCLEBLAZE","Biozyme Performance Whey","Rich Chocolate","₹4,299","TOP RATED","Premium","https://img10.hkrtcdn.com/39079/prd_3907869-MuscleBlaze-Biozyme-Performance-Whey-1.1-lb-Rich-Chocolate_o.jpg","https://www.muscleblaze.com/"),
    ("BIGMUSCLES","Gold Whey Isolate","Rich Chocolate • 2 KG","₹5,999","ISOLATE","Isolate","https://m.media-amazon.com/images/I/71rF2mA9o1L._SL1500_.jpg","https://www.bigmusclesnutrition.com/"),
    ("AVVATAR","Alpha Whey","Premium Indian Whey","₹3,113","BESTSELLER","Whey","https://www.avvatarindia.com/cdn/shop/files/alpha-whey-1kg_belgian-chocolate_1_1800x1800.jpg?v=1689723456","https://www.avvatarindia.com/"),
    ("RULE 1","R1 Protein","Premium Protein Formula","₹6,199","ELITE","Premium","https://supplementking.pk/wp-content/uploads/2023/07/Picsart_23-05-19_15-27-19-387.webp","https://ruleoneproteins.com/"),
    ("NAKPRO","Perform Whey Protein","Chocolate • 1 KG","₹2,299","VALUE","Whey","https://nutristar.in/cdn/shop/files/AJPA_1_2284241a-220f-4b51-a989-c29acbd04341.jpg?v=1761670579","https://nakpro.com/"),
    ("MUSCLEBLAZE","CreaPRO Creatine","Creapure® • Unflavoured","₹699","CREAPURE","Creatine","https://cdn.shopify.com/s/files/1/0735/3794/5897/files/612rGWh-JTL._SL1500.jpg?v=1742606471","https://www.muscleblaze.com/"),
    ("DYMATIZE","Elite 100% Whey","Rich Chocolate","₹6,999","ELITE","Premium","https://m.media-amazon.com/images/I/71ZXK7k1Q5L._SL1500_.jpg","https://www.dymatize.com/"),
    ("MYPROTEIN","Impact Whey","Premium Chocolate Protein","₹2,999","FAVOURITE","Whey","https://m.media-amazon.com/images/I/71d5D6lBfFL._SL1500_.jpg","https://www.myprotein.co.in/")
]

cards = []
for i,p in enumerate(products):
    brand,name,meta,price,tag,cat,img,link = p
    cards.append(f'''
    <article class="product-card reveal" data-category="{cat}" data-search="{brand} {name} {meta} {tag}">
      <div class="product-visual">
        <span class="product-badge">{tag}</span>
        <button class="heart" aria-label="Add to wishlist" data-name="{name}">♡</button>
        <div class="orb orb-a"></div><div class="orb orb-b"></div>
        <img src="{img}" alt="{brand} {name}" loading="lazy">
      </div>
      <div class="product-body">
        <div class="brand">{brand}</div>
        <h3>{name}</h3>
        <p>{meta}</p>
        <div class="rating"><span>★★★★★</span><small> 4.{5 + (i%5)} / 5</small></div>
        <div class="product-bottom">
          <div><strong>{price}</strong><del>₹{int(''.join(filter(str.isdigit,price))) + 600:,}</del></div>
          <div class="actions">
            <button class="quick-btn" data-id="{i}">QUICK VIEW</button>
            <a href="{link}" target="_blank" rel="noopener" class="add-btn">ADD +</a>
          </div>
        </div>
      </div>
    </article>''')

html = f'''<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>RXHN GETS — Gen-Z Supplement Store</title>
<meta name="theme-color" content="#09090f">
<style>
/* =========================================================
   RXHN GETS — SINGLE FILE GEN-Z 3D SUPPLEMENT STORE
   HTML + CSS + JAVASCRIPT ONLY
   ========================================================= */
@import url('https://fonts.googleapis.com/css2?family=Archivo+Black&family=DM+Mono:wght@400;500&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap');
:root {{
--bg:#09090f;--bg2:#101018;--card:#13131d;--card2:#191925;
--text:#f8f7ff;--muted:#9d9cab;--line:rgba(255,255,255,.09);
--acid:#d7ff00;--violet:#875cff;--cyan:#22e7ff;--pink:#ff5ccf;
--orange:#ff9d2e;--shadow:0 30px 90px rgba(0,0,0,.55);
}}
*{{box-sizing:border-box}}html{{scroll-behavior:smooth}}body{{margin:0;background:var(--bg);color:var(--text);font-family:"Plus Jakarta Sans",sans-serif;overflow-x:hidden}}button,input{{font:inherit}}button{{cursor:pointer}}a{{color:inherit;text-decoration:none}}
::selection{{background:var(--acid);color:#050505}}.noise{{position:fixed;inset:0;pointer-events:none;z-index:9999;opacity:.035;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.8'/%3E%3C/svg%3E")}}
#progress{{position:fixed;top:0;left:0;height:3px;background:linear-gradient(90deg,var(--acid),var(--cyan),var(--pink));z-index:1000;width:0}}
.cursor-glow{{position:fixed;width:420px;height:420px;border-radius:50%;pointer-events:none;z-index:-1;filter:blur(70px);background:rgba(135,92,255,.13);transform:translate(-50%,-50%)}}
.announcement{{height:35px;display:flex;align-items:center;justify-content:center;background:var(--acid);color:#080808;font-size:11px;font-weight:900;letter-spacing:2px;gap:12px}}
.announcement .dot{{width:7px;height:7px;border-radius:50%;background:#080808;box-shadow:0 0 0 5px rgba(0,0,0,.08)}}
.nav-wrap{{position:sticky;top:0;z-index:100;background:rgba(9,9,15,.72);backdrop-filter:blur(20px);border-bottom:1px solid var(--line)}}
nav{{max-width:1440px;margin:auto;padding:18px 30px;display:flex;align-items:center;gap:26px}}
.logo{{font-family:"Archivo Black";font-size:27px;letter-spacing:-2px;white-space:nowrap}}.logo span{{color:var(--acid)}}.logo i{{font-family:"DM Mono";font-style:normal;font-size:8px;letter-spacing:1px;background:var(--acid);color:#111;padding:4px 6px;border-radius:4px;vertical-align:middle;margin-left:4px}}
.nav-links{{display:flex;gap:24px;margin:auto}}.nav-links a{{font-size:12px;font-weight:800;color:#aaaab5;position:relative}}.nav-links a:after{{content:"";position:absolute;bottom:-8px;left:0;width:0;height:2px;background:var(--acid);transition:.3s}}.nav-links a:hover{{color:white}}.nav-links a:hover:after{{width:100%}}
.search-box{{width:250px;height:44px;border:1px solid var(--line);background:#12121b;border-radius:14px;display:flex;align-items:center;padding:0 13px;gap:10px}}.search-box input{{width:100%;border:0;outline:0;background:transparent;color:white;font-size:12px}}.search-box span{{color:var(--muted)}}.cart{{height:44px;min-width:44px;border-radius:14px;background:var(--text);color:#0b0b10;display:grid;place-items:center;font-weight:900;position:relative}}.cart b{{position:absolute;right:-7px;top:-7px;background:var(--pink);color:white;width:19px;height:19px;border-radius:50%;font-size:10px;display:grid;place-items:center}}
.hero{{max-width:1440px;margin:auto;min-height:720px;padding:60px 30px;display:grid;grid-template-columns:1.1fr .9fr;align-items:center;gap:40px;position:relative}}.hero-copy{{position:relative;z-index:2}}.eyebrow{{font-family:"DM Mono";font-size:11px;letter-spacing:2px;color:var(--acid);display:flex;gap:10px;align-items:center}}.eyebrow:before{{content:"";width:28px;height:1px;background:var(--acid)}}.hero h1{{font-family:"Archivo Black";font-size:clamp(64px,9vw,145px);line-height:.82;letter-spacing:-8px;margin:22px 0}}.hero h1 .stroke{{color:transparent;-webkit-text-stroke:2px var(--text)}}.hero h1 .acid{{color:var(--acid);text-shadow:8px 8px 0 rgba(215,255,0,.1)}}.hero p{{max-width:560px;color:var(--muted);line-height:1.8;font-size:15px}}.hero-buttons{{display:flex;gap:12px;margin-top:32px}}.primary,.secondary{{padding:16px 22px;border-radius:14px;font-size:12px;font-weight:900;border:0;transition:.25s}}.primary{{background:var(--acid);color:#080808;box-shadow:0 12px 30px rgba(215,255,0,.2)}}.primary:hover{{transform:translateY(-3px) scale(1.02)}}.secondary{{background:rgba(255,255,255,.04);color:white;border:1px solid var(--line)}}.secondary:hover{{background:rgba(255,255,255,.09)}}
.stats{{display:flex;gap:30px;margin-top:55px}}.stat{{border-left:1px solid var(--line);padding-left:18px}}.stat strong{{display:block;font-size:22px}}.stat small{{color:var(--muted);font-size:10px;text-transform:uppercase;letter-spacing:1px}}
.hero-art{{position:relative;height:600px;display:grid;place-items:center;perspective:1000px}}.hero-ring{{position:absolute;border:1px solid rgba(255,255,255,.12);border-radius:50%;width:540px;height:540px;animation:spin 18s linear infinite}}.hero-ring:after{{content:"RXHN • STACK MODE • 2026 • RXHN • STACK MODE • 2026 •";position:absolute;inset:0;display:grid;place-items:center;color:rgba(255,255,255,.1);font-family:"DM Mono";font-size:10px;letter-spacing:8px;text-align:center;line-height:45px;transform:rotate(30deg)}}@keyframes spin{{to{{transform:rotate(360deg)}}}}
.hero-product{{position:relative;z-index:2;width:420px;max-width:90%;height:500px;display:grid;place-items:center;transform-style:preserve-3d;animation:float 5s ease-in-out infinite}}.hero-product img{{width:100%;height:100%;object-fit:contain;filter:drop-shadow(0 45px 35px rgba(0,0,0,.5));mix-blend-mode:multiply;background:#efefef;border-radius:38px;padding:20px}}@keyframes float{{50%{{transform:translateY(-18px) rotateY(7deg)}}}}
.float-chip{{position:absolute;z-index:5;padding:12px 15px;background:rgba(21,21,30,.78);backdrop-filter:blur(12px);border:1px solid var(--line);border-radius:14px;font-size:11px;font-weight:800;box-shadow:var(--shadow)}}.chip1{{left:-20px;top:100px}}.chip2{{right:-25px;bottom:100px}}.chip3{{right:0;top:55px;color:var(--acid)}}
.marquee{{overflow:hidden;border-top:1px solid var(--line);border-bottom:1px solid var(--line);padding:18px 0;background:#0d0d14}}.marquee-track{{display:flex;width:max-content;animation:marquee 22s linear infinite}}.marquee-track span{{font-family:"Archivo Black";font-size:24px;letter-spacing:-1px;white-space:nowrap;margin-right:40px;color:#3d3d49}}.marquee-track b{{color:var(--acid);margin-left:40px}}@keyframes marquee{{to{{transform:translateX(-50%)}}}}
.section{{max-width:1440px;margin:auto;padding:110px 30px}}.section-top{{display:flex;align-items:end;justify-content:space-between;gap:30px;margin-bottom:35px}}.section-label{{font-family:"DM Mono";font-size:10px;letter-spacing:2px;color:var(--acid)}}.section-title{{font-family:"Archivo Black";font-size:clamp(36px,5vw,68px);letter-spacing:-4px;margin:8px 0 0;line-height:.9}}.section-text{{max-width:380px;color:var(--muted);font-size:13px;line-height:1.7}}
.category-grid{{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}}.cat-card{{min-height:230px;border-radius:24px;border:1px solid var(--line);padding:24px;position:relative;overflow:hidden;background:linear-gradient(145deg,#15151f,#0e0e14);transition:.35s}}.cat-card:hover{{transform:translateY(-8px);border-color:rgba(215,255,0,.5)}}.cat-card:nth-child(2){{background:linear-gradient(145deg,#1a1425,#11101a)}}.cat-card:nth-child(3){{background:linear-gradient(145deg,#102225,#0d1516)}}.cat-card:nth-child(4){{background:linear-gradient(145deg,#27170f,#15100d)}}.cat-card h3{{position:absolute;bottom:22px;left:24px;margin:0;font-family:"Archivo Black";font-size:25px;letter-spacing:-1px}}.cat-card .cat-num{{font-family:"DM Mono";font-size:10px;color:var(--muted)}}.cat-card .big-icon{{position:absolute;right:-10px;bottom:-20px;font-size:150px;opacity:.08;transform:rotate(-15deg)}}.filter-bar{{display:flex;gap:9px;flex-wrap:wrap;margin-bottom:25px}}.filter{{border:1px solid var(--line);background:#12121a;color:#a5a5b0;padding:11px 15px;border-radius:999px;font-size:11px;font-weight:900;transition:.25s}}.filter:hover,.filter.active{{background:var(--acid);color:#090909;border-color:var(--acid)}}.product-count{{margin-left:auto;font-family:"DM Mono";font-size:10px;color:var(--muted);padding:12px}}
.product-grid{{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:16px}}.product-card{{background:linear-gradient(145deg,#15151f,#101018);border:1px solid var(--line);border-radius:24px;overflow:hidden;transition:.35s;transform-style:preserve-3d}}.product-card:hover{{transform:translateY(-10px);box-shadow:var(--shadow);border-color:rgba(255,255,255,.2)}}.product-visual{{height:290px;background:#ececf0;position:relative;display:grid;place-items:center;overflow:hidden}}.product-visual img{{width:100%;height:100%;object-fit:contain;padding:25px;position:relative;z-index:2;mix-blend-mode:multiply;transition:.45s;filter:drop-shadow(0 20px 16px rgba(0,0,0,.2))}}.product-card:hover .product-visual img{{transform:scale(1.08) rotate(-2deg)}}.product-badge{{position:absolute;top:13px;left:13px;z-index:4;background:#111;color:var(--acid);padding:7px 9px;border-radius:8px;font-family:"DM Mono";font-size:9px;letter-spacing:.8px}}.heart{{position:absolute;top:12px;right:12px;z-index:5;width:38px;height:38px;border:0;border-radius:50%;background:white;color:#111;font-size:20px}}.heart.active{{background:var(--pink);color:white}}.orb{{position:absolute;border-radius:50%;filter:blur(1px);opacity:.65}}.orb-a{{width:150px;height:150px;background:#d7ff00;top:-70px;right:-50px}}.orb-b{{width:120px;height:120px;background:#22e7ff;bottom:-70px;left:-40px}}.product-body{{padding:19px}}.brand{{font-family:"DM Mono";font-size:9px;letter-spacing:1.5px;color:var(--acid);margin-bottom:8px}}.product-body h3{{margin:0;font-size:17px;line-height:1.25;min-height:42px}}.product-body p{{color:var(--muted);font-size:11px;margin:7px 0 11px;min-height:16px}}.rating{{font-size:11px;margin-bottom:17px}}.rating span{{color:var(--acid);letter-spacing:1px}}.rating small{{color:var(--muted)}}.product-bottom{{display:flex;align-items:end;justify-content:space-between;gap:10px}}.product-bottom strong{{font-size:20px;display:block}}.product-bottom del{{font-size:9px;color:#676775}}.actions{{display:flex;gap:7px}}.quick-btn,.add-btn{{border:1px solid var(--line);background:#1d1d28;color:white;padding:10px 8px;border-radius:10px;font-size:9px;font-weight:900}}.add-btn{{background:var(--acid);color:#111;border-color:var(--acid)}}
.stack-banner{{max-width:1440px;margin:0 auto;padding:0 30px}}.stack-inner{{min-height:330px;border-radius:30px;overflow:hidden;position:relative;background:linear-gradient(110deg,#d7ff00,#9dff30 45%,#0de4ff);color:#080808;padding:50px;display:flex;align-items:end}}.stack-inner:before{{content:"BUILD";position:absolute;right:-20px;top:-55px;font-family:"Archivo Black";font-size:230px;letter-spacing:-20px;color:rgba(0,0,0,.07)}}.stack-inner h2{{font-family:"Archivo Black";font-size:clamp(50px,8vw,110px);line-height:.8;letter-spacing:-6px;margin:0;position:relative;z-index:2}}.stack-inner p{{max-width:430px;font-weight:700;line-height:1.7;position:relative;z-index:2}}.stack-btn{{position:absolute;right:50px;bottom:50px;background:#09090f;color:white;padding:18px 22px;border-radius:14px;font-size:11px;font-weight:900;z-index:3}}
.bento{{display:grid;grid-template-columns:1.2fr .8fr .8fr;grid-auto-rows:230px;gap:15px}}.bento-card{{border:1px solid var(--line);border-radius:25px;padding:25px;background:#12121b;position:relative;overflow:hidden}}.bento-card:first-child{{grid-row:span 2;background:linear-gradient(145deg,#171427,#11111a)}}.bento-card h3{{font-family:"Archivo Black";font-size:25px;letter-spacing:-1px;margin:8px 0}}.bento-card p{{font-size:12px;color:var(--muted);max-width:300px;line-height:1.7}}.bento-card .num{{font-family:"DM Mono";color:var(--acid);font-size:11px}}.bento-card .emoji{{position:absolute;right:20px;bottom:-20px;font-size:130px;filter:grayscale(.1)}}.bento-card:nth-child(2){{background:linear-gradient(145deg,#10292a,#10161a)}}.bento-card:nth-child(3){{background:linear-gradient(145deg,#29131e,#161016)}}.bento-card:nth-child(4){{background:linear-gradient(145deg,#23180d,#17120e)}}.newsletter{{text-align:center;padding:100px 20px;border-top:1px solid var(--line);background:radial-gradient(circle at center,rgba(135,92,255,.12),transparent 40%)}}.newsletter h2{{font-family:"Archivo Black";font-size:clamp(42px,7vw,90px);line-height:.85;letter-spacing:-6px;margin:15px 0}}.newsletter p{{color:var(--muted);font-size:13px}}.email-box{{display:flex;width:min(520px,90%);margin:30px auto 0;padding:7px;border:1px solid var(--line);background:#12121b;border-radius:16px}}.email-box input{{flex:1;background:transparent;border:0;outline:0;color:white;padding:10px 14px}}.email-box button{{background:var(--acid);border:0;border-radius:11px;padding:13px 18px;font-size:11px;font-weight:900}}
footer{{max-width:1440px;margin:auto;padding:45px 30px 80px;display:flex;justify-content:space-between;gap:20px;border-top:1px solid var(--line);color:#777786;font-size:11px}}footer .logo{{color:white}}.modal{{position:fixed;inset:0;background:rgba(0,0,0,.72);backdrop-filter:blur(12px);display:none;align-items:center;justify-content:center;z-index:300;padding:20px}}.modal.open{{display:flex}}.modal-box{{width:min(900px,100%);background:#13131d;border:1px solid var(--line);border-radius:30px;display:grid;grid-template-columns:1fr 1fr;overflow:hidden;position:relative}}.modal-img{{background:#eee;min-height:450px;padding:35px;display:grid;place-items:center}}.modal-img img{{width:100%;height:100%;object-fit:contain;mix-blend-mode:multiply}}.modal-info{{padding:45px}}.close{{position:absolute;right:16px;top:16px;width:40px;height:40px;border:1px solid var(--line);background:#1d1d27;color:white;border-radius:50%;z-index:5}}.modal-info h2{{font-family:"Archivo Black";font-size:42px;letter-spacing:-2px;line-height:1;margin:15px 0}}.modal-info p{{color:var(--muted);font-size:13px;line-height:1.8}}.modal-price{{font-size:36px;font-weight:900;margin:25px 0}}.modal-buy{{display:inline-block;background:var(--acid);color:#111;padding:16px 20px;border-radius:13px;font-size:12px;font-weight:900}}
.toast{{position:fixed;bottom:25px;left:50%;transform:translate(-50%,140px);background:white;color:#111;padding:14px 18px;border-radius:13px;font-size:12px;font-weight:900;box-shadow:var(--shadow);z-index:500;transition:.4s}}.toast.show{{transform:translate(-50%,0)}}.reveal{{opacity:0;transform:translateY(25px)}}.reveal.show{{opacity:1;transform:none;transition:.7s cubic-bezier(.2,.8,.2,1)}}
@media(max-width:1050px){{.product-grid{{grid-template-columns:repeat(3,1fr)}}.category-grid{{grid-template-columns:repeat(2,1fr)}}.hero{{grid-template-columns:1fr}}.hero-art{{height:480px}}.bento{{grid-template-columns:1fr 1fr}}.nav-links{{display:none}}}}
@media(max-width:700px){{nav{{padding:14px 16px}}.announcement{{font-size:8px}}.search-box{{display:none}}.hero,.section{{padding-left:18px;padding-right:18px}}.hero{{min-height:auto;padding-top:55px}}.hero h1{{letter-spacing:-4px}}.stats{{gap:15px}}.hero-art{{height:380px}}.hero-product{{height:340px}}.hero-ring{{width:350px;height:350px}}.product-grid{{grid-template-columns:1fr 1fr;gap:10px}}.product-visual{{height:200px}}.product-body{{padding:13px}}.product-body h3{{font-size:14px}}.quick-btn{{display:none}}.product-bottom strong{{font-size:16px}}.category-grid{{grid-template-columns:1fr 1fr}}.cat-card{{min-height:170px}}.section-top{{display:block}}.section-text{{margin-top:20px}}.bento{{grid-template-columns:1fr;grid-auto-rows:200px}}.bento-card:first-child{{grid-row:span 1}}.modal-box{{grid-template-columns:1fr;max-height:90vh;overflow:auto}}.modal-img{{min-height:300px}}.modal-info{{padding:28px}}.stack-inner{{padding:30px;min-height:300px}}.stack-btn{{right:30px;bottom:30px}}footer{{flex-direction:column}}}}
</style>
</head>
<body>
<div id="progress"></div><div class="noise"></div><div class="cursor-glow"></div>
<div class="announcement"><span class="dot"></span> NEW DROP LIVE — BUILD YOUR NEXT STACK <span>⚡</span></div>
<div class="nav-wrap"><nav>
<a href="#" class="logo">RXHN<span>GETS</span><i>2026</i></a>
<div class="nav-links"><a href="#shop">SHOP</a><a href="#categories">CATEGORIES</a><a href="#stack">BUILD A STACK</a><a href="#about">ABOUT</a></div>
<div class="search-box"><span>⌕</span><input id="search" placeholder="Search your stack..."></div>
<button class="cart">◫<b id="cartCount">0</b></button>
</nav></div>

<section class="hero">
<div class="hero-copy reveal">
<div class="eyebrow">INDIA'S DIGITAL SUPPLEMENT PLAYGROUND</div>
<h1>GET<br><span class="stroke">JACKED</span><br><span class="acid">LOUD.</span></h1>
<p>Supplements, but make it internet culture. Explore the stack, discover your next favourite product and enter full beast mode.</p>
<div class="hero-buttons"><a class="primary" href="#shop">EXPLORE THE DROP ↘</a><button class="secondary" id="surprise">SURPRISE ME ⚡</button></div>
<div class="stats"><div class="stat"><strong>20+</strong><small>Products</small></div><div class="stat"><strong>04</strong><small>Categories</small></div><div class="stat"><strong>∞</strong><small>Beast Mode</small></div></div>
</div>
<div class="hero-art reveal">
<div class="hero-ring"></div><div class="hero-product"><img src="{products[0][6]}" alt="Featured Avvatar Whey"></div>
<div class="float-chip chip1">⚡ HIGH PROTEIN</div><div class="float-chip chip2">★ TRENDING NOW</div><div class="float-chip chip3">3D STACK MODE</div>
</div>
</section>

<div class="marquee"><div class="marquee-track"><span>PROTEIN <b>✦</b> CREATINE <b>✦</b> WHEY <b>✦</b> PERFORMANCE <b>✦</b> BUILD LOUD <b>✦</b> PROTEIN <b>✦</b> CREATINE <b>✦</b> WHEY <b>✦</b> PERFORMANCE <b>✦</b> BUILD LOUD <b>✦</b></span></div></div>

<section class="section" id="categories">
<div class="section-top reveal"><div><div class="section-label">01 / CHOOSE YOUR ARC</div><h2 class="section-title">WHAT'S YOUR<br>STACK?</h2></div><p class="section-text">No boring catalogue energy. Pick a category and start building your supplement universe.</p></div>
<div class="category-grid">
<div class="cat-card reveal" data-jump="Whey"><div class="cat-num">01 / WHEY</div><div class="big-icon">🥤</div><h3>WHEY<br>PROTEIN</h3></div>
<div class="cat-card reveal" data-jump="Isolate"><div class="cat-num">02 / CLEAN</div><div class="big-icon">⚡</div><h3>ISOLATE</h3></div>
<div class="cat-card reveal" data-jump="Creatine"><div class="cat-num">03 / POWER</div><div class="big-icon">🧪</div><h3>CREATINE</h3></div>
<div class="cat-card reveal" data-jump="Premium"><div class="cat-num">04 / ELITE</div><div class="big-icon">👑</div><h3>PREMIUM</h3></div>
</div>
</section>

<section class="section" id="shop">
<div class="section-top reveal"><div><div class="section-label">02 / THE DROP</div><h2 class="section-title">PICK YOUR<br>POWER-UP.</h2></div><p class="section-text">Each card has a different product entry. Use search, filters and quick view to explore.</p></div>
<div class="filter-bar">
<button class="filter active" data-filter="All">ALL DROP</button><button class="filter" data-filter="Whey">WHEY</button><button class="filter" data-filter="Isolate">ISOLATE</button><button class="filter" data-filter="Creatine">CREATINE</button><button class="filter" data-filter="Premium">PREMIUM</button>
<span class="product-count"><span id="productCount">20</span> PRODUCTS FOUND</span>
</div>
<div class="product-grid" id="productGrid">{''.join(cards)}</div>
</section>

<section class="stack-banner" id="stack"><div class="stack-inner reveal"><div><div class="section-label" style="color:#111">03 / BUILD YOUR STACK</div><h2>NO NPC<br>SUPPLEMENTS.</h2><p>Click surprise mode and let RXHN GETS pick a random product from the collection.</p></div><button class="stack-btn" id="randomStack">GENERATE STACK ⚡</button></div></section>

<section class="section" id="about">
<div class="section-top reveal"><div><div class="section-label">04 / WHY RXHN GETS</div><h2 class="section-title">TOUCH.<br>SCROLL.<br>FLEX.</h2></div></div>
<div class="bento">
<div class="bento-card reveal"><span class="num">A / 3D TOUCH</span><h3>UI THAT DOESN'T FEEL LIKE A BORING STORE.</h3><p>Glass layers, glow, motion, hover depth and tactile interactions create a modern Gen-Z shopping experience.</p><div class="emoji">🌀</div></div>
<div class="bento-card reveal"><span class="num">B / FILTER</span><h3>FIND IT FAST.</h3><p>Search and category filters.</p><div class="emoji">⌕</div></div>
<div class="bento-card reveal"><span class="num">C / SAVE</span><h3>LIKE YOUR PICKS.</h3><p>Wishlist interactions for your favourite products.</p><div class="emoji">♡</div></div>
<div class="bento-card reveal"><span class="num">D / STACK</span><h3>BUILD LOUD.</h3><p>Products displayed with different direct image sources.</p><div class="emoji">⚡</div></div>
</div>
</section>

<section class="newsletter"><div class="section-label">RXHN GETS / DROP ALERTS</div><h2>DON'T MISS<br><span style="color:var(--acid)">THE NEXT DROP.</span></h2><p>Join the digital stack. No boring spam energy.</p><div class="email-box"><input placeholder="your@email.com"><button id="subscribe">JOIN THE LIST</button></div></section>
<footer><div class="logo">RXHN<span>GETS</span><i>2026</i></div><div>GEN-Z SUPPLEMENT SHOWCASE • SINGLE HTML FILE</div><div>© 2026 RXHN GETS</div></footer>

<div class="modal" id="modal"><div class="modal-box"><button class="close" id="closeModal">×</button><div class="modal-img"><img id="modalImage" alt=""></div><div class="modal-info"><div class="section-label" id="modalBrand"></div><h2 id="modalName"></h2><p id="modalMeta"></p><div class="rating"><span>★★★★★</span> <small>Community favourite</small></div><div class="modal-price" id="modalPrice"></div><p>This is a premium RXHN GETS product preview. Visit the official brand/store page for product details, availability and current pricing.</p><a id="modalLink" target="_blank" rel="noopener" class="modal-buy">VIEW PRODUCT ↗</a></div></div></div>
<div class="toast" id="toast"></div>

<script>
const products = {products!r};
const grid=document.getElementById("product
