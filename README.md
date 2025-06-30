<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HYBRID PLC TRANSPORT & CAR RENT SERVICES</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Alpine.js for interactivity -->
    <script src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>

    <style>
        /* Custom styles */
        body {
            font-family: 'Inter', sans-serif;
        }
        .hero-section {
            background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://placehold.co/1920x1080/334155/e2e8f0?text=Modern+Hybrid+Cars');
            background-size: cover;
            background-position: center;
        }
        .testimonial-bg {
             background-color: #f8fafc;
        }
        .fade-in {
            animation: fadeIn 1s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .chat-bubble-user {
            background-color: #d1fae5; /* A light green */
            color: #064e3b;
        }
        .chat-bubble-ai {
            background-color: #e5e7eb; /* A light gray */
            color: #1f2937;
        }
    </style>
</head>
<body class="bg-white text-gray-800">

    <!-- Header -->
    <header class="bg-white shadow-md sticky top-0 z-50" x-data="{ mobileMenuOpen: false }">
        <nav class="container mx-auto px-6 py-3 flex justify-between items-center">
            <a href="#" class="text-xl font-bold text-gray-900">
                <div class="flex flex-col">
                    <span class="text-emerald-600 text-2xl">HYBRID</span><span class="text-2xl">PLC</span>
                    <span class="text-xs text-gray-500 font-medium">TRANSPORT & CAR RENT SERVICES</span>
                </div>
            </a>
            
            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center space-x-6">
                <a href="#home" class="text-gray-600 hover:text-emerald-600 transition duration-300">Home</a>
                <a href="#fleet" class="text-gray-600 hover:text-emerald-600 transition duration-300">Our Fleet</a>
                <a href="#services" class="text-gray-600 hover:text-emerald-600 transition duration-300">Services</a>
                <a href="#about" class="text-gray-600 hover:text-emerald-600 transition duration-300">About Us</a>
                <a href="#contact" class="text-gray-600 hover:text-emerald-600 transition duration-300">Contact</a>
            </div>
            
            <a href="#booking" class="hidden md:block bg-emerald-600 text-white px-5 py-2 rounded-full hover:bg-emerald-700 transition duration-300 shadow-lg">Book Now</a>

            <!-- Mobile Menu Button -->
            <div class="md:hidden">
                <button @click="mobileMenuOpen = !mobileMenuOpen" class="text-gray-800 focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                    </svg>
                </button>
            </div>
        </nav>

        <!-- Mobile Menu -->
        <div x-show="mobileMenuOpen" x-transition class="md:hidden bg-white border-t">
            <a href="#home" @click="mobileMenuOpen = false" class="block px-6 py-3 text-gray-600 hover:bg-gray-50 hover:text-emerald-600">Home</a>
            <a href="#fleet" @click="mobileMenuOpen = false" class="block px-6 py-3 text-gray-600 hover:bg-gray-50 hover:text-emerald-600">Our Fleet</a>
            <a href="#services" @click="mobileMenuOpen = false" class="block px-6 py-3 text-gray-600 hover:bg-gray-50 hover:text-emerald-600">Services</a>
            <a href="#about" @click="mobileMenuOpen = false" class="block px-6 py-3 text-gray-600 hover:bg-gray-50 hover:text-emerald-600">About Us</a>
            <a href="#contact" @click="mobileMenuOpen = false" class="block px-6 py-3 text-gray-600 hover:bg-gray-50 hover:text-emerald-600">Contact</a>
            <div class="px-6 py-4">
                 <a href="#booking" @click="mobileMenuOpen = false" class="block w-full text-center bg-emerald-600 text-white px-5 py-3 rounded-full hover:bg-emerald-700 transition duration-300 shadow-lg">Book Now</a>
            </div>
        </div>
    </header>

    <main>
        <!-- Main content of the website -->
        <!-- Hero Section -->
        <section id="home" class="hero-section text-white h-[80vh] flex items-center justify-center fade-in">
            <div class="text-center px-4">
                <h1 class="text-4xl md:text-6xl font-bold mb-4">Drive Green, Save More</h1>
                <p class="text-lg md:text-xl mb-8 max-w-2xl mx-auto">Experience the future of driving with our premium fleet of hybrid vehicles. Your perfect, eco-friendly ride is just a click away.</p>
                <a href="#booking" class="bg-emerald-600 text-white px-8 py-4 rounded-full text-lg font-semibold hover:bg-emerald-700 transition duration-300 shadow-xl">Explore Our Cars</a>
            </div>
        </section>

        <!-- Booking Form Section -->
        <section id="booking" class="bg-gray-100 py-12 md:py-20 -mt-20 relative z-10 mx-4 md:mx-auto max-w-6xl rounded-xl shadow-2xl">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-8 text-gray-900">Find Your Next Ride</h2>
                <form class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-6 items-end">
                    <div class="space-y-2">
                        <label for="pickup-location" class="font-medium text-gray-700">Pick-up Location</label>
                        <input type="text" id="pickup-location" placeholder="Addis Ababa, Bole Airport..." class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <div class="space-y-2">
                        <label for="pickup-date" class="font-medium text-gray-700">Pick-up Date</label>
                        <input type="date" id="pickup-date" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <div class="space-y-2">
                        <label for="return-date" class="font-medium text-gray-700">Return Date</label>
                        <input type="date" id="return-date" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                    </div>
                    <div class="space-y-2 lg:col-span-1">
                        <label for="car-type" class="font-medium text-gray-700">Car Type</label>
                         <select id="car-type" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                            <option>Any Hybrid</option>
                            <option>Compact</option>
                            <option>SUV</option>
                            <option>Luxury</option>
                        </select>
                    </div>
                    <button type="submit" class="w-full bg-emerald-600 text-white px-6 py-3 rounded-lg font-semibold text-lg hover:bg-emerald-700 transition duration-300 shadow-md md:col-span-2 lg:col-span-1">Search</button>
                </form>
            </div>
        </section>

        <!-- Our Fleet Section -->
        <section id="fleet" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-4xl font-bold text-gray-900">Our Hybrid Fleet</h2>
                    <p class="text-lg text-gray-600 mt-2">A diverse range of vehicles to meet your every need.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Car Card 1 -->
                    <div class="bg-gray-50 rounded-lg shadow-lg overflow-hidden transform hover:-translate-y-2 transition duration-300">
                        <img src="https://placehold.co/600x400/a7f3d0/1e293b?text=Toyota+Prius" alt="Toyota Prius" class="w-full h-56 object-cover">
                        <div class="p-6">
                            <h3 class="text-2xl font-semibold mb-2">Toyota Prius</h3>
                            <p class="text-gray-600 mb-4">The classic choice for efficiency and reliability.</p>
                            <div class="flex justify-between items-center text-sm text-gray-700 mb-4">
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>20+ KML</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 16v-2m8-8h2M4 12H2m15.364 6.364l1.414 1.414M5.222 5.222l1.414 1.414M18.778 5.222l-1.414 1.414M6.636 18.364l-1.414 1.414"></path><circle cx="12" cy="12" r="3"></circle></svg>Automatic</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283-.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>5 Seats</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <p class="text-2xl font-bold text-emerald-600">3000 ETB<span class="text-sm font-normal text-gray-600">/day</span></p>
                                <a href="#booking" class="bg-gray-900 text-white px-5 py-2 rounded-lg hover:bg-gray-700 transition duration-300">Rent Now</a>
                            </div>
                        </div>
                    </div>
                    <!-- Car Card 2 -->
                    <div class="bg-gray-50 rounded-lg shadow-lg overflow-hidden transform hover:-translate-y-2 transition duration-300">
                        <img src="https://placehold.co/600x400/6ee7b7/1e293b?text=Hyundai+Ioniq+5" alt="Hyundai Ioniq 5" class="w-full h-56 object-cover">
                        <div class="p-6">
                            <h3 class="text-2xl font-semibold mb-2">Hyundai Ioniq 5</h3>
                            <p class="text-gray-600 mb-4">Sleek, futuristic design with impressive electric range.</p>
                             <div class="flex justify-between items-center text-sm text-gray-700 mb-4">
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>450+ KM Range</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 16v-2m8-8h2M4 12H2m15.364 6.364l1.414 1.414M5.222 5.222l1.414 1.414M18.778 5.222l-1.414 1.414M6.636 18.364l-1.414 1.414"></path><circle cx="12" cy="12" r="3"></circle></svg>Automatic</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283-.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>5 Seats</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <p class="text-2xl font-bold text-emerald-600">4000 ETB<span class="text-sm font-normal text-gray-600">/day</span></p>
                                <a href="#booking" class="bg-gray-900 text-white px-5 py-2 rounded-lg hover:bg-gray-700 transition duration-300">Rent Now</a>
                            </div>
                        </div>
                    </div>
                    <!-- Car Card 3 -->
                    <div class="bg-gray-50 rounded-lg shadow-lg overflow-hidden transform hover:-translate-y-2 transition duration-300">
                        <img src="https://placehold.co/600x400/34d399/1e293b?text=Lexus+NX+Hybrid" alt="Lexus NX Hybrid" class="w-full h-56 object-cover">
                        <div class="p-6">
                            <h3 class="text-2xl font-semibold mb-2">Lexus NX Hybrid</h3>
                            <p class="text-gray-600 mb-4">Luxury meets efficiency in this premium hybrid SUV.</p>
                            <div class="flex justify-between items-center text-sm text-gray-700 mb-4">
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>16+ KML</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6V4m0 16v-2m8-8h2M4 12H2m15.364 6.364l1.414 1.414M5.222 5.222l1.414 1.414M18.778 5.222l-1.414 1.414M6.636 18.364l-1.414 1.414"></path><circle cx="12" cy="12" r="3"></circle></svg>Automatic</span>
                                <span class="flex items-center"><svg class="w-5 h-5 mr-1 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283-.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>5 Seats</span>
                            </div>
                            <div class="flex justify-between items-center">
                                <p class="text-2xl font-bold text-emerald-600">5000 ETB<span class="text-sm font-normal text-gray-600">/day</span></p>
                                <a href="#booking" class="bg-gray-900 text-white px-5 py-2 rounded-lg hover:bg-gray-700 transition duration-300">Rent Now</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="bg-gray-100 py-20">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-4xl font-bold text-gray-900">Why Rent With Us?</h2>
                    <p class="text-lg text-gray-600 mt-2">Unmatched service and benefits for a seamless rental experience.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="text-center p-6">
                        <div class="flex items-center justify-center h-16 w-16 rounded-full bg-emerald-100 text-emerald-600 mx-auto mb-4">
                           <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Eco-Friendly Fleet</h3>
                        <p class="text-gray-600">Reduce your carbon footprint with our modern, fuel-efficient hybrid vehicles.</p>
                    </div>
                    <div class="text-center p-6">
                        <div class="flex items-center justify-center h-16 w-16 rounded-full bg-emerald-100 text-emerald-600 mx-auto mb-4">
                           <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v.01"></path></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Transparent Pricing</h3>
                        <p class="text-gray-600">No hidden fees. The price you see is the price you pay.</p>
                    </div>
                    <div class="text-center p-6">
                        <div class="flex items-center justify-center h-16 w-16 rounded-full bg-emerald-100 text-emerald-600 mx-auto mb-4">
                           <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M7 21h10a2 2 0 002-2V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2z"></path></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Easy Online Booking</h3>
                        <p class="text-gray-600">Reserve your car in just a few clicks with our simple booking system.</p>
                    </div>
                    <div class="text-center p-6">
                        <div class="flex items-center justify-center h-16 w-16 rounded-full bg-emerald-100 text-emerald-600 mx-auto mb-4">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                # Hybridplcet.com
