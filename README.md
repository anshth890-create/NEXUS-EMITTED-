<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AetherVault Enterprise • Cards, Aquatics & Digital Cinema</title>
  <style>
    :root {
      --bg-main: #0b0f19;
      --bg-card: #131a2a;
      --bg-glass: rgba(19, 26, 42, 0.85);
      --gold: #f5b041;
      --gold-hover: #f39c12;
      --accent-blue: #3b82f6;
      --accent-aqua: #06b6d4;
      --accent-purple: #8b5cf6;
      --whatsapp: #22c55e;
      --danger: #ef4444;
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
      --border: rgba(255, 255, 255, 0.08);
    }

    * { box-sizing: border-box; font-family: 'Segoe UI', system-ui, -apple-system, sans-serif; margin: 0; padding: 0; }
    body { background: var(--bg-main); color: var(--text-main); line-height: 1.5; }

    /* Top Luxury Navbar */
    nav {
      background: var(--bg-glass);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 1000;
      padding: 14px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }
    .brand { font-size: 22px; font-weight: 800; letter-spacing: 0.5px; display: flex; align-items: center; gap: 8px; }
    .brand span { color: var(--gold); }
    .nav-links { display: flex; gap: 8px; flex-wrap: wrap; }
    .nav-btn {
      background: transparent;
      color: var(--text-muted);
      border: 1px solid transparent;
      padding: 8px 16px;
      border-radius: 8px;
      font-weight: 600;
      font-size: 14px;
      cursor: pointer;
      transition: 0.25s;
    }
    .nav-btn:hover { color: white; background: rgba(255,255,255,0.05); }
    .nav-btn.active { background: rgba(245, 176, 65, 0.15); color: var(--gold); border-color: rgba(245, 176, 65, 0.4); }

    .seller-btn {
      background: linear-gradient(135deg, var(--gold), #d97706);
      color: #000;
      border: none;
      padding: 8px 16px;
      border-radius: 8px;
      font-weight: 700;
      font-size: 13px;
      cursor: pointer;
      transition: 0.2s;
    }
    .seller-btn:hover { transform: translateY(-1px); box-shadow: 0 4px 12px rgba(245, 176, 65, 0.3); }

    /* Hero Banner */
    .hero {
      background: radial-gradient(circle at top right, #1e293b, #0b0f19);
      padding: 40px 24px;
      text-align: center;
      border-bottom: 1px solid var(--border);
    }
    .hero h1 { font-size: 32px; font-weight: 800; margin-bottom: 8px; }
    .hero h1 span { color: var(--gold); }
    .hero p { color: var(--text-muted); max-width: 650px; margin: auto; font-size: 15px; }

    /* Main Container */
    .container { max-width: 1280px; margin: 30px auto; padding: 0 20px; }

    /* Seller Admin Panel (Hidden by Default) */
    .admin-panel {
      display: none;
      background: var(--bg-card);
      border: 1px solid rgba(245, 176, 65, 0.4);
      border-radius: 16px;
      padding: 24px;
      margin-bottom: 35px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }
    .admin-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 18px; border-bottom: 1px solid var(--border); padding-bottom: 12px; }
    .admin-header h2 { color: var(--gold); font-size: 19px; }
    .form-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 14px; }
    .form-group label { display: block; font-size: 12px; font-weight: 600; color: var(--text-muted); margin-bottom: 5px; text-transform: uppercase; letter-spacing: 0.5px; }
    .form-group input, .form-group select {
      width: 100%;
      padding: 10px 12px;
      background: #0b0f19;
      border: 1px solid var(--border);
      color: white;
      border-radius: 8px;
      font-size: 14px;
    }
    .form-group input:focus, .form-group select:focus { outline: none; border-color: var(--gold); }

    /* Section Header */
    .section-view { display: none; animation: fadeIn 0.3s ease; }
    .section-view.active { display: block; }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

    .section-title-bar { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; flex-wrap: wrap; gap: 12px; }
    .section-title-bar h2 { font-size: 24px; display: flex; align-items: center; gap: 10px; }
    .sub-tabs { display: flex; gap: 8px; }
    .sub-tab { background: var(--bg-card); color: var(--text-muted); border: 1px solid var(--border); padding: 6px 14px; border-radius: 20px; cursor: pointer; font-size: 13px; font-weight: 600; }
    .sub-tab.active { background: var(--accent-blue); color: white; border-color: var(--accent-blue); }

    /* Product Cards Grid */
    .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 22px; }
    .product-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 14px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: 0.25s;
      position: relative;
    }
    .product-card:hover { transform: translateY(-5px); border-color: rgba(245, 176, 65, 0.4); box-shadow: 0 12px 24px rgba(0,0,0,0.4); }
    .img-wrap { background: #080b12; height: 220px; display: flex; align-items: center; justify-content: center; padding: 12px; position: relative; }
    .img-wrap.movie-poster { padding: 0; height: 260px; }
    .img-wrap img { max-width: 100%; max-height: 100%; object-fit: contain; border-radius: 6px; }
    .img-wrap.movie-poster img { width: 100%; height: 100%; object-fit: cover; border-radius: 0; }

    .tag-discount { position: absolute; top: 12px; left: 12px; background: var(--danger); color: white; font-size: 11px; font-weight: 800; padding: 3px 8px; border-radius: 6px; }
    .tag-type { position: absolute; top: 12px; right: 12px; background: rgba(0,0,0,0.75); backdrop-filter: blur(4px); color: var(--gold); border: 1px solid rgba(245,176,65,0.3); font-size: 11px; font-weight: 700; padding: 3px 8px; border-radius: 6px; }

    .card-body { padding: 16px; flex-grow: 1; display: flex; flex-direction: column; justify-content: space-between; }
    .card-meta { font-size: 12px; color: var(--accent-aqua); font-weight: 600; margin-bottom: 4px; }
    .card-title { font-size: 17px; font-weight: 700; color: white; margin-bottom: 10px; }
    
    .price-row { display: flex; align-items: baseline; gap: 8px; margin-bottom: 12px; }
    .price-now { font-size: 21px; font-weight: 800; color: var(--gold); }
    .price-old { font-size: 13px; color: var(--text-muted); text-decoration: line-through; }

    .btn-group { display: flex; flex-direction: column; gap: 8px; }
    .btn-action {
      width: 100%;
      padding: 10px;
      border: none;
      border-radius: 8px;
      font-weight: 700;
      font-size: 13px;
      cursor: pointer;
      transition: 0.2s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
    }
    .btn-emi { background: rgba(59, 130, 246, 0.15); color: #60a5fa; border: 1px solid rgba(59, 130, 246, 0.3); }
    .btn-emi:hover { background: var(--accent-blue); color: white; }
    .btn-wa { background: var(--whatsapp); color: #052e16; }
    .btn-wa:hover { background: #16a34a; color: white; }
    .btn-del { background: rgba(239, 68, 68, 0.15); color: #f87171; border: 1px solid rgba(239, 68, 68, 0.3); margin-top: 4px; }
    .btn-del:hover { background: var(--danger); color: white; }

    /* Global Multi-Currency EMI Calculator */
    .emi-wrapper {
      max-width: 850px;
      margin: auto;
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px;
      display: grid;
      grid-template-columns: 1.2fr 1fr;
      gap: 28px;
    }
    @media (max-width: 768px) { .emi-wrapper { grid-template-columns: 1fr; } }
    .emi-results {
      background: linear-gradient(145deg, #0b0f19, #162033);
      border: 1px solid rgba(245, 176, 65, 0.3);
      border-radius: 12px;
      padding: 22px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    .emi-highlight { text-align: center; padding-bottom: 18px; border-bottom: 1px solid var(--border); margin-bottom: 18px; }
    .emi-highlight span { font-size: 13px; color: var(--text-muted); text-transform: uppercase; letter-spacing: 1px; }
    .emi-highlight h3 { font-size: 34px; color: var(--gold); margin-top: 4px; }
    .emi-detail-row { display: flex; justify-content: space-between; margin-bottom: 12px; font-size: 14px; }
    .emi-detail-row strong { color: white; }

    footer { text-align: center; padding: 30px 20px; color: var(--text-muted); font-size: 13px; border-top: 1px solid var(--border); margin-top: 50px; }
  </style>
</head>
<body>

  <!-- Navigation Bar -->
  <nav>
    <div class="brand">⚡ Aether<span>Vault</span></div>
    <div class="nav-links">
      <button class="nav-btn active" onclick="switchSection('pokemon', this)">🃏 Pokémon Store</button>
      <button class="nav-btn" onclick="switchSection('aquarium', this)">🐠 Fish Tanks & Aquatics</button>
      <button class="nav-btn" onclick="switchSection('movies', this)">🎬 Digital Movies</button>
      <button class="nav-btn" onclick="switchSection('emi', this)">🌍 Global EMI Calculator</button>
    </div>
    <button class="seller-btn" id="sellerAuthBtn" onclick="handleSellerAuth()">🔐 Seller Login</button>
  </nav>

  <!-- Hero Section -->
  <div class="hero">
    <h1>Exclusive Collectibles, <span>Custom Aquatics</span> & Cinema</h1>
    <p>Direct Owner Storefront • 20% Instant Store Discount • Worldwide Multi-Currency EMI Planner</p>
  </div>

  <div class="container">

    <!-- SELLER-ONLY ADMIN PANEL -->
    <div class="admin-panel" id="adminPanel">
      <div class="admin-header">
        <h2>👑 Owner Control Center (Add New Listing)</h2>
        <button class="sub-tab" onclick="logoutSeller()">Lock Panel 🔒</button>
      </div>
      <div class="form-grid">
        <div class="form-group">
          <label>Your WhatsApp Number (with Country Code)</label>
          <input type="text" id="ownerWhatsApp" value="919876543210" onchange="saveWhatsApp()">
        </div>
        <div class="form-group">
          <label>Select Store Section</label>
          <select id="itemSection">
            <option value="pokemon-card">🃏 Pokémon Single Card</option>
            <option value="pokemon-pack">📦 Pokémon Booster Pack / Box</option>
            <option value="aquarium">🐠 Fish Tank / Aquarium Setup</option>
            <option value="movie">🎬 Digital Movie (Thumbnail + Price)</option>
          </select>
        </div>
        <div class="form-group">
          <label>Title / Movie Name / Card Name</label>
          <input type="text" id="itemTitle" placeholder="e.g. Charizard VMAX / 4ft Glass Tank / Inception">
        </div>
        <div class="form-group">
          <label>Subtitle / Specs / Quality</label>
          <input type="text" id="itemSpecs" placeholder="e.g. Mint Condition / 100L + Filter / 4K BluRay">
        </div>
        <div class="form-group">
          <label>Price in INR (₹) [20% Off Auto on Cards/Tanks]</label>
          <input type="number" id="itemPrice" placeholder="e.g. 5000">
        </div>
        <div class="form-group">
          <label>Upload Photo / Movie Thumbnail (Gallery)</label>
          <input type="file" id="itemFile" accept="image/*">
        </div>
        <div class="form-group">
          <label>OR Image / Thumbnail Link (Optional)</label>
          <input type="text" id="itemUrl" placeholder="https://...">
        </div>
        <div class="form-group" style="display:flex; align-items:flex-end;">
          <button class="seller-btn" style="width:100%; padding:11px;" onclick="publishItem()">🚀 Publish Listing Live</button>
        </div>
      </div>
    </div>

    <!-- SECTION 1: POKÉMON CARDS & PACKS -->
    <div id="sec-pokemon" class="section-view active">
      <div class="section-title-bar">
        <h2>🃏 Pokémon Cards & Sealed Packs</h2>
        <div class="sub-tabs">
          <button class="sub-tab active" onclick="filterPoke('all', this)">All Pokémon</button>
          <button class="sub-tab" onclick="filterPoke('pokemon-card', this)">Single Cards</button>
          <button class="sub-tab" onclick="filterPoke('pokemon-pack', this)">Booster Packs</button>
        </div>
      </div>
      <div class="grid" id="grid-pokemon"></div>
    </div>

    <!-- SECTION 2: FISH TANKS & AQUARIUMS -->
    <div id="sec-aquarium" class="section-view">
      <div class="section-title-bar">
        <h2>🐠 Custom Fish Tanks & Aquarium Store</h2>
        <span style="color:var(--accent-aqua); font-size:14px; font-weight:600;">Direct Seller Verified • 20% OFF</span>
      </div>
      <div class="grid" id="grid-aquarium"></div>
    </div>

    <!-- SECTION 3: MOVIES SECTION -->
    <div id="sec-movies" class="section-view">
      <div class="section-title-bar">
        <h2>🎬 Exclusive Movies Collection</h2>
        <span style="color:var(--gold); font-size:14px; font-weight:600;">Select Movie & Contact Seller on WhatsApp to Buy</span>
      </div>
      <div class="grid" id="grid-movies"></div>
    </div>

    <!-- SECTION 4: MULTI-CURRENCY GLOBAL EMI CALCULATOR -->
    <div id="sec-emi" class="section-view">
      <div class="section-title-bar" style="justify-content:center; text-align:center;">
        <h2>🌍 Worldwide Multi-Currency EMI Calculator</h2>
      </div>
      <div class="emi-wrapper">
        <div>
          <div class="form-group" style="margin-bottom:14px;">
            <label>Select Country & Currency</label>
            <select id="emiCurrency" onchange="calculateGlobalEMI()">
              <option value="INR|en-IN|₹|1" selected>🇮🇳 India — INR (₹)</option>
              <option value="USD|en-US|$|0.0118">🇺🇸 United States — USD ($)</option>
              <option value="EUR|de-DE|€|0.0110">🇪🇺 Europe — EUR (€)</option>
              <option value="GBP|en-GB|£|0.0092">🇬🇧 United Kingdom — GBP (£)</option>
              <option value="AED|en-AE|AED |0.0433">🇦🇪 UAE — AED</option>
              <option value="AUD|en-AU|A$|0.0180">🇦🇺 Australia — AUD (A$)</option>
              <option value="CAD|en-CA|C$|0.0164">🇨🇦 Canada — CAD (C$)</option>
              <option value="JPY|ja-JP|¥|1.82">🇯🇵 Japan — JPY (¥)</option>
            </select>
          </div>
          <div class="form-group" style="margin-bottom:14px;">
            <label>Product Price (Base Amount in INR ₹)</label>
            <input type="number" id="emiPrincipal" value="15000" min="100" oninput="calculateGlobalEMI()">
          </div>
          <div class="form-group" style="margin-bottom:14px;">
            <label>Annual Interest Rate (%)</label>
            <input type="number" id="emiRate" value="12" min="0" max="60" step="0.1" oninput="calculateGlobalEMI()">
          </div>
          <div class="form-group">
            <label>Installment Tenure (Months)</label>
            <select id="emiTenure" onchange="calculateGlobalEMI()">
              <option value="3">3 Months</option>
              <option value="6" selected>6 Months</option>
              <option value="9">9 Months</option>
              <option value="12">12 Months (1 Year)</option>
              <option value="18">18 Months</option>
              <option value="24">24 Months (2 Years)</option>
              <option value="36">36 Months (3 Years)</option>
            </select>
          </div>
        </div>

        <div class="emi-results">
          <div class="emi-highlight">
            <span>Estimated Monthly EMI</span>
            <h3 id="resMonthly">₹0</h3>
          </div>
          <div class="emi-detail-row">
            <span style="color:var(--text-muted);">Principal Amount:</span>
            <strong id="resPrincipal">₹0</strong>
          </div>
          <div class="emi-detail-row">
            <span style="color:var(--text-muted);">Total Interest Payable:</span>
            <strong id="resInterest">₹0</strong>
          </div>
          <div class="emi-detail-row" style="border-top:1px solid var(--border); padding-top:10px; margin-top:6px;">
            <span style="color:var(--gold);">Total Amount Payable:</span>
            <strong id="resTotal" style="color:var(--gold); font-size:16px;">₹0</strong>
          </div>
        </div>
      </div>
    </div>

  </div>

  <footer>
    © 2026 AetherVault Direct Store • Only Authorized Seller Can List Products • All Transactions Verified via WhatsApp
  </footer>

  <script>
    // SELLER SECURITY PIN (Change this password anytime)
    const SELLER_PIN = "admin123";
    let isSellerAuthenticated = false;
    let currentPokeFilter = "all";

    // Default Initial Inventory
    const initialInventory = [
      { id: 101, section: "pokemon-card", title: "Charizard VMAX Rainbow", specs: "Secret Rare • PSA 10 Mint", price: 24500, image: "https://images.pokemontcg.io/swsh35/74_hires.png" },
      { id: 102, section: "pokemon-pack", title: "Scarlet & Violet 151 Booster Pack", specs: "Factory Sealed • 10 Cards", price: 1250, image: "https://tcgplayer-cdn.tcgplayer.com/product/502006_in_1000x1000.jpg" },
      { id: 103, section: "pokemon-card", title: "Articuno GX Full Art", specs: "Ultra Rare • Near Mint", price: 8500, image: "https://images.pokemontcg.io/sm7/31_hires.png" },
      { id: 201, section: "aquarium", title: "Crystal Clear Rimless Nano Tank (60L)", specs: "Ultra-White Glass + LED Light + Silent Filter", price: 6500, image: "https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?auto=format&fit=crop&w=600&q=80" },
      { id: 202, section: "aquarium", title: "Planted Aquascape Complete Setup", specs: "3ft Tank + CO2 Diffuser + 50W Heater", price: 14000, image: "https://images.unsplash.com/photo-1544551763-46a013bb70d5?auto=format&fit=crop&w=600&q=80" },
      { id: 301, section: "movie", title: "Interstellar (IMAX Collector's Edition)", specs: "4K Ultra HD • Dual Audio • Instant Access", price: 499, image: "https://images.unsplash.com/photo-1534447677768-be436bb09401?auto=format&fit=crop&w=600&q=80" },
      { id: 302, section: "movie", title: "The Dark Knight Trilogy", specs: "1080p Blu-Ray Rip • Complete Bundle", price: 799, image: "https://images.unsplash.com/photo-1509347528160-9a9e33742cdb?auto=format&fit=crop&w=600&q=80" }
    ];

    let inventory = JSON.parse(localStorage.getItem("aetherVaultEnterprise_v1")) || initialInventory;

    // Load Saved WhatsApp
    const savedWA = localStorage.getItem("aetherVaultOwnerWA");
    if (savedWA) document.getElementById("ownerWhatsApp").value = savedWA;

    function saveWhatsApp() {
      localStorage.setItem("aetherVaultOwnerWA", document.getElementById("ownerWhatsApp").value.trim());
    }

    // Seller Authentication (Only Owner Can Sell)
    function handleSellerAuth() {
      if (isSellerAuthenticated) {
        const panel = document.getElementById("adminPanel");
        panel.style.display = panel.style.display === "block" ? "none" : "block";
        return;
      }
      const enteredPin = prompt("Enter Owner Seller Password to Manage Store (Default: admin123):");
      if (enteredPin === SELLER_PIN) {
        isSellerAuthenticated = true;
        document.getElementById("adminPanel").style.display = "block";
        document.getElementById("sellerAuthBtn").innerText = "⚙️ Owner Panel";
        renderAllSections();
      } else if (enteredPin !== null) {
        alert("❌ Incorrect Password! Only the store owner can add or edit items.");
      }
    }

    function logoutSeller() {
      isSellerAuthenticated = false;
      document.getElementById("adminPanel").style.display = "none";
      document.getElementById("sellerAuthBtn").innerText = "🔐 Seller Login";
      renderAllSections();
    }

    // Switch Top Navigation Ta
