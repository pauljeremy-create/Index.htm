
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>DSAJO INTERNATIONAL SELLER | Premium IT & Electronics, Tanzania</title>
  <!-- Google Fonts + Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f4f7fc;
      color: #1e2a3e;
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    /* tech themed background subtle pattern overlay */
    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: url('https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=2070&auto=format');
      background-size: cover;
      background-position: center;
      opacity: 0.08;
      pointer-events: none;
      z-index: -2;
    }

    /* modern glassmorphism + gradients */
    :root {
      --primary: #0066cc;
      --primary-dark: #004d99;
      --secondary: #00a3cc;
      --accent: #ff8c42;
      --dark: #0a1927;
      --light: #ffffff;
      --gray-bg: #f0f4f9;
    }

    .container {
      max-width: 1300px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* header / navigation */
    .navbar {
      background: rgba(10, 25, 39, 0.92);
      backdrop-filter: blur(12px);
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
    }
    .nav-container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      padding: 1rem 2rem;
      max-width: 1400px;
      margin: 0 auto;
    }
    .logo h2 {
      color: white;
      font-weight: 700;
      letter-spacing: -0.5px;
    }
    .logo span {
      color: var(--accent);
      font-size: 1.1rem;
    }
    .nav-links {
      display: flex;
      gap: 1.8rem;
      list-style: none;
      flex-wrap: wrap;
    }
    .nav-links a {
      color: #eef2ff;
      text-decoration: none;
      font-weight: 500;
      transition: 0.3s;
      font-size: 1rem;
    }
    .nav-links a:hover, .nav-links a.active {
      color: var(--accent);
      transform: translateY(-2px);
    }
    .menu-icon {
      font-size: 1.8rem;
      color: white;
      cursor: pointer;
      display: none;
    }

    /* Hero */
    .hero {
      background: linear-gradient(135deg, rgba(0,30,50,0.85), rgba(0,80,100,0.85)), url('https://images.unsplash.com/photo-1550745165-9bc0c2527bb8?q=80&w=2070&auto=format');
      background-size: cover;
      background-position: center;
      padding: 5rem 1rem;
      text-align: center;
      color: white;
    }
    .hero h1 {
      font-size: 3rem;
      font-weight: 800;
      animation: fadeUp 0.8s ease;
    }
    .hero p {
      font-size: 1.2rem;
      margin: 1rem 0;
      max-width: 700px;
      margin-left: auto;
      margin-right: auto;
    }
    .cta-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
    }
    .btn-primary, .btn-secondary {
      padding: 12px 28px;
      border-radius: 40px;
      font-weight: 600;
      transition: 0.3s;
      text-decoration: none;
      display: inline-block;
    }
    .btn-primary {
      background: var(--accent);
      color: #1e2a3e;
    }
    .btn-primary:hover {
      background: #ff9e5e;
      transform: scale(1.02);
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    }
    .btn-secondary {
      background: transparent;
      border: 2px solid white;
      color: white;
    }
    .btn-secondary:hover {
      background: white;
      color: #0066cc;
    }

    /* sections */
    section {
      padding: 4rem 0;
    }
    .section-title {
      text-align: center;
      font-size: 2.2rem;
      font-weight: 700;
      margin-bottom: 2.5rem;
      position: relative;
    }
    .section-title:after {
      content: '';
      width: 80px;
      height: 4px;
      background: var(--accent);
      position: absolute;
      bottom: -12px;
      left: 50%;
      transform: translateX(-50%);
      border-radius: 4px;
    }

    /* product cards */
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
      gap: 2rem;
    }
    .product-card {
      background: white;
      border-radius: 24px;
      overflow: hidden;
      box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .product-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 30px -10px rgba(0,0,0,0.15);
    }
    .product-img {
      height: 180px;
      background: #eef2ff;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 4rem;
      color: var(--primary);
    }
    .product-info {
      padding: 1.2rem;
    }
    .product-info h3 {
      font-size: 1.2rem;
      font-weight: 700;
    }
    .price {
      font-weight: 800;
      color: var(--primary-dark);
      margin: 0.5rem 0;
      font-size: 1.3rem;
    }
    .qty-selector {
      display: flex;
      align-items: center;
      gap: 8px;
      margin: 10px 0;
    }
    .qty-selector button {
      background: #e2e8f0;
      border: none;
      width: 28px;
      height: 28px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: bold;
    }
    .qty-input {
      width: 50px;
      text-align: center;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    .buy-now {
      background: var(--primary);
      color: white;
      border: none;
      padding: 8px 12px;
      border-radius: 40px;
      width: 100%;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
      margin-top: 5px;
    }
    .buy-now:hover {
      background: var(--primary-dark);
    }

    /* order summary + checkout */
    .order-checkout {
      background: white;
      border-radius: 28px;
      padding: 1.5rem;
      box-shadow: 0 12px 30px rgba(0,0,0,0.08);
      margin-top: 2rem;
    }
    .cart-items {
      margin-bottom: 1rem;
      max-height: 260px;
      overflow-y: auto;
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid #eef2f0;
      padding: 8px 0;
    }
    .checkout-form input, .checkout-form textarea, .contact-form input, .contact-form textarea {
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 20px;
      font-family: inherit;
    }
    .submit-btn {
      background: var(--primary);
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 40px;
      font-weight: bold;
      cursor: pointer;
    }

    /* payment methods icons */
    .payment-icons {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
      font-size: 2rem;
      margin: 1rem 0;
    }
    .testimonial-grid {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
      justify-content: center;
    }
    .testimonial-card {
      background: white;
      padding: 1.5rem;
      border-radius: 24px;
      width: 280px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    }
    footer {
      background: #0a1927;
      color: #bbccdd;
      padding: 2rem 0;
      text-align: center;
    }
    .social-icons i {
      font-size: 1.8rem;
      margin: 0 12px;
      color: white;
      transition: 0.2s;
    }
    .map {
      border-radius: 24px;
      overflow: hidden;
      height: 300px;
    }
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(20px);}
      to { opacity: 1; transform: translateY(0);}
    }
    @media (max-width: 900px) {
      .menu-icon { display: block; }
      .nav-links {
        position: fixed;
        top: 70px;
        left: -100%;
        flex-direction: column;
        background: #0a1927e6;
        backdrop-filter: blur(20px);
        width: 70%;
        padding: 2rem;
        border-radius: 0 20px 20px 0;
        transition: 0.3s;
        gap: 1.8rem;
      }
      .nav-links.active {
        left: 0;
      }
    }
  </style>
