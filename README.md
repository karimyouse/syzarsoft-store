<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SyzarSoft Store</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Reset and Body Styling */
        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #e6f2ef; /* خلفية فاتحة تناسب ألوان الشعار */
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
    
        /* Header and Navigation Styling */
        header {
            background-color: #2f4f4f; /* لون داكن لتكامل مع الشعار */
            color: white;
            padding: 20px;
            text-align: center;
        }
    
        nav {
            background-color: #56c596; /* لون متوافق مع الشعار */
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 5px 30px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
    
        /* Logo Styling */
        .nav-left {
            display: flex;
            align-items: center;
            gap: 20px;
        }
    
        .nav-logo img {
            width: 70px; /* تكبير الشعار */
            height: 70px;
            border-radius: 12px;
            transition: transform 0.3s ease;
        }
    
        .nav-logo img:hover {
            transform: scale(1.1); /* تأثير تكبير عند التمرير */
        }
    
        /* Navigation Menu */
        .nav-menu {
            display: flex;
            gap: 20px;
        }
    
        .nav-menu a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }
    
        .nav-menu a:hover {
            color: #004d40;
        }
    
        /* Search Bar */
        .search-bar {
            position: relative;
            width: 300px;
        }
    
        .search-bar input {
            width: 100%;
            padding: 10px 15px;
            border: none;
            border-radius: 20px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            outline: none;
        }
    
        .search-bar button {
            position: absolute;
            right: 10px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            cursor: pointer;
            color: #004d40;
            font-size: 18px;
        }
    
        /* Icons Section */
        .nav-icons {
            display: flex;
            gap: 20px;
            align-items: center;
        }
    
        .nav-icons a {
            color: white;
            font-size: 24px;
            text-decoration: none;
            transition: transform 0.2s;
        }
    
        .nav-icons a:hover {
            transform: scale(1.1);
        }
    
        /* Support Links */
        .support {
            display: flex;
            align-items: center;
            gap: 15px;
        }
    
        .support a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s ease, transform 0.3s ease, background-color 0.3s ease;
            padding: 8px 12px;
            border-radius: 8px;
        }
    
        .support a i {
            color: #ffe08a;
            transition: color 0.3s ease;
        }
    
        .support a:hover {
            background-color: #ffe08a;
            color: #004d40;
            transform: scale(1.1);
        }
    
        .support a:hover i {
            color: #004d40;
        }
    
        /* Section Styling */
        section {
            margin: 20px;
            padding: 20px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease-in-out;
        }
    
        section:hover {
            transform: scale(1.02);
        }
    
        /* Product Grid */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
    
        .product {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            text-align: center;
            padding: 15px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
    
        .product:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
    
        .product img {
            max-width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
        }
    
        /* Button Styling */
        button {
            background-color: #56c596;
            color: white;
            border: none;
            padding: 12px 24px;
            cursor: pointer;
            border-radius: 8px;
            transition: background-color 0.3s ease, transform 0.2s ease;
            width: 100%;
            margin-top: 10px;
        }
    
        button:hover {
            background-color: #388e3c;
            transform: translateY(-3px);
        }
    
        /* Footer */
        footer {
            text-align: center;
            padding: 1px;
            background-color: #333;
            color: white;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    
        /* Back-to-Top Button */
        #back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #56c596;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }
    
        #back-to-top:hover {
            background-color: #004d40;
            transform: scale(1.1);
        }
    
        @media (max-width: 768px) {
            .nav-menu {
                flex-direction: column;
                align-items: center;
            }
    
            section {
                margin: 10px;
            }
        }

        #payment-methods {
        margin: 20px;
        padding: 20px;
        background-color: white;
        border-radius: 12px;
        box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    }

    #payment-methods h2 {
        text-align: center;
        color: #004d40;
        margin-bottom: 15px;
    }

    .payment-list {
        list-style-type: none;
        padding: 0;
        font-size: 18px;
    }

    .payment-list li {
        background-color: #f3f7fb;
        margin: 10px 0;
        padding: 10px;
        border-radius: 8px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }

    .payment-list li strong {
        color: #2f4f4f;
    }

    .modal {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    z-index: 2000;
    text-align: center;
    animation: fadeIn 0.5s ease;
}

.modal h2 {
    margin-bottom: 10px;
    color: #004d40;
}

.modal button {
    background-color: #56c596;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.modal button:hover {
    background-color: #388e3c;
}

/* Fade In Animation */
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
    
        html {
            scroll-behavior: smooth;
        }
    </style>
    
