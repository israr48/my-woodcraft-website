# my-woodcraft-website
"Welcome to WoodCraft Carpentry Services — where craftsmanship meets innovation. We specialize in designing and building high-quality custom woodwork for your home and business. Whether you're looking for custom furniture, home renovations, or specialized woodworking projects, our experienced team is here to turn your vision into reality."
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WoodCraft Carpentry Services</title>
    <style>
        /* Reset Default Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        /* Body Styling */
        body {
            background-color: #f4f1ea;
            color: #333;
        }

        /* Header Styling */
        header {
            background: #8B5A2B;
            color: white;
            text-align: center;
            padding: 20px;
            background-image: url('your-cover-image.jpg'); /* Replace with your cover image */
            background-size: cover;
            background-position: center;
        }

        header h1 {
            margin-bottom: 10px;
        }

        header p {
            font-style: italic;
        }

        /* Navigation Bar */
        nav {
            background: #6F4E37;
            text-align: center;
            padding: 10px;
            position: relative;
        }

        .nav-links {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 10px;
            transition: 0.3s;
        }

        nav a:hover {
            background: #543B27;
        }

        /* Mobile Menu Button */
        .menu-toggle {
            display: none;
            background: #543B27;
            color: white;
            border: none;
            padding: 10px;
            font-size: 18px;
            cursor: pointer;
            width: 100%;
            text-align: left;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                background: #6F4E37;
                position: absolute;
                width: 100%;
                top: 40px;
                left: 0;
            }

            .nav-links a {
                padding: 10px;
                display: block;
            }

            .menu-toggle {
                display: block;
            }
        }

        /* Main Content */
        main {
            padding: 20px;
            text-align: center;
        }

        /* About Section */
        .about {
            background: white;
            padding: 20px;
            margin: 20px auto;
            width: 80%;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }

        /* Services Section */
        .services {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 20px;
        }

        .service-card {
            background-color: white;
            width: 200px;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .service-card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 10px;
        }

        .service-card h3 {
            margin-top: 10px;
        }

        .service-card p {
            margin: 10px 0;
        }

        .add-to-cart {
            background-color: #6F4E37;
            color: white;
            padding: 8px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .add-to-cart:hover {
            background-color: #543B27;
        }

        /* Footer */
        footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .contact-buttons a {
            display: inline-block;
            padding: 10px;
            margin: 5px;
            background-color: #25D366; /* WhatsApp green color */
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-size: 18px;
        }

        .contact-buttons a:hover {
            background-color: #128C7E;
        }

        .contact-landline {
            background-color: #008CBA;
        }

    </style>
</head>
<body>

    <header>
        <h1>WoodCraft Carpentry Services</h1>
        <p id="greeting"></p> <!-- Dynamic Greeting -->
    </header>

    <nav>
        <button class="menu-toggle">☰ Menu</button>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">Services</a>
            <a href="#">Gallery</a>
            <a href="#">Contact</a>
        </div>
    </nav>

    <main>
        <section class="about">
            <h2>About Our Carpentry Services</h2>
            <p>We specialize in custom woodwork, furniture design, and home renovations. Our expert carpenters create functional and beautiful wood pieces to enhance your living space.</p>
        </section>

        <section class="services">
            <div class="service-card">
                <img src="service1.jpg" alt="Furniture Design">
                <h3>Furniture Design</h3>
                <p>Custom-made furniture to fit your style and space.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>

            <div class="service-card">
                <img src="service2.jpg" alt="Woodworking">
                <h3>Woodworking</h3>
                <p>Quality woodworking for home and office interiors.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>

            <div class="service-card">
                <img src="service3.jpg" alt="Renovations">
                <h3>Renovations</h3>
                <p>Transform your space with our expert carpentry renovations.</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>

            <!-- Add more services here -->
        </section>

        <section class="contact-buttons">
            <a href="https://wa.me/923439780933" target="_blank">Contact us on WhatsApp</a>
            <a href="tel:+923439780933" class="contact-landline">Call Us (Landline)</a>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 WoodCraft Carpentry Services. All rights reserved.</p>
    </footer>

    <script>
        // Dynamic Greeting Based on Time
        function updateGreeting() {
            const greeting = document.getElementById("greeting");
            const hour = new Date().getHours();

            if (hour < 12) {
                greeting.innerText = "Good Morning! Start your day with quality craftsmanship.";
            } else if (hour < 18) {
                greeting.innerText = "Good Afternoon! We build excellence in every piece.";
            } else {
                greeting.innerText = "Good Evening! Your dream woodwork awaits.";
            }
        }

        // Call function on page load
        updateGreeting();

        // Mobile Menu Toggle
        const menuToggle = document.querySelector(".menu-toggle");
        const navLinks = document.querySelector(".nav-links");

        menuToggle.addEventListener("click", () => {
            navLinks.style.display = (navLinks.style.display === "flex") ? "none" : "flex";
        });
    </script>

</body>
</html>