</head>
<body>
<div class="navbar">
  <div class="nav-container">
    <div class="logo"><h2>DSAJO<span> IT SELLER</span></h2></div>
    <div class="menu-icon" id="menuToggle"><i class="fas fa-bars"></i></div>
    <ul class="nav-links" id="navLinks">
      <li><a href="#home" class="nav-link">Home</a></li>
      <li><a href="#about" class="nav-link">About Us</a></li>
      <li><a href="#products" class="nav-link">Products</a></li>
      <li><a href="#services" class="nav-link">Services</a></li>
      <li><a href="#orders" class="nav-link">Orders</a></li>
      <li><a href="#payment" class="nav-link">Payment Methods</a></li>
      <li><a href="#contact" class="nav-link">Contact</a></li>
    </ul>
  </div>
</div>

<!-- Hero -->
<section id="home" class="hero">
  <div class="container">
    <h1>Power Your World with DSAJO</h1>
    <p>Premium Computers, Laptops, CCTV, Networking & Electronics – Trusted supplier in Tanzania.</p>
    <div class="cta-buttons">
      <a href="#products" class="btn-primary"><i class="fas fa-shopping-cart"></i> Shop Now</a>
      <a href="#contact" class="btn-secondary"><i class="fas fa-headset"></i> Contact Sales</a>
    </div>
  </div>
</section>