</head>
<body>
    <header>
        <h1>SyzarSoft Store</h1>
        <div class="modal" id="welcomeModal">
            <h2>Welcome to SyzarSoft Store!</h2>
            <p>Enjoy our special discounts on all products today!</p>
            <button onclick="closeModal()">Close</button>
        </div>
        <nav>
            <div class="nav-left">
                <div class="nav-logo">
                    <img src="https://i.imgur.com/Mhmy4N8.png" alt="SyzarSoft Logo">
                </div>
                <div class="nav-menu">
                    <a href="#windows">Windows Keys</a>
                    <a href="#antivirus">Antivirus</a>
                    <a href="#vpn">VPN</a>
                    <a href="#idm">IDM</a>
                    <a href="#iobit">IObit</a>
                </div>
            </div>
        
            <div class="nav-icons">
                <div class="support">
                    <a href="mailto:karim51600002@gmail.com" target="_blank">
                        <i class="fas fa-envelope"></i> Email Us
                    </a>
                    <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                        <i class="fas fa-phone"></i> +972567611790
                    </a>
                </div>
            </div>
        </nav>
    </header>

    <section id="windows">
        <h2>Windows Keys</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://i.imgur.com/gpRmL3J.png" alt="Windows 10 Pro">
                <h3>Windows 10 Pro OEM Key</h3>
                <p>Price: 20.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/gpRmL3J.png" alt="Windows 10 Pro">
                <h3>Windows 10 Pro Retail Key</h3>
                <p>Price: 50.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/qiKzCOz.png" alt="Windows 11 Professional OEM">
                <h3>Windows 11 Professional OEM Key</h3>
                <p>Price: 25.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/qiKzCOz.png" alt="Windows 11 Professional Retail">
                <h3>Windows 11 Professional Retail Key</h3>
                <p>Price: 54.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/C1tIeid.png" alt="Windows 11 Home OEM">
                <h3>Windows 11 Home OEM Key</h3>
                <p>Price: 20.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/C1tIeid.png" alt="Windows 11 Home Retail">
                <h3>Windows 11 Home Retail Key</h3>
                <p>Price: 50.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/6xiYflr.png" alt="Windows 10 Home">
                <h3>Windows 10 Home OEM Key</h3>
                <p>Price: 20.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/qkzDcUO.png" alt="Windows 8.1 Pro">
                <h3>Windows 8.1 Pro OEM Key</h3>
                <p>Price: 15.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
        </div>
    </section>

    <section id="antivirus">
        <h2>Antivirus Programs</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://i.imgur.com/vxGgekx.png" alt="Bitdefender Antivirus">
                <h3>Bitdefender Antivirus Plus PC - 1 Device 1 Year Key</h3>
                <p>Price: 59.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/RwVGZqt.png" alt="Trend Micro Maximum Security">
                <h3>Trend Micro Maximum Security - 5 Devices 3 Years Key</h3>
                <p>Price: 79.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/RwVGZqt.png" alt="Kaspersky Internet Security 2024">
                <h3>Kaspersky Internet Security 2024 Key - 1 Device 1 Year</h3>
                <p>Price: 54.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/oTPkwLB.png" alt="Kaspersky Anti-Virus 2023">
                <h3>Kaspersky Anti-Virus 2023 Key - 1 Device 1 Year</h3>
                <p>Price: 64.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/p7Z1koV.png" alt="AVG Ultimate 2023">
                <h3>AVG Ultimate 2023 - 10 Devices 2 Years Key</h3>
                <p>Price: 99.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/39KlEhI.png" alt="McAfee AntiVirus 2024">
                <h3>McAfee AntiVirus 2024 (PC) - (1 Device) - (1 Year Key)</h3>
                <p>Price: 39.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
    
            
            <div class="product">
                <img src="https://i.imgur.com/Bxs03jV.png" alt="Avast Cleanup Premium">
                <h3>Avast Cleanup Premium Key - 10 Devices 1 Year</h3>
                <p>Price: 110.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/3HalC39.png" alt="Avast Ultimate">
                <h3>Avast Ultimate Key - 10 Devices 1 Year</h3>
                <p>Price: 100.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/p7Z1koV.png" alt="AVG Ultimate 2023">
                <h3>AVG Ultimate 2023 - 10 Devices 3 Years Key</h3>
                <p>Price: 128.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/RI4z0CP.jpeg" alt="ESET NOD32 Antivirus Security">
                <h3>ESET NOD32 Antivirus Security - 1 PC 1 Year</h3>
                <p>Price: 179.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/toKGfjn.jpeg" alt="ESET NOD32 Antivirus Security">
                <h3>ESET NOD32 Antivirus Security - 3 PCs - 1 Year</h3>
                <p>Price: 199.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/HJqEEg8.jpeg" alt="ESET Internet Security">
                <h3>ESET Internet Security - 1 PC - 1 Year</h3>
                <p>Price: 224.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/6mGJG7h.jpeg" alt="ESET Internet Security">
                <h3>ESET Internet Security - 3 PCs - 1 Year</h3>
                <p>Price: 249.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/JOSODYr.jpeg" alt="ESET NOD32 Antivirus Security">
                <h3>ESET NOD32 Antivirus Security - 5 PCs - 1 Year</h3>
                <p>Price: 279.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/WSxJjwZ.jpeg" alt="ESET Internet Security">
                <h3>ESET Internet Security - 5 PCs - 1 Year</h3>
                <p>Price: 307.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/Dk5vkpK.jpeg" alt="ESET Smart Security Premium">
                <h3>ESET Smart Security Premium - 1 Device 1 Year</h3>
                <p>Price: 364.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/3WOcJNf.png" alt="IObit Malware Fighter 10 PRO">
                <h3>IObit Malware Fighter 10 PRO - 1 Device 1 Year</h3>
                <p>Price: 62.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
        </div>
    </section>
    
    <section id="vpn">
        <h2>VPN Programs</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://i.imgur.com/U6JrlI0.png" alt="Avast SecureLine VPN">
                <h3>Avast SecureLine VPN Key - 1 Device 2 Years</h3>
                <p>Price: 73.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/U6JrlI0.png" alt="Avast SecureLine VPN">
                <h3>Avast SecureLine VPN Key - 1 Device 1 Year</h3>
                <p>Price: 30.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/GUmaumQ.png" alt="PureVPN Key">
                <h3>PureVPN Key - 10 Devices 1 Year</h3>
                <p>Price: 114.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/GUmaumQ.png" alt="PureVPN Key">
                <h3>PureVPN Key - 10 Devices 2 Years</h3>
                <p>Price: 95.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/heZVBJx.png" alt="Avast HMA Pro VPN">
                <h3>Avast HMA Pro VPN Key - Unlimited Devices 1 Year</h3>
                <p>Price: 44.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
        </div>
    </section>
    

    <section id="idm">
        <h2>IDM Program</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://i.imgur.com/zEcHEAG.jpeg" alt="Internet Download Manager">
                <h3>Internet Download Manager Key - 1 Device 1 Year</h3>
                <p>Price: 39.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/jVTL9VC.jpeg" alt="Internet Download Manager">
                <h3>Internet Download Manager Key - 1 Device Lifetime</h3>
                <p>Price: 85.50 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
        </div>
    </section>

    <section id="iobit">
        <h2>IObit Programs</h2>
        <div class="product-grid">
            <div class="product">
                <img src="https://i.imgur.com/RTW7Xgz.png" alt="IObit Protected Folder PRO">
                <h3>IObit Protected Folder PRO - 1 Device 1 Year</h3>
                <p>Price: 14.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/RTW7Xgz.png" alt="iObit Protected Folder">
                <h3>iObit Protected Folder - 1 PC - 20 Years</h3>
                <p>Price: 99.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/cK7k4bV.png" alt="IObit Driver Booster 10 PRO">
                <h3>IObit Driver Booster 10 PRO - 1 Device 1 Year</h3>
                <p>Price: 39.49 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/cK7k4bV.png" alt="IObit Driver Booster 10 PRO">
                <h3>IObit Driver Booster 10 PRO - 3 Devices 1 Year</h3>
                <p>Price: 50.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/cK7k4bV.png" alt="IObit Driver Booster 10 PRO">
                <h3>IObit Driver Booster 10 PRO - 1 Device 2 Years</h3>
                <p>Price: 79.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/7Fc8yuN.png" alt="IObit Uninstaller 12 PRO">
                <h3>IObit Uninstaller 12 PRO - 3 Devices 1 Year</h3>
                <p>Price: 47.99 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
            <div class="product">
                <img src="https://i.imgur.com/3WOcJNf.png" alt="IObit Malware Fighter 10 PRO">
                <h3>IObit Malware Fighter 10 PRO - 1 Device 1 Year</h3>
                <p>Price: 62.00 ILS</p>
                <a href="https://wa.me/qr/J4JLLVTUONAXG1" target="_blank">
                    <button>Buy Now</button>
                </a>
            </div>
        </div>
    </section>

    <section id="payment-methods">
        <h2>Payment Methods</h2>
        <ul class="payment-list">
            <li><strong>Bank of Palestine:</strong> Account Number - 123456789</li>
            <li><strong>My Bank:</strong> Account Number - 0599791033</li>
        </ul>
    </section>
    
    <footer>
        <p>&copy; 2024 SyzarSoft Store. All Rights Reserved.</p>
    </footer>

    <button id="back-to-top">&#8679;</button>

    <script>
        const backToTopButton = document.getElementById('back-to-top');
        const nav = document.querySelector('nav');
        const navLinks = document.querySelectorAll('.nav-link');
        let lastScrollTop = 0;

        window.addEventListener('scroll', () => {
            let scrollTop = window.pageYOffset || document.documentElement.scrollTop;

            if (scrollTop > lastScrollTop) {
                nav.classList.add('hidden');
            } else {
                nav.classList.remove('hidden');
            }
            lastScrollTop = scrollTop;

            backToTopButton.style.display = scrollTop > 300 ? 'block' : 'none';
        });

        window.addEventListener('load', () => {
    // Show the modal after 1 second
    setTimeout(() => {
        document.getElementById('welcomeModal').style.display = 'block';
    }, 1000);
});

function closeModal() {
    document.getElementById('welcomeModal').style.display = 'none';
}


        backToTopButton.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                document.querySelector(link.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
            });
        });
    </script>
</body>
</html>
