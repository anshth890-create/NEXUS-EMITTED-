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

        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background: var(--bg-main); color: var(--text-main); min-height: 100vh; display: flex; flex-direction: column; }

        header {
            background: rgba(11, 15, 25, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo { font-size: 1.5rem; font-weight: 800; background: linear-gradient(135deg, var(--gold), var(--accent-aqua)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; letter-spacing: 1px; }
        nav { display: flex; gap: 1rem; align-items: center; flex-wrap: wrap; }
        .nav-btn { background: transparent; border: 1px solid var(--border); color: var(--text-main); padding: 0.5rem 1rem; border-radius: 8px; cursor: pointer; transition: 0.3s; font-weight: 600; }
        .nav-btn:hover, .nav-btn.active { background: var(--gold); color: #000; border-color: var(--gold); }

        .container { max-width: 1400px; margin: 2rem auto; padding: 0 1rem; width: 100%; flex: 1; }
        .section { display: none; }
        .section.active { display: block; }

        .hero-banner {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1), rgba(245, 176, 65, 0.1));
            border: 1px solid var(--border);
            border-radius: 16px;
            padding: 3rem 2rem;
            text-align: center;
            margin-bottom: 2rem;
        }
        .hero-banner h1 { font-size: 2.5rem; margin-bottom: 1rem; background: linear-gradient(135deg, #fff, var(--text-muted)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .hero-banner p { color: var(--text-muted); font-size: 1.1rem; max-width: 600px; margin: 0 auto; }

        .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 1.5rem; }
        
        .card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .card:hover { transform: translateY(-5px); box-shadow: 0 10px 30px rgba(0,0,0,0.5); border-color: rgba(245, 176, 65, 0.3); }
        .card img { width: 100%; height: 220px; object-fit: cover; }
        .card-content { padding: 1.25rem; }
        .card-title { font-size: 1.2rem; font-weight: 700; margin-bottom: 0.5rem; }
        .card-desc { color: var(--text-muted); font-size: 0.9rem; margin-bottom: 1rem; line-height: 1.4; }
        .price-tag { font-size: 1.3rem; font-weight: 800; color: var(--gold); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem; }
        .original-price { text-decoration: line-through; color: var(--text-muted); font-size: 0.9rem; }

        .btn {
            width: 100%;
            padding: 0.75rem;
            border: none;
            border-radius: 8px;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            transition: 0.2s;
        }
        .btn-whatsapp { background: var(--whatsapp); color: #fff; }
        .btn-whatsapp:hover { opacity: 0.9; }

        /* EMI Calculator Styles */
        .calculator-card { background: var(--bg-card); border: 1px solid var(--border); border-radius: 16px; padding: 2rem; max-width: 600px; margin: 0 auto; }
        .form-group { margin-bottom: 1.25rem; }
        .form-group label { display: block; margin-bottom: 0.5rem; font-weight: 600; color: var(--text-muted); }
        .form-group input, .form-group select { width: 100%; padding: 0.75rem; background: var(--bg-main); border: 1px solid var(--border); border-radius: 8px; color: var(--text-main); font-size: 1rem; }
        .emi-result { background: rgba(245, 176, 65, 0.1); border: 1px solid var(--gold); border-radius: 12px; padding: 1.5rem; text-align: center; margin-top: 1.5rem; }
        .emi-result h3 { font-size: 2rem; color: var(--gold); margin-top: 0.5rem; }

        /* Admin Modal */
        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); backdrop-filter: blur(5px); justify-content: center; align-items: center; z-index: 2000; }
        .modal-content { background: var(--bg-card); border: 1px solid var(--border); padding: 2rem; border-radius: 16px; width: 100%; max-width: 500px; position: relative; }
        .close-modal { position: absolute; top: 1rem; right: 1rem; background: none; border: none; color: var(--text-main); font-size: 1.5rem; cursor: pointer; }

        @media(max-width: 768px) {
            header { padding: 1rem; flex-direction: column; gap: 1rem; }
            .hero-banner h1 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">⚡ AETHERVAULT ENTERPRISE</div>
        <nav>
            <button class="nav-btn active" onclick="switchTab('cards')">Pokémon Cards</button>
            <button class="nav-btn" onclick="switchTab('aquatics')">Aquatics & Fish</button>
            <button class="nav-btn" onclick="switchTab('movies')">Digital Cinema</button>
            <button class="nav-btn" onclick="switchTab('emi')">EMI Calculator</button>
            <button class="nav-btn" onclick="openAdminLogin()" style="border-color: var(--accent-purple);">Admin</button>
        </nav>
    </header>

    <div class="container">
        <!-- POKEMON CARDS SECTION -->
        <div id="cards-section" class="section active">
            <div class="hero-banner">
                <h1>Rare Pokémon Collectibles</h1>
                <p>Explore verified holographic prints, rare editions, and graded collector cards with automated discounts.</p>
            </div>
            <div class="grid" id="pokemon-grid"></div>
        </div>

        <!-- AQUATICS SECTION -->
        <div id="aquatics-section" class="section">
            <div class="hero-banner">
                <h1>Aquarium & Fishkeeping Gear</h1>
                <p>Professional grade filters, heaters, premium diets, and vibrant aquatic life delivered securely.</p>
            </div>
            <div class="grid" id="aquatics-grid"></div>
        </div>

        <!-- MOVIES SECTION -->
        <div id="movies-section" class="section">
            <div class="hero-banner">
                <h1>Digital Movie Showcase</h1>
                <p>Stream highlights and connect instantly via WhatsApp for digital access and cinematic rentals.</p>
            </div>
            <div class="grid" id="movies-grid"></div>
        </div>

        <!-- EMI CALCULATOR SECTION -->
        <div id="emi-section" class="section">
            <div class="hero-banner">
                <h1>Multi-Currency EMI Calculator</h1>
                <p>Plan your flexible installment payments across multiple global currencies instantly.</p>
            </div>
            <div class="calculator-card">
                <div class="form-group">
                    <label>Select Currency</label>
                    <select id="currency-select" onchange="calculateEMI()">
                        <option value="₹">INR (₹)</option>
                        <option value="$">USD ($)</option>
                        <option value="€">EUR (€)</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Principal Amount</label>
                    <input type="number" id="loan-amount" value="15000" oninput="calculateEMI()">
                </div>
                <div class="form-group">
                    <label>Annual Interest Rate (%)</label>
                    <input type="number" id="interest-rate" value="12" step="0.1" oninput="calculateEMI()">
                </div>
                <div class="form-group">
                    <label>Tenure (Months)</label>
                    <input type="number" id="loan-tenure" value="6" oninput="calculateEMI()">
                </div>
                <div class="emi-result">
                    <span style="color: var(--text-muted); font-size: 0.9rem;">Estimated Monthly Payment</span>
                    <h3 id="emi-output">₹2,596</h3>
                </div>
            </div>
        </div>
    </div>

    <!-- ADMIN MODAL -->
    <div id="admin-modal" class="modal">
        <div class="modal-content">
            <button class="close-modal" onclick="closeModal()">&times;</button>
            <h2 style="margin-bottom: 1.5rem;">Admin Panel Login</h2>
            <div class="form-group">
                <label>Admin Password</label>
                <input type="password" id="admin-pass" placeholder="Enter password (admin123)">
            </div>
            <button class="btn btn-whatsapp" onclick="verifyAdmin()">Authenticate</button>
        </div>
    </div>

    <script>
        let storeData = {
            cards: [
                { id: 1, title: "Articuno GX (Holofoil)", price: 2499, original: 3120, img: "https://images.unsplash.com/photo-1613771404784-3a5686aa2be3?w=500&q=80", desc: "Mint condition holographic collectible card with protective case." },
                { id: 2, title: "Rainbow Charizard VMAX", price: 4999, original: 6249, img: "https://images.unsplash.com/photo-1607604276583-eef5d076aa5f?w=500&q=80", desc: "Ultra-rare secret rare edition with pristine centering." }
            ],
            aquatics: [
                { id: 1, title: "50W Submersible Aquarium Heater", price: 1299, original: 1624, img: "https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?w=500&q=80", desc: "Precision temperature control thermostat for freshwater tanks." },
                { id: 2, title: "Optimum Green Pellet Food (1kg)", price: 450, original: 562, img: "https://images.unsplash.com/photo-1535591273668-578e3112a44f?w=500&q=80", desc: "High protein color-enhancing sinking diet for Goldfish and Cichlids." }
            ],
            movies: [
                { id: 1, title: "Stranger Things Season Showcase", price: 799, original: 999, img: "https://images.unsplash.com/photo-1536440136628-849c177e76a1?w=500&q=80", desc: "Cinematic digital vault release with behind-the-scenes features." },
                { id: 2, title: "Sci-Fi Cyberpunk Anthology", price: 599, original: 749, img: "https://images.unsplash.com/photo-1518709268805-4e9042af9f23?w=500&q=80", desc: "Exclusive futuristic short-film series with 4K HDR mastering." }
            ]
        };

        function switchTab(tabId) {
            document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));
            
            const targetSec = document.getElementById(tabId + '-section');
            if(targetSec) targetSec.classList.add('active');
            event.target.classList.add('active');
        }

        function renderStore() {
            document.getElementById('pokemon-grid').innerHTML = storeData.cards.map(item => `
                <div class="card">
                    <img src="${item.img}" alt="${item.title}">
                    <div class="card-content">
                        <div class="card-title">${item.title}</div>
                        <div class="card-desc">${item.desc}</div>
                        <div class="price-tag">₹${item.price} <span class="original-price">₹${item.original}</span></div>
                        <button class="btn btn-whatsapp" onclick="orderWhatsApp('${item.title}', ${item.price})">Order via WhatsApp</button>
                    </div>
                </div>
            `).join('');

            document.getElementById('aquatics-grid').innerHTML = storeData.aquatics.map(item => `
                <div class="card">
                    <img src="${item.img}" alt="${item.title}">
                    <div class="card-content">
                        <div class="card-title">${item.title}</div>
                        <div class="card-desc">${item.desc}</div>
                        <div class="price-tag">₹${item.price} <span class="original-price">₹${item.original}</span></div>
                        <button class="btn btn-whatsapp" onclick="orderWhatsApp('${item.title}', ${item.price})">Order via WhatsApp</button>
                    </div>
                </div>
            `).join('');

            document.getElementById('movies-grid').innerHTML = storeData.movies.map(item => `
                <div class="card">
                    <img src="${item.img}" alt="${item.title}">
                    <div class="card-content">
                        <div class="card-title">${item.title}</div>
                        <div class="card-desc">${item.desc}</div>
                        <div class="price-tag">₹${item.price} <span class="original-price">₹${item.original}</span></div>
                        <button class="btn btn-whatsapp" onclick="orderWhatsApp('${item.title}', ${item.price})">Inquire via WhatsApp</button>
                    </div>
                </div>
            `).join('');
        }

        function orderWhatsApp(itemTitle, itemPrice) {
            const message = encodeURIComponent(`Hello AetherVault, I would like to order/inquire about: *${itemTitle}* priced at ₹${itemPrice}. Please share further details.`);
            window.open(`https://wa.me/?text=${message}`, '_blank');
        }

        function calculateEMI() {
            const curr = document.getElementById('currency-select').value;
            const P = parseFloat(document.getElementById('loan-amount').value) || 0;
            const r = (parseFloat(document.getElementById('interest-rate').value) || 0) / 12 / 100;
            const n = parseFloat(document.getElementById('loan-tenure').value) || 1;

            let emi = 0;
            if (r === 0) {
                emi = P / n;
            } else {
                emi = (P * r * Math.pow(1 + r, n)) / (Math.pow(1 + r, n) - 1);
            }
            document.getElementById('emi-output').innerText = curr + Math.round(emi).toLocaleString();
        }

        function openAdminLogin() {
            document.getElementById('admin-modal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('admin-modal').style.display = 'none';
        }

        function verifyAdmin() {
            const pass = document.getElementById('admin-pass').value;
            if(pass === 'admin123') {
                alert('Authentication Successful! Admin controls unlocked.');
                closeModal();
            } else {
                alert('Incorrect Password! Default is admin123');
            }
        }

        window.onload = () => {
            renderStore();
            calculateEMI();
        };
    </script>
</body>
</html>