<div class="container">
  <!-- About -->
  <section id="about">
    <h2 class="section-title">About Company</h2>
    <p style="text-align:center; max-width:800px; margin:0 auto; line-height:1.6;">DSAJO INTERNATIONAL SELLER is a leading IT & electronics provider based in Moshi, Tanzania. We specialize in cutting-edge computers, laptops, networking devices, CCTV systems, printers, and accessories. With a passion for technology and customer satisfaction, we deliver authentic products and end-to-end support for businesses and individuals.</p>
    <div style="text-align:center; margin-top:30px;"><i class="fas fa-map-marker-alt"></i> <strong>Moshi, Tanzania</strong> | <i class="fab fa-whatsapp"></i> +255761927093</div>
  </section>

  <!-- Products section with sample product cards -->
  <section id="products">
    <h2 class="section-title">Featured Products</h2>
    <div class="products-grid" id="productsGrid"></div>
  </section>

  <!-- Services section -->
  <section id="services">
    <h2 class="section-title">Our Services</h2>
    <div style="display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:1.5rem; text-align:center;">
      <div><i class="fas fa-laptop-code" style="font-size:2.5rem; color:#0066cc;"></i><h3>IT Consultancy</h3></div>
      <div><i class="fas fa-shield-alt" style="font-size:2.5rem; color:#0066cc;"></i><h3>CCTV Installation</h3></div>
      <div><i class="fas fa-network-wired" style="font-size:2.5rem; color:#0066cc;"></i><h3>Networking Solutions</h3></div>
      <div><i class="fas fa-print" style="font-size:2.5rem; color:#0066cc;"></i><h3>Printer Support</h3></div>
    </div>
  </section>

  <!-- Orders + shopping cart -->
  <section id="orders">
    <h2 class="section-title">Order Summary & Checkout</h2>
    <div class="order-checkout">
      <h3><i class="fas fa-cart-plus"></i> Your Cart</h3>
      <div id="cartItemsList" class="cart-items">Cart is empty.</div>
      <div><strong>Total: </strong>TZS <span id="cartTotal">0</span></div>
      <hr>
      <h3>Checkout Form</h3>
      <form id="checkoutForm" class="checkout-form">
        <input type="text" id="fullName" placeholder="Full Name" required>
        <input type="email" id="emailAddr" placeholder="Email" required>
        <input type="tel" id="phoneNum" placeholder="Phone" required>
        <textarea id="deliveryAddr" rows="2" placeholder="Delivery Address - Moshi / Tanzania"></textarea>
        <button type="submit" class="submit-btn">Place Order <i class="fas fa-check-circle"></i></button>
      </form>
      <div id="orderMessage" style="margin-top:10px; color:green;"></div>
    </div>
  </section>

  <!-- Payment Methods -->
  <section id="payment">
    <h2 class="section-title">Payment Methods</h2>
    <div class="payment-icons">
      <i class="fas fa-mobile-alt"></i> M-Pesa &nbsp;|&nbsp; <i class="fas fa-mobile-alt"></i> Airtel Money &nbsp;|&nbsp; <i class="fas fa-mobile-alt"></i> Tigo Pesa
      <i class="fas fa-university"></i> Bank Transfer &nbsp;|&nbsp; <i class="fab fa-cc-visa"></i> Visa/MasterCard
    </div>
    <p style="text-align:center;">Fast & secure payments: M-Pesa, Airtel Money, Tigo Pesa, Bank Transfer, Cards accepted.</p>
  </section>

  <!-- Contact + Google Map + Testimonials + Newsletter -->
  <section id="contact">
    <h2 class="section-title">Contact Us</h2>
    <div style="display:grid; grid-template-columns:1fr 1fr; gap:2rem;">
      <div>
        <form id="contactForm">
          <input type="text" id="contactName" placeholder="Name" required>
          <input type="email" id="contactEmail" placeholder="Email" required>
          <input type="tel" id="contactPhone" placeholder="Phone">
          <textarea id="contactMsg" rows="3" placeholder="Your message..."></textarea>
          <button type="submit" class="submit-btn">Send Message <i class="fas fa-paper-plane"></i></button>
          <p id="formFeedback" style="margin-top:8px;"></p>
        </form>
        <div style="margin-top:1rem;"><i class="fas fa-envelope"></i> saulojeremiah2@gmail.com<br><i class="fab fa-whatsapp"></i> +255761927093<br><i class="fas fa-map-pin"></i> Moshi, Tanzania</div>
      </div>
      <div class="map">
        <iframe width="100%" height="100%" style="border:0; border-radius:20px;" loading="lazy" allowfullscreen referrerpolicy="no-referrer-when-downgrade" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d101381.43988521325!2d37.2834036!3d-3.3348381!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1833b5f20c91cbe1%3A0x5faa2e7d45c0eacc!2sMoshi%2C%20Tanzania!5e0!3m2!1sen!2stz!4v1712334567890!5m2!1sen!2stz"></iframe>
      </div>
    </div>
  </section>

  <!-- Testimonials -->
  <section>
    <h2 class="section-title">What Our Clients Say</h2>
    <div class="testimonial-grid">
      <div class="testimonial-card"><i class="fas fa-star" style="color:#ffaa33;"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><p>"Best IT supplier in Moshi! Genuine laptops and fast service."</p><h4>- Grace M.</h4></div>
      <div class="testimonial-card"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><p>"CCTV installation was seamless, excellent after-sales support."</p><h4>- Joseph K.</h4></div>
      <div class="testimonial-card"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i><p>"Reliable networking gear and professional team."</p><h4>- Aisha S.</h4></div>
    </div>
  </section>

  <!-- Newsletter -->
  <section>
    <div style="background:#0a1927; padding:2rem; border-radius:48px; text-align:center; color:white;">
      <h3>Subscribe to our Newsletter</h3>
      <div style="display:flex; flex-wrap:wrap; justify-content:center; gap:12px; margin-top:1rem;">
        <input type="email" id="newsletterEmail" placeholder="Your email address" style="padding:12px; border-radius:40px; border:none; width:260px;">
        <button id="newsletterBtn" class="btn-primary" style="background:#ff8c42;">Subscribe</button>
      </div>
      <p id="newsMsg" style="margin-top:10px;"></p>
    </div>
  </section>
