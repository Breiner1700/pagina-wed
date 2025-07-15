<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LA DISTRIBUIDORA BERMUDEZ LA #01</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .custom-bg {
            background: linear-gradient(90deg, #e63946 0%, #e63946 50%, #22c55e 50%, #22c55e 100%);
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
        .category-tab.active {
            border-bottom: 3px solid #e63946;
            color: #e63946;
        }
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }
        .pulse-animation {
            animation: pulse 2s infinite;
        }
    </style>
</head>
<body class="font-sans bg-gray-50">
    <!-- Header/Navigation -->
    <header class="custom-bg text-white shadow-lg">
        <div class="container mx-auto px-4 py-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center mb-4 md:mb-0">
                    <div class="bg-white rounded-full p-2 mr-4">
                        <i class="fas fa-store text-3xl text-red-600"></i>
                    </div>
                    <h1 class="text-3xl font-bold">
                        <span class="text-white">LA DISTRIBUIDORA</span>
                        <span class="block md:inline-block text-2xl">BERMUDEZ LA #01</span>
                    </h1>
                </div>
                <nav class="w-full md:w-auto">
                    <ul class="flex flex-col md:flex-row space-y-2 md:space-y-0 md:space-x-8 text-lg font-medium">
                        <li><a href="#inicio" class="hover:text-gray-200 transition">Inicio</a></li>
                        <li><a href="#productos" class="hover:text-gray-200 transition">Productos</a></li>
                        <li><a href="#nosotros" class="hover:text-gray-200 transition">Nosotros</a></li>
                        <li><a href="#contacto" class="hover:text-gray-200 transition">Contacto</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="inicio" class="relative overflow-hidden">
        <div class="custom-bg h-64 md:h-96 flex items-center justify-center">
            <div class="text-center px-4 z-10">
                <h2 class="text-4xl md:text-6xl font-bold text-white mb-4">Distribuidora de Confianza</h2>
                <p class="text-xl md:text-2xl text-white mb-8">Los mejores productos al mejor precio</p>
                <a href="#productos" class="bg-white text-red-600 font-bold py-3 px-8 rounded-full hover:bg-gray-100 transition duration-300 inline-block pulse-animation">
                    Ver Productos
                </a>
            </div>
        </div>
        <div class="absolute inset-0 bg-black opacity-20"></div>
    </section>

    <!-- About Section -->
    <section id="nosotros" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Sobre Nosotros</h2>
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img src="https://images.unsplash.com/photo-1606787366852-de2797f1d31d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80" 
                         alt="Distribuidora Bermúdez" 
                         class="rounded-lg shadow-xl w-full h-auto">
                </div>
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-semibold text-green-700 mb-4">Nuestra Historia</h3>
                    <p class="text-gray-600 mb-4">
                        LA DISTRIBUIDORA BERMUDEZ LA #01 es una empresa familiar con más de 20 años de experiencia en la distribución de alimentos y productos de primera necesidad. Nos enorgullecemos de ofrecer productos de la más alta calidad a precios competitivos.
                    </p>
                    <p class="text-gray-600 mb-6">
                        Nuestro compromiso es con la satisfacción total de nuestros clientes, brindando un servicio personalizado y atención de excelencia en cada pedido.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <div class="flex items-center bg-green-50 px-4 py-2 rounded-full">
                            <i class="fas fa-check-circle text-green-600 mr-2"></i>
                            <span class="text-green-800">Calidad garantizada</span>
                        </div>
                        <div class="flex items-center bg-red-50 px-4 py-2 rounded-full">
                            <i class="fas fa-truck text-red-600 mr-2"></i>
                            <span class="text-red-800">Entrega rápida</span>
                        </div>
                        <div class="flex items-center bg-green-50 px-4 py-2 rounded-full">
                            <i class="fas fa-hand-holding-usd text-green-600 mr-2"></i>
                            <span class="text-green-800">Mejores precios</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="productos" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Nuestros Productos</h2>
            
            <!-- Category Tabs -->
            <div class="flex overflow-x-auto pb-2 mb-8 scrollbar-hide">
                <div class="flex space-x-1 mx-auto">
                    <button onclick="filterProducts('todos')" class="category-tab active px-6 py-2 font-medium rounded-t-lg transition">Todos</button>
                    <button onclick="filterProducts('alimentos')" class="category-tab px-6 py-2 font-medium rounded-t-lg transition">Alimentos</button>
                    <button onclick="filterProducts('vegetales')" class="category-tab px-6 py-2 font-medium rounded-t-lg transition">Vegetales</button>
                    <button onclick="filterProducts('otros')" class="category-tab px-6 py-2 font-medium rounded-t-lg transition">Otros</button>
                </div>
            </div>
            
            <!-- Products Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8" id="products-container">
                <!-- Product cards will be inserted here by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Contacto</h2>
            
            <div class="flex flex-col md:flex-row gap-8">
                <!-- Contact Info -->
                <div class="md:w-1/2 bg-green-50 p-8 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-green-700 mb-6">Información de Contacto</h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <i class="fas fa-map-marker-alt text-red-600 text-xl mt-1 mr-4"></i>
                            <div>
                                <h4 class="font-bold text-gray-800">Dirección</h4>
                                <p class="text-gray-600">Esomercasur, Maracaibo 4004, Zulia Venezuela</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <i class="fas fa-phone-alt text-red-600 text-xl mt-1 mr-4"></i>
                            <div>
                                <h4 class="font-bold text-gray-800">Teléfono</h4>
                                <p class="text-gray-600">+58 414-9699812</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <i class="fas fa-envelope text-red-600 text-xl mt-1 mr-4"></i>
                            <div>
                                <h4 class="font-bold text-gray-800">Email</h4>
                                <p class="text-gray-600">contacto@bermudezla1.com</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <i class="fas fa-clock text-red-600 text-xl mt-1 mr-4"></i>
                            <div>
                                <h4 class="font-bold text-gray-800">Horario</h4>
                                <p class="text-gray-600">Abierto las 24 horas, los 7 días de la semana</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="mt-8">
                        <h4 class="font-bold text-gray-800 mb-4">Síguenos en redes</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-green-600 text-white p-3 rounded-full hover:bg-green-700 transition">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                            <a href="#" class="bg-red-600 text-white p-3 rounded-full hover:bg-red-700 transition">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="#" class="bg-green-600 text-white p-3 rounded-full hover:bg-green-700 transition">
                                <i class="fab fa-whatsapp"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <!-- Contact Form -->
                <div class="md:w-1/2 bg-red-50 p-8 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold text-red-700 mb-6">Envíanos un mensaje</h3>
                    
                    <form class="space-y-4">
                        <div>
                            <label for="name" class="block text-gray-700 font-medium mb-1">Nombre</label>
                            <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500">
                        </div>
                        
                        <div>
                            <label for="email" class="block text-gray-700 font-medium mb-1">Email</label>
                            <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500">
                        </div>
                        
                        <div>
                            <label for="phone" class="block text-gray-700 font-medium mb-1">Teléfono</label>
                            <input type="tel" id="phone" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500">
                        </div>
                        
                        <div>
                            <label for="message" class="block text-gray-700 font-medium mb-1">Mensaje</label>
                            <textarea id="message" rows="4" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500"></textarea>
                        </div>
                        
                        <button type="submit" class="bg-green-600 text-white font-bold py-3 px-6 rounded-lg hover:bg-green-700 transition duration-300 w-full">
                            Enviar Mensaje
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <div class="bg-gray-100 py-8">
        <div class="container mx-auto px-4">
            <h3 class="text-2xl font-bold text-center mb-8 text-gray-800">Nuestra Ubicación</h3>
            <div class="rounded-lg overflow-hidden shadow-lg">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3022.215373510509!2d-73.9878449246876!3d40.75798597138949!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c25855c6480299%3A0x55194ec5a1ae072e!2sTimes%20Square!5e0!3m2!1sen!2sus!4v1687891912345!5m2!1sen!2sus" 
                        width="100%" 
                        height="450" 
                        style="border:0;" 
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="custom-bg text-white py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h2 class="text-2xl font-bold">LA DISTRIBUIDORA BERMUDEZ</h2>
                    <p class="text-lg">LA #01</p>
                </div>
                
                <div class="text-center md:text-right">
                    <p>&copy; 2025 Distribuidora Bermúdez. Todos los derechos reservados.</p>
                    <p class="mt-2">Diseñado con <i class="fas fa-heart text-red-300"></i> para nuestros clientes</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- Floating WhatsApp Button -->
    <a href="https://wa.me/584149699812" class="fixed bottom-8 right-8 bg-green-600 text-white w-16 h-16 rounded-full flex items-center justify-center text-3xl shadow-lg hover:bg-green-700 transition z-50">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Product data
        const products = [
            {
                id: 1,
                name: "Pimentón",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1601493700631-2b16ec4b4716?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Pimentones frescos, rojos y jugosos."
            },
            {
                id: 2,
                name: "Ajos",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1601493700895-ee8a5d2a5b5a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Ajos frescos y aromáticos, selección premium."
            },
            {
                id: 3,
                name: "Variedad de Ajís",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1601493700631-2b16ec4b4716?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Mezcla de ajíes picantes y dulces."
            },
            {
                id: 4,
                name: "Tomates Frescos",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1594282486555-50ae92f9792a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Tomates rojos frescos, recién cosechados."
            },
            {
                id: 5,
                name: "Lechuga Romana",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1603048719536-1a7bed751132?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Lechuga romana fresca, crujiente."
            },
            {
                id: 6,
                name: "Zanahorias",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1447175008436-054170c2e979?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Zanahorias dulces y frescas."
            },
            {
                id: 7,
                name: "Papas",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1518977676601-b53f82aba655?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Papas frescas de la mejor calidad."
            },
            {
                id: 8,
                name: "Tomates al mayor",
                category: "vegetales",
                image: "https://images.unsplash.com/photo-1594282486555-50ae92f9792a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=880&q=80",
                description: "Tomates frescos por cantidad mayorista."
            }
        ];

        // Function to render products
        function renderProducts(category = 'todos') {
            const container = document.getElementById('products-container');
            container.innerHTML = '';
            
            const filteredProducts = category === 'todos' 
                ? products 
                : products.filter(product => product.category === category);
            
            filteredProducts.forEach(product => {
                const card = document.createElement('div');
                card.className = 'bg-white rounded-lg overflow-hidden shadow-md product-card transition duration-300';
                card.innerHTML = `
                    <div class="h-48 overflow-hidden">
                        <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="text-xl font-semibold text-gray-800 mb-2">${product.name}</h3>
                        <p class="text-gray-600 mb-4">${product.description}</p>
                        <div class="flex justify-between items-center">
                            <span class="text-green-600 font-bold">Consultar precio</span>
                            <button class="bg-red-600 text-white px-4 py-1 rounded-full hover:bg-red-700 transition">
                                <i class="fas fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                `;
                container.appendChild(card);
            });
        }

        // Function to filter products
        function filterProducts(category) {
            renderProducts(category);
            
            // Update active tab
            document.querySelectorAll('.category-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            event.target.classList.add('active');
        }

        // Initialize page
        document.addEventListener('DOMContentLoaded', () => {
            renderProducts();
            
            // Smooth scrolling for navigation
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
