<!DOCTYPE html>
<html lang="en">
<head>
    <base target="_self">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Al Najm Furniture Ltd - Premium Furniture & Home Accessories</title>
    <meta name="description" content="Al Najm Furniture Ltd offers premium furniture and home accessories. Shop our curated collection of modern, classic, and luxury furniture pieces for every room in your home.">
    <meta name="keywords" content="furniture, home accessories, luxury furniture, modern furniture, classic furniture, Al Najm Furniture">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: "#1a365d",
                        secondary: "#2d3748",
                        accent: "#c53030",
                        "wood-brown": "#8B4513",
                        "cream": "#F5F5DC",
                        "gold": "#D4AF37"
                    },
                    fontFamily: {
                        'display': ['Playfair Display', 'serif'],
                        'body': ['Inter', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        .admin-panel {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
    </style>
</head>
<body class="min-h-screen bg-gray-50 font-body">
    <!-- Header & Navigation -->
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <!-- Logo -->
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 bg-primary rounded-full flex items-center justify-center">
                        <i class="fas fa-star text-white text-xl"></i>
                    </div>
                    <div>
                        <h1 class="text-2xl font-bold text-primary font-display">Al Najm Furniture</h1>
                        <p class="text-xs text-gray-500">Ltd.</p>
                    </div>
                </div>

                <!-- Desktop Navigation -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('home')">Home</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('products')">Products</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('categories')">Categories</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('about')">About Us</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('contact')">Contact</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium transition-colors" onclick="navigateTo('admin')">Admin Panel</a>
                </nav>

                <!-- Mobile Menu Button -->
                <button id="mobileMenuBtn" class="md:hidden text-gray-700">
                    <i class="fas fa-bars text-2xl"></i>
                </button>

                <!-- Cart & User -->
                <div class="flex items-center space-x-4">
                    <button class="relative text-gray-700 hover:text-primary">
                        <i class="fas fa-shopping-cart text-xl"></i>
                        <span class="absolute -top-2 -right-2 bg-accent text-white text-xs rounded-full w-5 h-5 flex items-center justify-center" id="cartCount">0</span>
                    </button>
                    <button class="text-gray-700 hover:text-primary">
                        <i class="fas fa-user text-xl"></i>
                    </button>
                </div>
            </div>

            <!-- Mobile Navigation -->
            <div id="mobileMenu" class="hidden md:hidden py-4 border-t">
                <div class="flex flex-col space-y-3">
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('home')">Home</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('products')">Products</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('categories')">Categories</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('about')">About Us</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('contact')">Contact</a>
                    <a href="#" class="text-gray-700 hover:text-primary font-medium py-2" onclick="navigateTo('admin')">Admin Panel</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content Area -->
    <main id="contentArea" class="container mx-auto px-4 py-8">
        <!-- Home Section -->
        <section id="home" class="content-section">
            <!-- Hero Section -->
            <div class="relative h-96 rounded-xl overflow-hidden mb-12">
                <img src="https://picsum.photos/1200/400?random=1" alt="Luxury living room furniture showcase" class="w-full h-full object-cover" loading="lazy">
                <div class="absolute inset-0 bg-black bg-opacity-40 flex items-center">
                    <div class="text-white px-8 max-w-2xl">
                        <h2 class="text-4xl md:text-5xl font-bold font-display mb-4">Elevate Your Living Space</h2>
                        <p class="text-xl mb-6">Premium furniture and accessories that transform houses into homes</p>
                        <button onclick="navigateTo('products')" class="bg-primary hover:bg-secondary text-white px-8 py-3 rounded-lg font-semibold transition-colors">Shop Now</button>
                    </div>
                </div>
            </div>

            <!-- Featured Categories -->
            <div class="mb-12">
                <h2 class="text-3xl font-bold text-primary mb-8 font-display text-center">Shop by Category</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <div class="bg-white rounded-xl shadow-md overflow-hidden">
                        <img src="https://picsum.photos/400/250?random=2" alt="Living room furniture" class="w-full h-48 object-cover" loading="lazy">
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">Living Room</h3>
                            <p class="text-gray-600 mb-4">Sofas, chairs, tables, and entertainment units</p>
                            <button onclick="filterCategory('living-room')" class="text-primary hover:text-secondary font-semibold">Browse Collection →</button>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl shadow-md overflow-hidden">
                        <img src="https://picsum.photos/400/250?random=3" alt="Bedroom furniture" class="w-full h-48 object-cover" loading="lazy">
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">Bedroom</h3>
                            <p class="text-gray-600 mb-4">Beds, wardrobes, dressers, and nightstands</p>
                            <button onclick="filterCategory('bedroom')" class="text-primary hover:text-secondary font-semibold">Browse Collection →</button>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl shadow-md overflow-hidden">
                        <img src="https://picsum.photos/400/250?random=4" alt="Dining furniture" class="w-full h-48 object-cover" loading="lazy">
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-2">Dining</h3>
                            <p class="text-gray-600 mb-4">Dining tables, chairs, buffets, and serving carts</p>
                            <button onclick="filterCategory('dining')" class="text-primary hover:text-secondary font-semibold">Browse Collection →</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Featured Products -->
            <div class="mb-12">
                <div class="flex justify-between items-center mb-8">
                    <h2 class="text-3xl font-bold text-primary font-display">Featured Products</h2>
                    <button onclick="navigateTo('products')" class="text-primary hover:text-secondary font-semibold">View All →</button>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6" id="featuredProducts">
                    <!-- Featured products will be loaded here -->
                </div>
            </div>
        </section>

        <!-- Products Section -->
        <section id="products" class="content-section hidden">
            <div class="mb-8">
                <h2 class="text-3xl font-bold text-primary mb-4 font-display">All Products</h2>
                <div class="flex flex-wrap gap-4 mb-6">
                    <button onclick="filterCategory('all')" class="px-4 py-2 bg-primary text-white rounded-lg">All</button>
                    <button onclick="filterCategory('living-room')" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg">Living Room</button>
                    <button onclick="filterCategory('bedroom')" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg">Bedroom</button>
                    <button onclick="filterCategory('dining')" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg">Dining</button>
                    <button onclick="filterCategory('office')" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg">Office</button>
                    <button onclick="filterCategory('accessories')" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded-lg">Accessories</button>
                </div>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6" id="allProducts">
                <!-- All products will be loaded here -->
            </div>
        </section>

        <!-- Categories Section -->
        <section id="categories" class="content-section hidden">
            <h2 class="text-3xl font-bold text-primary mb-8 font-display text-center">Product Categories</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" id="categoriesGrid">
                <!-- Categories will be loaded here -->
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="content-section hidden">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-3xl font-bold text-primary mb-6 font-display text-center">About Al Najm Furniture Ltd</h2>
                <div class="bg-white rounded-xl shadow-md p-8">
                    <div class="mb-8">
                        <img src="https://picsum.photos/800/400?random=5" alt="Our showroom" class="w-full rounded-lg mb-6" loading="lazy">
                        <h3 class="text-2xl font-bold mb-4 text-secondary">Our Story</h3>
                        <p class="text-gray-700 mb-4">Founded in 2005, Al Najm Furniture Ltd has been at the forefront of furniture design and manufacturing in the region. Our name "Al Najm" (The Star) reflects our commitment to providing star-quality furniture that illuminates homes with elegance and comfort.</p>
                        <p class="text-gray-700 mb-4">We specialize in crafting premium furniture pieces that blend traditional craftsmanship with modern design sensibilities. Each piece in our collection is carefully curated to ensure it meets our high standards of quality, durability, and aesthetic appeal.</p>
                    </div>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
                        <div class="text-center p-4">
                            <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fas fa-award text-white text-2xl"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-2">Premium Quality</h4>
                            <p class="text-gray-600">Using only the finest materials and craftsmanship</p>
                        </div>
                        <div class="text-center p-4">
                            <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fas fa-truck text-white text-2xl"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-2">Free Delivery</h4>
                            <p class="text-gray-600">Free delivery on all orders above $500</p>
                        </div>
                        <div class="text-center p-4">
                            <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4">
                                <i class="fas fa-shield-alt text-white text-2xl"></i>
                            </div>
                            <h4 class="text-xl font-bold mb-2">5-Year Warranty</h4>
                            <p class="text-gray-600">Comprehensive warranty on all our products</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="content-section hidden">
            <div class="max-w-4xl mx-auto">
                <h2 class="text-3xl font-bold text-primary mb-8 font-display text-center">Contact Us</h2>
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                    <div class="bg-white rounded-xl shadow-md p-8">
                        <h3 class="text-2xl font-bold mb-6 text-secondary">Get in Touch</h3>
                        <form id="contactForm" class="space-y-4">
                            <div>
                                <label class="block text-gray-700 mb-2">Full Name</label>
                                <input type="text" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-primary" required>
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Email Address</label>
                                <input type="email" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-primary" required>
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Phone Number</label>
                                <input type="tel" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-primary">
                            </div>
                            <div>
                                <label class="block text-gray-700 mb-2">Message</label>
                                <textarea rows="4" class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-primary" required></textarea>
                            </div>
                            <button type="submit" class="w-full bg-primary hover:bg-secondary text-white py-3 rounded-lg font-semibold transition-colors">Send Message</button>
                        </form>
                    </div>
                    
                    <div class="space-y-6">
                        <div class="bg-white rounded-xl shadow-md p-6">
                            <h4 class="text-xl font-bold mb-4 text-secondary">Contact Information</h4>
                            <div class="space-y-4">
                                <div class="flex items-center">
                                    <i class="fas fa-map-marker-alt text-primary text-xl mr-4"></i>
                                    <div>
                                        <p class="font-semibold">Address</p>
                                        <p class="text-gray-600">123 Furniture Street, Design District</p>
                                        <p class="text-gray-600">Dubai, UAE</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <i class="fas fa-phone text-primary text-xl mr-4"></i>
                                    <div>
                                        <p class="font-semibold">Phone</p>
                                        <p class="text-gray-600">+971 4 123 4567</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <i class="fas fa-envelope text-primary text-xl mr-4"></i>
                                    <div>
                                        <p class="font-semibold">Email</p>
                                        <p class="text-gray-600">info@alnajmfurniture.com</p>
                                    </div>
                                </div>
                                <div class="flex items-center">
                                    <i class="fas fa-clock text-primary text-xl mr-4"></i>
                                    <div>
                                        <p class="font-semibold">Business Hours</p>
                                        <p class="text-gray-600">Sunday - Thursday: 9:00 AM - 8:00 PM</p>
                                        <p class="text-gray-600">Friday - Saturday: 10:00 AM - 6:00 PM</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="bg-white rounded-xl shadow-md p-6">
                            <h4 class="text-xl font-bold mb-4 text-secondary">Follow Us</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 bg-blue-600 text-white rounded-full flex items-center justify-center hover:bg-blue-700">
                                    <i class="fab fa-facebook-f"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-pink-600 text-white rounded-full flex items-center justify-center hover:bg-pink-700">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-blue-400 text-white rounded-full flex items-center justify-center hover:bg-blue-500">
                                    <i class="fab fa-twitter"></i>
                                </a>
                                <a href="#" class="w-10 h-10 bg-red-600 text-white rounded-full flex items-center justify-center hover:bg-red-700">
                                    <i class="fab fa-youtube"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Admin Panel Section -->
        <section id="admin" class="content-section hidden">
            <div class="max-w-6xl mx-auto">
                <h2 class="text-3xl font-bold text-primary mb-8 font-display text-center">Admin Panel</h2>
                
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <!-- Add New Product -->
                    <div class="lg:col-span-2">
                        <div class="bg-white rounded-xl shadow-md p-8 admin-panel text-white">
                            <h3 class="text-2xl font-bold mb-6">Add New Product</h3>
                            <form id="addProductForm" class="space-y-4">
                                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                    <div>
                                        <label class="block mb-2">Product Name</label>
                                        <input type="text" id="productName" class="w-full px-4 py-2 rounded-lg text-gray-800" required>
                                    </div>
                                    <div>
                                        <label class="block mb-2">Price ($)</label>
                                        <input type="number" id="productPrice" class="w-full px-4 py-2 rounded-lg text-gray-800" step="0.01" required>
                                    </div>
                                </div>
                                
                                <div>
                                    <label class="block mb-2">Category</label>
                                    <select id="productCategory" class="w-full px-4 py-2 rounded-lg text-gray-800" required>
                                        <option value="">Select Category</option>
                                        <option value="living-room">Living Room</option>
                                        <option value="bedroom">Bedroom</option>
                                        <option value="dining">Dining</option>
                                        <option value="office">Office</option>
                                        <option value="accessories">Accessories</option>
                                    </select>
                                </div>
                                
                                <div>
                                    <label class="block mb-2">Description</label>
                                    <textarea id="productDescription" rows="3" class="w-full px-4 py-2 rounded-lg text-gray-800" required></textarea>
                                </div>
                                
                                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                    <div>
                                        <label class="block mb-2">Stock Quantity</label>
                                        <input type="number" id="productStock" class="w-full px-4 py-2 rounded-lg text-gray-800" required>
                                    </div>
                                    <div>
                                        <label class="block mb-2">Image URL</label>
                                        <input type="text" id="productImage" class="w-full px-4 py-2 rounded-lg text-gray-800" value="https://picsum.photos/400/300?random=" required>
                                    </div>
                                </div>
                                
                                <div class="flex space-x-4 pt-4">
                                    <button type="submit" class="bg-white text-purple-700 hover:bg-gray-100 px-6 py-3 rounded-lg font-semibold transition-colors">Add Product</button>
                                    <button type="button" onclick="clearProductForm()" class="bg-gray-200 text-gray-700 hover:bg-gray-300 px-6 py-3 rounded-lg font-semibold transition-colors">Clear Form</button>
                                </div>
                            </form>
                        </div>
                    </div>
                    
                    <!-- Product Management -->
                    <div class="bg-white rounded-xl shadow-md p-6">
                        <h3 class="text-xl font-bold mb-6 text-secondary">Product Management</h3>
                        <div class="space-y-4">
                            <div class="p-4 bg-gray-50 rounded-lg">
                                <h4 class="font-semibold mb-2">Total Products</h4>
                                <p class="text-3xl font-bold text-primary" id="totalProducts">0</p>
                            </div>
                            <div class="p-4 bg-gray-50 rounded-lg">
                                <h4 class="font-semibold mb-2">Categories</h4>
                                <p class="text-3xl font-bold text-primary" id="totalCategories">0</p>
                            </div>
                            <div class="p-4 bg-gray-50 rounded-lg">
                                <h4 class="font-semibold mb-2">Total Value</h4>
                                <p class="text-3xl font-bold text-primary" id="totalValue">$0</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product List -->
                <div class="mt-8">
                    <h3 class="text-2xl font-bold mb-6 text-secondary">Current Products</h3>
                    <div class="bg-white rounded-xl shadow-md overflow-hidden">
                        <div class="overflow-x-auto">
                            <table class="w-full">
                                <thead class="bg-gray-50">
                                    <tr>
                                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Product</th>
                                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Category</th>
                                        <th class="px6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Price</th>
                                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Stock</th>
                                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Actions</th>
                                    </tr>
                                </thead>
                                <tbody class="divide-y divide-gray-200" id="productTableBody">
                                    <!-- Product rows will be loaded here -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-primary text-white mt-12">
        <div class="container mx-auto px-4 py-12">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-white rounded-full flex items-center justify-center">
                            <i class="fas fa-star text-primary text-xl"></i>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold font-display">Al Najm Furniture</h3>
                            <p class="text-sm text-gray-300">Ltd.</p>
                        </div>
                    </div>
                    <p class="text-gray-300">Premium furniture and accessories for your dream home.</p>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors" onclick="navigateTo('home')">Home</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors" onclick="navigateTo('products')">Products</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors" onclick="navigateTo('categories')">Categories</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors" onclick="navigateTo('about')">About Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Customer Service</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors" onclick="navigateTo('contact')">Contact Us</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors">Shipping Policy</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors">Return Policy</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white transition-colors">FAQ</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-bold mb-4">Newsletter</h4>
                    <p class="text-gray-300 mb-4">Subscribe for updates and exclusive offers</p>
                    <div class="flex">
                        <input type="email" placeholder="Your email" class="flex-grow px-4 py-2 rounded-l-lg text-gray-800">
                        <button class="bg-accent hover:bg-red-700 px-4 py-2 rounded-r-lg font-semibold">Subscribe</button>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-300">
                <p>&copy; 2024 Al Najm Furniture Ltd. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Cookie Consent -->
    <div id="cookieConsent" class="fixed bottom-0 left-0 right-0 bg-gray-800 text-white p-4 hidden">
        <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
            <p class="mb-4 md:mb-0">We use cookies to enhance your experience. By continuing to visit this site you agree to our use of cookies.</p>
            <div class="flex space-x-4">
                <button onclick="acceptCookies()" class="bg-primary hover:bg-secondary px-4 py-2 rounded-lg">Accept</button>
                <button onclick="declineCookies()" class="bg-gray-700 hover:bg-gray-600 px-4 py-2 rounded-lg">Decline</button>
            </div>
        </div>
    </div>

    <script>
        // Define data at the beginning
        let products = [
            {
                "id": 1,
                "name": "Luxury Leather Sofa",
                "category": "living-room",
                "price": 1299.99,
                "description": "Premium genuine leather sofa with mahogany wood frame",
                "image": "https://picsum.photos/400/300?random=6",
                "stock": 15,
                "featured": true
            },
            {
                "id": 2,
                "name": "King Size Bed Frame",
                "category": "bedroom",
                "price": 899.99,
                "description": "Solid oak king size bed with storage drawers",
                "image": "https://picsum.photos/400/300?random=7",
                "stock": 8,
                "featured": true
            },
            {
                "id": 3,
                "name": "Dining Table Set",
                "category": "dining",
                "price": 1499.99,
                "description": "6-seater dining table with matching chairs",
                "image": "https://picsum.photos/400/300?random=8",
                "stock": 12,
                "featured": true
            },
            {
                "id": 4,
                "name": "Executive Office Desk",
                "category": "office",
                "price": 699.99,
                "description": "Modern executive desk with cable management",
                "image": "https://picsum.photos/400/300?random=9",
                "stock": 20,
                "featured": false
            },
            {
                "id": 5,
                "name": "Decorative Wall Mirror",
                "category": "accessories",
                "price": 249.99,
                "description": "Ornate gold-finished wall mirror",
                "image": "https://picsum.photos/400/300?random=10",
                "stock": 25,
                "featured": false
            },
            {
                "id": 6,
                "name": "Coffee Table",
                "category": "living-room",
                "price": 349.99,
                "description": "Glass top coffee table with metal legs",
                "image": "https://picsum.photos/400/300?random=11",
                "stock": 18,
                "featured": false
            },
            {
                "id": 7,
                "name": "Wardrobe Cabinet",
                "category": "bedroom",
                "price": 799.99,
                "description": "3-door wardrobe with mirror and drawers",
                "image": "https://picsum.photos/400/300?random=12",
                "stock": 10,
                "featured": false
            },
            {
                "id": 8,
                "name": "Bar Stools Set",
                "category": "dining",
                "price": 299.99,
                "description": "Set of 2 adjustable height bar stools",
                "image": "https://picsum.photos/400/300?random=13",
                "stock": 30,
                "featured": false
            }
        ];

        let categories = [
            { "id": "living-room", "name": "Living Room", "count": 2, "image": "https://picsum.photos/400/250?random=14" },
            { "id": "bedroom", "name": "Bedroom", "count": 2, "image": "https://picsum.photos/400/250?random=15" },
            { "id": "dining", "name": "Dining", "count": 2, "image": "https://picsum.photos/400/250?random=16" },
            { "id": "office", "name": "Office", "count": 1, "image": "https://picsum.photos/400/250?random=17" },
            { "id": "accessories", "name": "Accessories", "count": 1, "image": "https://picsum.photos/400/250?random=18" }
        ];

        let cart = [];
        let currentProductId = products.length;

        // DOM Elements
        const mobileMenuBtn = document.getElementById("mobileMenuBtn");
        const mobileMenu = document.getElementById("mobileMenu");
        const contentArea = document.getElementById("contentArea");
        const featuredProducts = document.getElementById("featuredProducts");
        const allProducts = document.getElementById("allProducts");
        const categoriesGrid = document.getElementById("categoriesGrid");
        const productTableBody = document.getElementById("productTableBody");
        const totalProducts = document.getElementById("totalProducts");
        const totalCategories = document.getElementById("totalCategories");
        const totalValue = document.getElementById("totalValue");
        const cartCount = document.getElementById("cartCount");
        const cookieConsent = document.getElementById("cookieConsent");

        // Initialize
        document.addEventListener("DOMContentLoaded", function() {
            initializeApp();
            showCookieConsent();
        });

        function initializeApp() {
            // Mobile menu toggle
            mobileMenuBtn.addEventListener("click", function() {
                mobileMenu.classList.toggle("hidden");
            });

            // Load initial content
            loadFeaturedProducts();
            loadAllProducts();
            loadCategories();
            updateAdminStats();
            loadProductTable();

            // Form submissions
            document.getElementById("contactForm").addEventListener("submit", function(e) {
                e.preventDefault();
                alert("Thank you for your message! We will get back to you soon.");
                this.reset();
            });

            document.getElementById("addProductForm").addEventListener("submit", function(e) {
                e.preventDefault();
                addNewProduct();
            });

            // Initialize navigation
            navigateTo("home");
        }

        // Navigation function
        function navigateTo(section) {
            // Hide all sections
            const sections = document.querySelectorAll(".content-section");
            sections.forEach(section => section.classList.add("hidden"));
            
            // Show selected section
            document.getElementById(section).classList.remove("hidden");
            
            // Close mobile menu if open
            mobileMenu.classList.add("hidden");
            
            // Update active navigation
            updateActiveNav(section);
        }

        function updateActiveNav(section) {
            const navLinks = document.querySelectorAll("nav a, #mobileMenu a");
            navLinks.forEach(link => {
                link.classList.remove("text-primary", "font-bold");
                link.classList.add("text-gray-700");
            });
            
            // Find and highlight active link
            const activeLink = Array.from(navLinks).find(link => 
                link.getAttribute("onclick") && link.getAttribute("onclick").includes(section)
            );
            if (activeLink) {
                activeLink.classList.remove("text-gray-700");
                activeLink.classList.add("text-primary", "font-bold");
            }
        }

        // Product functions
        function loadFeaturedProducts() {
            featuredProducts.innerHTML = "";
            const featured = products.filter(product => product.featured);
            
            featured.forEach(product => {
                const productCard = createProductCard(product);
                featuredProducts.appendChild(productCard);
            });
        }

        function loadAllProducts() {
            allProducts.innerHTML = "";
            products.forEach(product => {
                const productCard = createProductCard(product);
                allProducts.appendChild(productCard);
            });
        }

        function createProductCard(product) {
            const card = document.createElement("div");
            card.className = "bg-white rounded-xl shadow-md overflow-hidden product-card transition-all duration-300";
            card.innerHTML = `
                <div class="relative">
                    <img src="${product.image}" alt="${product.name}" class="w-full h-48 object-cover" loading="lazy">
                    ${product.featured ? '<span class="absolute top-2 left-2 bg-accent text-white px-2 py-1 rounded text-xs font-semibold">Featured</span>' : ''}
                </div>
                <div class="p-4">
                    <div class="flex justify-between items-start mb-2">
                        <h3 class="font-bold text-lg text-gray-800">${product.name}</h3>
                        <span class="text-primary font-bold text-xl">$${product.price.toFixed(2)}</span>
                    </div>
                    <p class="text-gray-600 text-sm mb-4">${product.description}</p>
                    <div class="flex justify-between items-center">
                        <span class="text-sm ${product.stock > 10 ? "text-green-600" : product.stock > 0 ? "text-yellow-600" : "text-red-600"}">
                            ${product.stock > 10 ? "In Stock" : product.stock > 0 ? "Low Stock" : "Out of Stock"}
                        </span>
                        <div class="flex space-x-2">
                            <button onclick="addToCart(${product.id})" class="bg-primary hover:bg-secondary text-white px-4 py-2 rounded-lg text-sm font-semibold transition-colors">
                                <i class="fas fa-cart-plus mr-1"></i> Add
                            </button>
                            <button onclick="viewProduct(${product.id})" class="border border-primary text-primary hover:bg-primary hover:text-white px-4 py-2 rounded-lg text-sm font-semibold transition-colors">
                                View
                            </button>
                        </div>
                    </div>
                </div>
            `;
            return card;
        }

        function filterCategory(category) {
            navigateTo("products");
            if (category === "all") {
                loadAllProducts();
            } else {
                allProducts.innerHTML = "";
                const filtered = products.filter(product => product.category === category);
                filtered.forEach(product => {
                    const productCard = createProductCard(product);
                    allProducts.appendChild(productCard);
                });
            }
        }

        function loadCategories() {
            categoriesGrid.innerHTML = "";
            categories.forEach(category => {
                const categoryCard = document.createElement("div");
                categoryCard.className = "bg-white rounded-xl shadow-md overflow-hidden";
                categoryCard.innerHTML = `
                    <img src="${category.image}" alt="${category.name}" class="w-full h-48 object-cover" loading="lazy">
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">${category.name}</h3>
                        <p class="text-gray-600 mb-4">${category.count} products available</p>
                        <button onclick="filterCategory('${category.id}')" class="text-primary hover:text-secondary font-semibold">
                            Browse Collection →
                        </button>
                    </div>
                `;
                categoriesGrid.appendChild(categoryCard);
            });
        }

        // Cart functions
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            if (product && product.stock > 0) {
                cart.push(product);
                updateCartCount();
                alert("${product.name} added to cart!");
            } else {
                alert("Product is out of stock!");
            }
        }

        function updateCartCount() {
            cartCount.textContent = cart.length;
        }

        function viewProduct(productId) {
            const product = products.find(p => p.id === productId);
            if (product) {
                alert("Product Details:\n\nName: ${product.name}\nPrice: $${product.price.toFixed(2)}\nCategory: ${product.category}\nDescription: ${product.description}\nStock: ${product.stock} units");
            }
        }

        // Admin functions
        function addNewProduct() {
            const name = document.getElementById("productName").value;
            const price = parseFloat(document.getElementById("productPrice").value);
            const category = document.getElementById("productCategory").value;
            const description = document.getElementById("productDescription").value;
            const stock = parseInt(document.getElementById("productStock").value);
            const image = document.getElementById("productImage").value;
            
            if (!name || !price || !category || !description || !stock || !image) {
                alert("Please fill in all fields!");
                return;
            }
            
            currentProductId++;
            const newProduct = {
                id: currentProductId,
                name: name,
                category: category,
                price: price,
                description: description,
                image: image + currentProductId,
                stock: stock,
                featured: false
            };
            
            products.push(newProduct);
            
            // Update categories count
            const categoryIndex = categories.findIndex(c => c.id === category);
            if (categoryIndex !== -1) {
                categories[categoryIndex].count++;
            }
            
            // Update UI
            loadAllProducts();
            loadFeaturedProducts();
            loadCategories();
            updateAdminStats();
            loadProductTable();
            
            // Clear form
            clearProductForm();
            
            alert("Product added successfully!");
        }

        function clearProductForm() {
            document.getElementById("addProductForm").reset();
            document.getElementById("productImage").value = "https://picsum.photos/400/300?random=";
        }

        function updateAdminStats() {
            totalProducts.textContent = products.length;
            totalCategories.textContent = categories.length;
            
            const totalValueAmount = products.reduce((sum, product) => sum + (product.price * product.stock), 0);
            totalValue.textContent = "$${totalValueAmount.toFixed(2)}";
        }

        function loadProductTable() {
            productTableBody.innerHTML = "";
            products.forEach(product => {
                const row = document.createElement("tr");
                row.innerHTML = `
                    <td class="px-6 py-4 whitespace-nowrap">
                        <div class="flex items-center">
                            <div class="flex-shrink-0 h-10 w-10">
                                <img class="h-10 w-10 rounded-full object-cover" src="${product.image}" alt="${product.name}">
                            </div>
                            <div class="ml-4">
                                <div class="text-sm font-medium text-gray-900">${product.name}</div>
                            </div>
                        </div>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap">
                        <span class="px-2 inline-flex text-xs leading-5 font-semibold rounded-full bg-blue-100 text-blue-800">
                            ${product.category}
                        </span>
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-900">
                        $${product.price.toFixed(2)}
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap text-sm ${product.stock > 10 ? "text-green-600" : product.stock > 0 ? "text-yellow-600" : "text-red-600"}">
                        ${product.stock}
                    </td>
                    <td class="px-6 py-4 whitespace-nowrap text-sm font-medium">
                        <button onclick="editProduct(${product.id})" class="text-indigo-600 hover:text-indigo-900 mr-3">Edit</button>
                        <button onclick="deleteProduct(${product.id})" class="text-red-600 hover:text-red-900">Delete</button>
                    </td>
                `;
                productTableBody.appendChild(row);
            });
        }

        function editProduct(productId) {
            const product = products.find(p => p.id === productId);
            if (product) {
                document.getElementById("productName").value = product.name;
                document.getElementById("productPrice").value = product.price;
                document.getElementById("productCategory").value = product.category;
                document.getElementById("productDescription").value = product.description;
                document.getElementById("productStock").value = product.stock;
                document.getElementById("productImage").value = product.image.replace(/\\?random=\\d+$/, "");
                
                // Scroll to admin panel
                navigateTo("admin");
                alert("Product loaded for editing. Update the form and click 'Add Product' to save changes.");
            }
        }

        function deleteProduct(productId) {
            if (confirm("Are you sure you want to delete this product?")) {
                const productIndex = products.findIndex(p => p.id === productId);
                if (productIndex !== -1) {
                    const product = products[productIndex];
                    
                    // Update category count
                    const categoryIndex = categories.findIndex(c => c.id === product.category);
                    if (categoryIndex !== -1 && categories[categoryIndex].count > 0) {
                        categories[categoryIndex].count--;
                    }
                    
                    products.splice(productIndex, 1);
                    
                    // Update UI
                    loadAllProducts();
                    loadFeaturedProducts();
                    loadCategories();
                    updateAdminStats();
                    loadProductTable();
                    
                    alert("Product deleted successfully!");
                }
            }
        }

        // Cookie consent
        function showCookieConsent() {
            if (!localStorage.getItem("cookiesAccepted")) {
                setTimeout(() => {
                    cookieConsent.classList.remove("hidden");
                }, 2000);
            }
        }

        function acceptCookies() {
            localStorage.setItem("cookiesAccepted", "true");
            cookieConsent.classList.add("hidden");
        }

        function declineCookies() {
            localStorage.setItem("cookiesAccepted", "false");
            cookieConsent.classList.add("hidden");
        }
    </script>
</body>
</html>
