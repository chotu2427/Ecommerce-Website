<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8"> <!-- Ensures proper character encoding -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Makes the site responsive -->
    <title>ShopEasy - E-Commerce</title>
    <link rel="stylesheet" href="styles.css"> <!-- Links to the CSS file -->
</head>
<body>
    <!-- Header Section: Contains logo and navigation -->
    <header>
        <div class="logo">
            <h1>ShopEasy</h1> <!-- Brand name -->
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#cart" class="cart">Cart (<span id="cart-count">0</span>)</a></li> <!-- Cart with counter -->
            </ul>
        </nav>
    </header>

    <!-- Hero Section: Promotional banner to attract users -->
    <section class="hero" id="home">
        <h2>Discover Amazing Deals at ShopEasy</h2>
        <p>Shop the latest electronics, fashion, and more at unbeatable prices!</p>
        <a href="#products" class="btn">Shop Now</a> <!-- Call-to-action button -->
    </section>

    <!-- Product Filter Section: Allows users to filter products -->
    <section class="filter">
        <h3>Filter Products</h3>
        <div class="filter-options">
            <select id="category-filter">
                <option value="all">All Categories</option>
                <option value="electronics">Electronics</option>
                <option value="fashion">Fashion</option>
                <option value="accessories">Accessories</option>
            </select>
            <input type="text" id="search-bar" placeholder="Search products...">
        </div>
    </section>

    <!-- Products Section: Displays product cards in a grid -->
    <section id="products" class="products">
        <h2>Our Products</h2>
        <div class="product-grid">
            <!-- Product Card 1 -->
            <div class="product-card" data-category="electronics">
                <img src="https://via.placeholder.com/200" alt="Smartphone">
                <h3>Smartphone Pro</h3>
                <p class="price">$499.99</p>
                <p class="description">Latest 5G smartphone with 128GB storage.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <!-- Product Card 2 -->
            <div class="product-card" data-category="electronics">
                <img src="https://via.placeholder.com/200" alt="Laptop">
                <h3>UltraBook</h3>
                <p class="price">$999.99</p>
                <p class="description">Lightweight laptop with 16GB RAM.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <!-- Product Card 3 -->
            <div class="product-card" data-category="accessories">
                <img src="https://via.placeholder.com/200" alt="Headphones">
                <h3>Wireless Headphones</h3>
                <p class="price">$99.99</p>
                <p class="description">Noise-canceling headphones with 20h battery.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <!-- Product Card 4 -->
            <div class="product-card" data-category="fashion">
                <img src="https://via.placeholder.com/200" alt="Jacket">
                <h3>Leather Jacket</h3>
                <p class="price">$149.99</p>
                <p class="description">Stylish jacket for all seasons.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
        </div>
    </section>

    <!-- Footer Section: Contains copyright and links -->
    <footer>
        <p>© 2025 ShopEasy. All rights reserved.</p>
        <div class="footer-links">
            <a href="#privacy">Privacy Policy</a> | 
            <a href="#terms">Terms of Service</a> | 
            <a href="#support">Customer Support</a>
        </div>
    </footer>
</body>
</html>
/* Reset default styles for consistency */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    line-height: 1.6;
    color: #333;
    background: #f4f4f4; /* Light background for contrast */
}

/* Header Styles */
header {
    background: #2c3e50; /* Dark blue background */
    color: #fff;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky; /* Sticks header to top when scrolling */
    top: 0;
    z-index: 100;
}

.logo h1 {
    font-size: 1.8rem;
    font-weight: bold;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 1.5rem; /* Space between nav items */
}

nav ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 1rem;
    transition: color 0.3s; /* Smooth color transition on hover */
}

nav ul li a:hover {
    color: #f1c40f; /* Yellow hover effect */
}

.cart {
    background: #e74c3c; /* Red background for cart */
    padding: 0.5rem 1rem;
    border-radius: 5px;
}

/* Hero Section */
.hero {
    background: url('https://via.placeholder.com/1200x400') center/cover no-repeat; /* Placeholder background */
    text-align: center;
    padding: 6rem 2rem;
    color: #fff;
    background-color: #34495e; /* Fallback color */
}

.hero h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
}

.btn {
    background: #e74c3c; /* Red button */
    color: #fff;
    padding: 0.8rem 1.5rem;
    text-decoration: none;
    border-radius: 5px;
    font-size: 1rem;
    transition: background 0.3s;
}

.btn:hover {
    background: #c0392b; /* Darker red on hover */
}

/* Filter Section */
.filter {
    padding: 2rem;
    text-align: center;
    background: #fff;
    margin: 1rem 0;
}

.filter h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

.filter-options {
    display: flex;
    justify-content: center;
    gap: 1rem;
}

.filter-options select, .filter-options input {
    padding: 0.5rem;
    font-size: 1rem;
    border: 1px solid #ddd;
    border-radius: 5px;
    outline: none;
}

.filter-options input {
    width: 200px;
}

/* Products Section */
.products {
    padding: 3rem 2rem;
    text-align: center;
}

.products h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
}

.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Responsive grid */
    gap: 2rem;
}

.product-card {
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 10px;
    padding: 1rem;
    text-align: center;
    transition: transform 0.3s, box-shadow 0.3s; /* Smooth hover effects */
}

.product-card:hover {
    transform: translateY(-5px); /* Lift effect */
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1); /* Shadow on hover */
}

.product-card img {
    max-width: 100%;
    border-radius: 10px;
    margin-bottom: 0.5rem;
}

.product-card h3 {
    font-size: 1.2rem;
    margin: 0.5rem 0;
}

.product-card .price {
    color: #e74c3c; /* Red price text */
    font-size: 1.1rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
}

.product-card .description {
    font-size: 0.9rem;
    color: #666;
    margin-bottom: 1rem;
}

.add-to-cart {
    background: #2ecc71; /* Green button */
    color: #fff;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s;
}

.add-to-cart:hover {
    background: #27ae60; /* Darker green on hover */
}

/* Footer Styles */
footer {
    background: #2c3e50;
    color: #fff;
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
}

.footer-links a {
    color: #fff;
    text-decoration: none;
    margin: 0 0.5rem;
}

.footer-links a:hover {
    color: #f1c40f; /* Yellow hover effect */
}

/* Responsive Design */
@media (max-width: 768px) {
    header {
        flex-direction: column; /* Stack header items vertically */
        gap: 1rem;
    }

    nav ul {
        flex-direction: column; /* Stack nav items vertically */
        text-align: center;
    }

    .hero {
        padding: 4rem 1rem; /* Reduce padding on smaller screens */
    }

    .hero h2 {
        font-size: 2rem;
    }

    .hero p {
        font-size: 1rem;
    }

    .filter-options {
        flex-direction: column; /* Stack filter options vertically */
        align-items: center;
    }

    .filter-options input {
        width: 100%; /* Full-width search bar */
    }
}# Ecommerce-Website
