<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Allin1Insurance.lk | Sri Lanka Motor Insurance</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #004080;
            --secondary: #ff6600;
            --bg-light: #f4f7f6;
            --text-dark: #333;
            --white: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
        }

        /* --- Welcome Modal / Overlay --- */
        #welcome-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            background: rgba(0, 64, 128, 0.95);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }

        .modal-content {
            background: var(--white);
            padding: 40px;
            border-radius: 12px;
            text-align: center;
            max-width: 500px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .modal-content h1 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        .modal-content p {
            margin-bottom: 30px;
            color: #666;
        }

        .btn-container {
            display: flex;
            gap: 20px;
            justify-content: center;
        }

        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.2s, background 0.3s;
        }

        .btn-3rd-party {
            background: var(--bg-light);
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-full {
            background: var(--secondary);
            color: var(--white);
        }

        .btn:hover {
            transform: translateY(-3px);
            opacity: 0.9;
        }

        /* --- Main Website Layout --- */
        header {
            background: var(--primary);
            color: var(--white);
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        header .logo {
            font-size: 24px;
            font-weight: 700;
        }

        header .logo span {
            color: var(--secondary);
        }

        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 40px;
        }

        /* --- Quotation Form --- */
        .form-section {
            background: var(--white);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            height: fit-content;
        }

        .form-section h2 {
            margin-bottom: 20px;
            color: var(--primary);
            font-size: 22px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
            font-size: 14px;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 14px;
        }

        .submit-btn {
            width: 100%;
            background: var(--secondary);
            color: var(--white);
            border: none;
            padding: 15px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 10px;
            transition: background 0.3s;
        }

        .submit-btn:hover {
            background: #e65c00;
        }

        .selected-policy-badge {
            display: inline-block;
            background: var(--bg-light);
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 12px;
            color: var(--primary);
            margin-bottom: 15px;
            font-weight: bold;
        }

        /* --- Partners Grid --- */
        .partners-section h2 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 28px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .company-card {
            background: var(--white);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .company-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }

        .company-card img {
            max-width: 100%;
            height: 80px;
            object-fit: contain;
            margin-bottom: 15px;
            border-radius: 4px;
        }

        .company-card h3 {
            font-size: 16px;
            color: var(--text-dark);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
            .btn-container {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <div id="welcome-modal">
        <div class="modal-content">
            <h1>Allin1Insurance.lk</h1>
            <p>Welcome! To get the most accurate quotations from our partners, please select the type of cover you are looking for.</p>
            <div class="btn-container">
                <button class="btn btn-3rd-party" onclick="enterSite('3rd Party Insurance')">3rd Party Insurance</button>
                <button class="btn btn-full" onclick="enterSite('Full Insurance (Comprehensive)')">Full Insurance</button>
            </div>
        </div>
    </div>

    <header>
        <div class="logo">Allin1<span>Insurance.lk</span></div>
        <div style="font-size: 14px;">Sri Lanka's #1 Aggregator</div>
    </header>

    <div class="container">
        
        <div class="form-section">
            <h2>Request Quotations</h2>
            <div class="selected-policy-badge" id="policy-display">Cover Type: Not Selected</div>
            
            <form id="quote-form">
                <div class="form-group">
                    <label>Vehicle Make & Model</label>
                    <input type="text" placeholder="e.g. Toyota Aqua, Honda Fit" required>
                </div>
                <div class="form-group">
                    <label>Year of Manufacture</label>
                    <input type="number" placeholder="e.g. 2018" required>
                </div>
                <div class="form-group">
                    <label>Registration Number</label>
                    <input type="text" placeholder="e.g. CBA-1234 (or 'Unregistered')" required>
                </div>
                <div class="form-group">
                    <label>Your Full Name</label>
                    <input type="text" placeholder="John Doe" required>
                </div>
                <div class="form-group">
                    <label>Mobile Number</label>
                    <input type="tel" placeholder="07XXXXXXXX" required>
                </div>
                <button type="submit" class="submit-btn">Get Quotes from All Partners</button>
            </form>
        </div>

        <div class="partners-section">
            <h2>Our Partner Companies</h2>
            <p style="margin-bottom: 20px; color: #666;">We will fetch the best rates from all registered general motor insurers in Sri Lanka.</p>
            <div class="grid" id="companies-grid">
                </div>
        </div>

    </div>

    <script>
        // Store the user's initial selection
        let selectedCoverType = "";

        // Function to handle the modal buttons
        function enterSite(coverType) {
            selectedCoverType = coverType;
            
            // Update the form to reflect the user's choice
            document.getElementById('policy-display').innerText = "Cover Type: " + selectedCoverType;
            
            // Hide the modal smoothly
            const modal = document.getElementById('welcome-modal');
            modal.style.opacity = "0";
            setTimeout(() => {
                modal.style.display = "none";
            }, 500);
        }

        // --- INSURANCE COMPANIES DATA ---
        // To use real logos, replace the URL in the 'logo' field with your local file path.
        // Example: logo: "images/ceylinco-logo.png"
        
        const insuranceCompanies = [
            { name: "Sri Lanka Insurance (SLIC)", logo: "https://placehold.co/200x100/004080/FFF?text=SLIC" },
            { name: "Ceylinco General", logo: "https://placehold.co/200x100/cc0000/FFF?text=Ceylinco" },
            { name: "Allianz Insurance", logo: "https://placehold.co/200x100/0033a0/FFF?text=Allianz" },
            { name: "Fairfirst Insurance", logo: "https://placehold.co/200x100/ff6600/FFF?text=Fairfirst" },
            { name: "HNB General", logo: "https://placehold.co/200x100/ffcc00/000?text=HNB+General" },
            { name: "Janashakthi Insurance", logo: "https://placehold.co/200x100/fca311/000?text=Janashakthi" },
            { name: "LOLC General", logo: "https://placehold.co/200x100/00296b/FFF?text=LOLC" },
            { name: "People's Insurance", logo: "https://placehold.co/200x100/008000/FFF?text=People's" },
            { name: "Amana Takaful", logo: "https://placehold.co/200x100/00b4d8/FFF?text=Amana" },
            { name: "Continental Insurance", logo: "https://placehold.co/200x100/d62828/FFF?text=Continental" },
            { name: "Co-operative Insurance", logo: "https://placehold.co/200x100/2a9d8f/FFF?text=Co-op" },
            { name: "MBSL Insurance", logo: "https://placehold.co/200x100/e76f51/FFF?text=MBSL" },
            { name: "Orient Insurance", logo: "https://placehold.co/200x100/f4a261/FFF?text=Orient" },
            { name: "Sanasa General", logo: "https://placehold.co/200x100/e9c46a/000?text=Sanasa" }
        ];

        // Function to render the companies into the HTML grid
        function renderCompanies() {
            const gridContainer = document.getElementById('companies-grid');
            
            insuranceCompanies.forEach(company => {
                const card = document.createElement('div');
                card.className = 'company-card';
                card.innerHTML = `
                    <img src="${company.logo}" alt="${company.name} Logo">
                    <h3>${company.name}</h3>
                `;
                gridContainer.appendChild(card);
            });
        }

        // Handle the Form Submission
        document.getElementById('quote-form').addEventListener('submit', function(e) {
            e.preventDefault(); // Prevents the page from refreshing
            
            // In a real website, this is where you would send data to a backend server.
            // For the portfolio, we will just show a success alert.
            alert(`Success! Your request for ${selectedCoverType} has been submitted to all 14 partners. They will contact you shortly.`);
            
            // Reset the form
            this.reset();
        });

        // Initialize the app by rendering the companies
        renderCompanies();

    </script>
</body>
</html># Allin1insurance1.lk
