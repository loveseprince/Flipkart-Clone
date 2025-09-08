<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flipkart Clone - Online Shopping</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', Arial, sans-serif;
            background-color: #f1f3f6;
            line-height: 1.6;
        }

        /* Header Styles */
        .header {
            background: linear-gradient(135deg, #2874f0 0%, #1e5bb8 100%);
            color: white;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 16px;
        }

        .header-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px 0;
            gap: 20px;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 24px;
            font-weight: bold;
            text-decoration: none;
            color: white;
            min-width: 140px;
        }

        .logo i {
            color: #ffe500;
        }

        .search-container {
            flex: 1;
            max-width: 500px;
            position: relative;
        }

        .search-box {
            width: 100%;
            padding: 12px 50px 12px 16px;
            border: none;
            border-radius: 8px;
            font-size: 14px;
            outline: none;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .search-btn {
            position: absolute;
            right: 12px;
            top: 50%;
            transform: translateY(-50%);
            background: none;
            border: none;
            color: #2874f0;
            cursor: pointer;
            font-size: 16px;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 24px;
        }

        .header-btn {
            display: flex;
            align-items: center;
            gap: 6px;
            color: white;
            text-decoration: none;
            font-size: 14px;
            padding: 8px 12px;
            border-radius: 6px;
            transition: background 0.3s;
        }

        .header-btn:hover {
            background: rgba(255,255,255,0.1);
        }

        .cart-count {
            background: #ff6b35;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 12px;
            margin-left: 4px;
        }

        /* Mobile Menu */
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 20px;
            cursor: pointer;
        }

        .mobile-nav {
            display: none;
            background: #1e5bb8;
            padding: 16px;
        }

        .mobile-nav.active {
            display: block;
        }

        .mobile-nav-item {
            display: block;
            color: white;
            text-decoration: none;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        /* Categories Bar */
        .categories-bar {
            background: white;
            border-bottom: 1px solid #e0e0e0;
            overflow-x: auto;
            scrollbar-width: none;
        }

        .categories-bar::-webkit-scrollbar {
            display: none;
        }

        .categories-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            gap: 0;
        }

        .category-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 16px 12px;
            text-decoration: none;
            color: #333;
            min-width: 80px;
            transition: all 0.3s;
            position: relative;
        }

        .category-item:hover {
            background: #f8f9fa;
            transform: translateY(-2px);
        }

        .category-item i {
            font-size: 20px;
            color: #2874f0;
            margin-bottom: 4px;
        }

        .category-item span {
            font-size: 12px;
            text-align: center;
            font-weight: 500;
        }

        /* Main Content */
        .main-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 16px;
        }

        /* Banner */
        .banner-section {
            margin-bottom: 24px;
        }

        .banner-slider {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }

        .banner-slide {
            width: 100%;
            height: 280px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            font-weight: bold;
            position: relative;
            background-size: cover;
            background-position: center;
        }

        .banner-content {
            text-align: center;
            z-index: 2;
        }

        .banner-title {
            font-size: 32px;
            margin-bottom: 12px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .banner-subtitle {
            font-size: 18px;
            opacity: 0.9;
        }

        /* Products Grid */
        .section {
            margin-bottom: 32px;
        }

        .section-header {
            display: flex;
            justify-content: between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 2px solid #2874f0;
        }

        .section-title {
            font-size: 24px;
            font-weight: 600;
            color: #333;
        }

        .view-all-btn {
            color: #2874f0;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 16px;
            border: 1px solid #2874f0;
            border-radius: 6px;
            transition: all 0.3s;
        }

        .view-all-btn:hover {
            background: #2874f0;
            color: white;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 16px;
        }

        .product-card {
            background: white;
            border-radius: 12px;
            padding: 16px;
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .product-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .product-image {
            width: 100%;
            height: 180px;
            background: linear-gradient(45deg, #f0f2f5, #e4e7eb);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 12px;
            position: relative;
            overflow: hidden;
        }

        .product-image i {
            font-size: 48px;
            color: #2874f0;
            opacity: 0.7;
        }

        .product-badge {
            position: absolute;
            top: 8px;
            right: 8px;
            background: #ff6b35;
            color: white;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: bold;
        }

        .product-title {
            font-size: 14px;
            font-weight: 500;
            color: #333;
            margin-bottom: 8px;
            line-height: 1.3;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .product-price {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-bottom: 8px;
        }

        .current-price {
            font-size: 16px;
            font-weight: bold;
            color: #333;
        }

        .original-price {
            font-size: 14px;
            color: #888;
            text-decoration: line-through;
        }

        .discount {
            color: #388e3c;
            font-size: 12px;
            font-weight: bold;
        }

        .product-rating {
            display: flex;
            align-items: center;
            gap: 4px;
            margin-bottom: 8px;
        }

        .rating-stars {
            color: #ff9800;
        }

        .rating-text {
            font-size: 12px;
            color: #666;
        }

        .add-to-cart-btn {
            width: 100%;
            padding: 10px;
            background: #2874f0;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s;
        }

        .add-to-cart-btn:hover {
            background: #1e5bb8;
        }

        /* Footer */
        .footer {
            background: #172337;
            color: white;
            margin-top: 48px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 16px 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 32px;
            margin-bottom: 32px;
        }

        .footer-section h3 {
            color: #fff;
            margin-bottom: 16px;
            font-size: 16px;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 8px;
        }

        .footer-section ul li a {
            color: #ccc;
            text-decoration: none;
            font-size: 14px;
            transition: color 0.3s;
        }

        .footer-section ul li a:hover {
            color: #2874f0;
        }

        .footer-bottom {
            border-top: 1px solid #333;
            padding-top: 20px;
            text-align: center;
            color: #ccc;
            font-size: 14px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-top {
                flex-wrap: wrap;
            }

            .header-actions {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .search-container {
                order: 3;
                flex-basis: 100%;
                margin-top: 12px;
            }

            .categories-container {
                justify-content: flex-start;
            }

            .category-item {
                min-width: 70px;
                padding: 12px 8px;
            }

            .category-item span {
                font-size: 11px;
            }

            .banner-slide {
                height: 200px;
            }

            .banner-title {
                font-size: 24px;
            }

            .banner-subtitle {
                font-size: 16px;
            }

            .products-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 12px;
            }

            .product-card {
                padding: 12px;
            }

            .product-image {
                height: 140px;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 24px;
            }
        }

        @media (max-width: 480px) {
            .products-grid {
                grid-template-columns: 1fr;
            }

            .main-content {
                padding: 16px 12px;
            }

            .section-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 12px;
            }
        }

        /* Loading Animation */
        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }

        .loading {
            animation: pulse 1.5s ease-in-out infinite;
        }

        /* Utility Classes */
        .text-center { text-align: center; }
        .mb-16 { margin-bottom: 16px; }
        .mb-24 { margin-bottom: 24px; }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-container">
            <div class="header-top">
                <a href="#" class="logo">
                    <i class="fas fa-shopping-bag"></i>
                    Flipkart
                </a>
                
                <div class="search-container">
                    <input type="text" class="search-box" placeholder="Search for products, brands and more">
                    <button class="search-btn">
                        <i class="fas fa-search"></i>
                    </button>
                </div>

                <div class="header-actions">
                    <a href="#" class="header-btn">
                        <i class="fas fa-user"></i>
                        Login
                    </a>
                    <a href="#" class="header-btn">
                        <i class="fas fa-heart"></i>
                        Wishlist
                    </a>
                    <a href="#" class="header-btn">
                        <i class="fas fa-shopping-cart"></i>
                        Cart
                        <span class="cart-count">3</span>
                    </a>
                </div>

                <button class="mobile-menu-btn" onclick="toggleMobileMenu()">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>

        <nav class="mobile-nav" id="mobileNav">
            <a href="#" class="mobile-nav-item">
                <i class="fas fa-user"></i> Login
            </a>
            <a href="#" class="mobile-nav-item">
                <i class="fas fa-heart"></i> Wishlist
            </a>
            <a href="#" class="mobile-nav-item">
                <i class="fas fa-shopping-cart"></i> Cart
            </a>
        </nav>
    </header>

    <!-- Categories Bar -->
    <div class="categories-bar">
        <div class="categories-container">
            <a href="#" class="category-item">
                <i class="fas fa-mobile-alt"></i>
                <span>Mobiles</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-laptop"></i>
                <span>Laptops</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-tshirt"></i>
                <span>Fashion</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-tv"></i>
                <span>Electronics</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-home"></i>
                <span>Home</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-couch"></i>
                <span>Furniture</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-dumbbell"></i>
                <span>Sports</span>
            </a>
            <a href="#" class="category-item">
                <i class="fas fa-book"></i>
                <span>Books</span>
            </a>
        </div>
    </div>

    <!-- Main Content -->
    <main class="main-content">
        <!-- Banner Section -->
        <section class="banner-section">
            <div class="banner-slider">
                <div class="banner-slide">
                    <div class="banner-content">
                        <h2 class="banner-title">Mega Sale</h2>
                        <p class="banner-subtitle">Up to 80% Off on Electronics</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Best Deals Section -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Best Deals</h2>
                <a href="#" class="view-all-btn">View All</a>
            </div>
            <div class="products-grid" id="dealsGrid">
                <!-- Products will be loaded here -->
            </div>
        </section>

        <!-- Electronics Section -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Electronics</h2>
                <a href="#" class="view-all-btn">View All</a>
            </div>
            <div class="products-grid" id="electronicsGrid">
                <!-- Products will be loaded here -->
            </div>
        </section>

        <!-- Fashion Section -->
        <section class="section">
            <div class="section-header">
                <h2 class="section-title">Fashion</h2>
                <a href="#" class="view-all-btn">View All</a>
            </div>
            <div class="products-grid" id="fashionGrid">
                <!-- Products will be loaded here -->
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <div class="footer-grid">
                <div class="footer-section">
                    <h3>About</h3>
                    <ul>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Press</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Help</h3>
                    <ul>
                        <li><a href="#">Payments</a></li>
                        <li><a href="#">Shipping</a></li>
                        <li><a href="#">Cancellation & Returns</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Policy</h3>
                    <ul>
                        <li><a href="#">Return Policy</a></li>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Security</a></li>
                        <li><a href="#">Privacy</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Social</h3>
                    <ul>
                        <li><a href="#">Facebook</a></li>
                        <li><a href="#">Twitter</a></li>
                        <li><a href="#">YouTube</a></li>
                        <li><a href="#">Instagram</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Flipkart Clone. All rights reserved. | Become a Seller | Advertise | Gift Cards</p>
            </div>
        </div>
    </footer>

    <script>
        // Sample product data
        const products = {
            deals: [
                {
                    title: "Samsung Galaxy S21 Ultra",
                    currentPrice: "₹89,999",
                    originalPrice: "₹1,05,999",
                    discount: "15% off",
                    rating: 4.5,
                    reviews: 1250,
                    icon: "fas fa-mobile-alt",
                    badge: "Deal"
                },
                {
                    title: "Apple MacBook Air M1",
                    currentPrice: "₹92,900",
                    originalPrice: "₹99,900",
                    discount: "7% off",
                    rating: 4.8,
                    reviews: 890,
                    icon: "fas fa-laptop",
                    badge: "Hot"
                },
                {
                    title: "Sony WH-1000XM4 Headphones",
                    currentPrice: "₹24,990",
                    originalPrice: "₹29,990",
                    discount: "17% off",
                    rating: 4.6,
                    reviews: 2340,
                    icon: "fas fa-headphones",
                    badge: "Sale"
                },
                {
                    title: "OnePlus 9 Pro 5G",
                    currentPrice: "₹64,999",
                    originalPrice: "₹69,999",
                    discount: "7% off",
                    rating: 4.3,
                    reviews: 567,
                    icon: "fas fa-mobile-alt",
                    badge: "New"
                }
            ],
            electronics: [
                {
                    title: "LG 55\" 4K Smart TV",
                    currentPrice: "₹52,999",
                    originalPrice: "₹65,999",
                    discount: "20% off",
                    rating: 4.4,
                    reviews: 890,
                    icon: "fas fa-tv",
                    badge: "Deal"
                },
                {
                    title: "Canon EOS 1500D DSLR",
                    currentPrice: "₹31,999",
                    originalPrice: "₹36,999",
                    discount: "14% off",
                    rating: 4.7,
                    reviews: 456,
                    icon: "fas fa-camera",
                    badge: "Hot"
                },
                {
                    title: "Dell Gaming Laptop",
                    currentPrice: "₹78,990",
                    originalPrice: "₹89,990",
                    discount: "12% off",
                    rating: 4.5,
                    reviews: 234,
                    icon: "fas fa-laptop",
                    badge: "Gaming"
                },
                {
                    title: "JBL Bluetooth Speaker",
                    currentPrice: "₹3,999",
                    originalPrice: "₹5,999",
                    discount: "33% off",
                    rating: 4.2,
                    reviews: 1890,
                    icon: "fas fa-volume-up",
                    badge: "Sale"
                }
            ],
            fashion: [
                {
                    title: "Levi's Men's Jeans",
                    currentPrice: "₹1,899",
                    originalPrice: "₹2,999",
                    discount: "37% off",
                    rating: 4.1,
                    reviews: 789,
                    icon: "fas fa-tshirt",
                    badge: "Fashion"
                },
                {
                    title: "Nike Running Shoes",
                    currentPrice: "₹4,995",
                    originalPrice: "₹6,995",
                    discount: "29% off",
                    rating: 4.6,
                    reviews: 1234,
                    icon: "fas fa-running",
                    badge: "Sports"
                },
                {
                    title: "Fossil Women's Watch",
                    currentPrice: "₹8,995",
                    originalPrice: "₹12,995",
                    discount: "31% off",
                    rating: 4.4,
                    reviews: 345,
                    icon: "fas fa-clock",
                    badge: "Luxury"
                },
                {
                    title: "Ray-Ban Sunglasses",
                    currentPrice: "₹7,999",
                    originalPrice: "₹12,999",
                    discount: "38% off",
                    rating: 4.7,
                    reviews: 567,
                    icon: "fas fa-glasses",
                    badge: "Brand"
                }
            ]
        };

        // Function to create product card HTML
        function createProductCard(product) {
            return `
                <div class="product-card" onclick="viewProduct('${product.title}')">
                    <div class="product-image">
                        <i class="${product.icon}"></i>
                        <span class="product-badge">${product.badge}</span>
                    </div>
                    <h3 class="product-title">${product.title}</h3>
                    <div class="product-price">
                        <span class="current-price">${product.currentPrice}</span>
                        <span class="original-price">${product.originalPrice}</span>
                        <span class="discount">${product.discount}</span>
                    </div>
                    <div class="product-rating">
                        <span class="rating-stars">${'★'.repeat(Math.floor(product.rating))}${'☆'.repeat(5-Math.floor(product.rating))}</span>
                        <span class="rating-text">(${product.reviews})</span>
                    </div>
                    <button class="add-to-cart-btn" onclick="event.stopPropagation(); addToCart('${product.title}')">
                        Add to Cart
                    </button>
                </div>
            `;
        }

        // Function to load products into grids
        function loadProducts() {
            const dealsGrid = document.getElementById('dealsGrid');
            const electronicsGrid = document.getElementById('electronicsGrid');
            const fashionGrid = document.getElementById('fashionGrid');

            dealsGrid.innerHTML = products.deals.map(createProductCard).join('');
            electronicsGrid.innerHTML = products.electronics.map(createProductCard).join('');
            fashionGrid.innerHTML = products.fashion.map(createProductCard).join('');
        }

        // Function to toggle mobile menu
        function toggleMobileMenu() {
            const mobileNav = document.getElementById('mobileNav');
            mobileNav.classList.toggle('active');
        }

        // Function to add to cart (placeholder)
        function addToCart(productTitle) {
            alert(`Added "${productTitle}" to cart!`);
            updateCartCount();
        }

        // Function to view product (placeholder)
        function viewProduct(productTitle) {
            alert(`Viewing "${productTitle}"`);
        }

        // Function to update cart count
        function updateCartCount() {
            const cartCount = document.querySelector('.cart-count');
            let currentCount = parseInt(cartCount.textContent);
            cartCount.textContent = currentCount + 1;
        }

        // Search functionality
        document.querySelector('.search-box').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                const query = e.target.value;
                if (query.trim()) {
                    alert(`Searching for: ${query}`);
                }
            }
        });

        document.querySelector('.search-btn').addEventListener('click', function() {
            const query = document.querySelector('.search-box').value;
            if (query.trim()) {
                alert(`Searching for: ${query}`);
            }
        });

        // Close mobile menu when clicking outside
        document.addEventListener('click', function(e) {
            const mobileNav = document.getElementById('mobileNav');
            const menuBtn = document.querySelector('.mobile-menu-btn');
            
            if (!mobileNav.contains(e.target) && !menuBtn.contains(e.target)) {
                mobileNav.classList.remove('active');
            }
        });

        // Smooth scrolling for category items
        document.querySelectorAll('.category-item').forEach(item => {
            item.addEventListener('click', function(e) {
                e.preventDefault();
                const categoryName = this.querySelector('span').textContent.toLowerCase();
                alert(`Browsing ${categoryName} category`);
            });
        });

        // Load products when page loads
        document.addEventListener('DOMContentLoaded', function() {
            loadProducts();
            
            // Add loading animation initially
            setTimeout(() => {
                document.querySelectorAll('.product-card').forEach(card => {
                    card.classList.remove('loading');
                });
            }, 500);
        });

        // Add scroll effect to categories bar
        let isScrolling = false;
        document.querySelector('.categories-bar').addEventListener('wheel', function(e) {
            if (!isScrolling) {
                isScrolling = true;
                this.scrollLeft += e.deltaY;
                setTimeout(() => { isScrolling = false; }, 100);
            }
        });
    </script>
</body>
</html>
