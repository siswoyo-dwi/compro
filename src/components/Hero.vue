<template>
    <div class="pb-3 relative" id="hero">
      <!-- <div class="mx-4 mt-0 w-100 text-center flex justify-content-center"> -->
      <section id="hero" class="section hero">
        <img src="../../public/images/42ea7b46-14d8-4a6c-8691-7888ffb775df.webp" alt="CV MIB LABS Logo" class="logo">
        <h1 class="hero-title">Welcome to CV MIB LABS</h1>
        <p class="hero-subtitle">Professional Web Development Services</p>
        <a href="#services" class="cta-button">Explore Services</a>
      </section>
    </div>
</template>
<style>

.hero {
    background-image: url("https://img.freepik.com/premium-photo/diverse-group-software-developers-coding-multiple-screens-with-tech-gadgets-scattered_1271244-277381.jpg?w=740");
    background-size: cover; /* Ensures the image covers the entire hero section */
    background-position: center; /* Centers the image */
    background-repeat: no-repeat; /* Prevents the image from repeating */
    color: #fff;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
}

/* Hero Section */

.logo {
    width: 120px;
    animation: zoomIn 1s ease-in-out;
}

.hero-title {
    font-size: 2.5em;
    animation: fadeIn 1.5s ease-in-out;
}

.hero-subtitle {
    font-size: 1.2em;
    margin-bottom: 20px;
    animation: fadeIn 2s ease-in-out;
}

.cta-button {
    padding: 10px 20px;
    background: #fff;
    color: #2575fc;
    text-decoration: none;
    border-radius: 5px;
    transition: transform 0.3s;
    animation: slideIn 2s ease-in-out;
}

.cta-button:hover {
    transform: scale(1.1);
}

.service-card {
    background: #f4f4f4;
    padding: 20px;
    margin: 10px;
    border-radius: 5px;
    animation: slideUp 0.8s ease-in-out;
}

.footer {
    background: #333;
    color: #fff;
    padding: 10px;
    text-align: center;
}

@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

@keyframes slideIn {
    from {
        transform: translateY(20px);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes zoomIn {
    from {
        transform: scale(0.8);
        opacity: 0;
    }
    to {
        transform: scale(1);
        opacity: 1;
    }
}

@keyframes slideUp {
    from {
        transform: translateY(20px);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

/* Responsive Design */
@media (max-width: 768px) {
    .hero-title {
        font-size: 1.8em;
    }

    .hero-subtitle {
        font-size: 1em;
    }
}
/* Navbar Styles */
.navbar {
    position: fixed;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.7); /* Semi-transparent background */
    padding: 10px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 10;
}

.navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
}

.brand-logo {
    color: #fff;
    text-decoration: none;
    font-size: 1.5em;
    font-weight: bold;
}

.navbar-toggle {
    display: none;
    background: none;
    border: none;
    color: #fff;
    font-size: 1.8em;
    cursor: pointer;
}

.navbar-menu {
    display: flex;
    list-style: none;
    gap: 20px;
}

.navbar-menu li {
    margin: 0;
}

.navbar-menu a {
    color: #fff;
    text-decoration: none;
    font-size: 1em;
    padding: 8px 15px;
    transition: background-color 0.3s;
}

.navbar-menu a:hover {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 5px;
}

/* Mobile Styles */
@media (max-width: 768px) {
    .navbar-toggle {
        display: block;
    }

    .navbar-menu {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 100%;
        right: 0;
        background-color: rgba(0, 0, 0, 0.8);
        width: 200px;
        text-align: right;
        padding: 10px 20px;
        border-radius: 5px;
    }

    .navbar-menu.active {
        display: flex;
    }

    .navbar-menu li {
        margin: 10px 0;
    }
}
</style>