</div>

<footer>
  <div class="social-icons">
    <i class="fab fa-facebook-f"></i> <i class="fab fa-twitter"></i> <i class="fab fa-instagram"></i> <i class="fab fa-linkedin-in"></i> <i class="fab fa-whatsapp"></i>
  </div>
  <p>🩸Moshi, Tanzania | 📞 +255761927093 | 📧 saulojeremiah2@gmail.com</p>
  <p><strong>Developed by Paul Jeremy</strong> | <strong>Published by DSAJO Developers</strong></p>
  <p>© 2025 DSAJO INTERNATIONAL SELLER – Premium IT & Electronics. All rights reserved.</p>
</footer>

<script>
  // sample products array
  const products = [
    { id:1, name:"Gaming Laptop", price:1850000, icon:"fas fa-laptop-code", desc:"High-performance RTX graphics" },
    { id:2, name:"Desktop Computer", price:950000, icon:"fas fa-desktop", desc:"Core i7, 16GB RAM" },
    { id:3, name:"Wireless Router", price:185000, icon:"fas fa-wifi", desc:"Dual-band Gigabit" },
    { id:4, name:"CCTV Camera", price:210000, icon:"fas fa-video", desc:"4MP night vision" },
    { id:5, name:"HP Printer", price:450000, icon:"fas fa-print", desc:"All-in-one wireless" },
    { id:6, name:"External Hard Drive", price:320000, icon:"fas fa-hdd", desc:"2TB USB 3.0" },
    { id:7, name:"Mechanical Keyboard", price:125000, icon:"fas fa-keyboard", desc:"RGB mechanical" },
    { id:8, name:"LED Monitor", price:520000, icon:"fas fa-tv", desc:"24inch 75Hz" },
    { id:9, name:"UPS Power Backup", price:380000, icon:"fas fa-bolt", desc:"650VA surge protection" },
    { id:10, name:"Computer Mouse", price:45000, icon:"fas fa-mouse", desc:"Wireless ergonomic" }
  ];

  let cart = [];

  function renderProducts(){
    const grid = document.getElementById("productsGrid");
    if(!grid) return;
    grid.innerHTML = "";
    products.forEach(p => {
      const card = document.createElement("div");
      card.className = "product-card";
      card.innerHTML = `
        <div class="product-img"><i class="${p.icon}" style="font-size:4rem;"></i></div>
        <div class="product-info">
          <h3>${p.name}</h3>
          <p style="font-size:0.8rem;">${p.desc}</p>
          <div class="price">TZS ${p.price.toLocaleString()}</div>
          <div class="qty-selector">
            <button class="qty-minus" data-id="${p.id}">-</button>
            <input type="number" class="qty-input" id="qty-${p.id}" value="1" min="1" style="width:55px;">
            <button class="qty-plus" data-id="${p.id}">+</button>
          </div>
          <button class="buy-now" data-id="${p.id}"><i class="fas fa-cart-plus"></i> Add to Cart</button>
        </div>
      `;
      grid.appendChild(card);
    });
    // attach events dynamically
    document.querySelectorAll('.buy-now').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const id = parseInt(btn.dataset.id);
        const qtyInput = document.getElementById(`qty-${id}`);
        let qty = parseInt(qtyInput.value);
        if(isNaN(qty) || qty<1) qty=1;
        addToCart(id, qty);
      });
    });
    document.querySelectorAll('.qty-plus').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const id = parseInt(btn.dataset.id);
        const inp = document.getElementById(`qty-${id}`);
        inp.value = parseInt(inp.value)+1;
      });
    });
    document.querySelectorAll('.qty-minus').forEach(btn => {
      btn.addEventListener('click', (e) => {
        const id = parseInt(btn.dataset.id);
        const inp = document.getElementById(`qty-${id}`);
        let val = parseInt(inp.value);
        if(val>1) inp.value = val-1;
      });
    });
  }

  function addToCart(productId, quantity){
    const product = products.find(p => p.id === productId);
    if(!product) return;
    const existing = cart.find(item => item.id === productId);
    if(existing){
      existing.quantity += quantity;
    } else {
      cart.push({ ...product, quantity });
    }
    updateCartUI();
    showToast(`${product.name} added to cart!`);
  }

  fun
