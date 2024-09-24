<template>
    <!-- Services Section -->
    <section id="services" class="section services">
        <h2>Our Services</h2>
        <p>At MIB LABS, we offer a range of services to help you excel in web development. Our expert-led training and real-world projects ensure you gain practical experience in essential programming languages and frameworks.</p>
        
        <div class="service-card-container">
            <!-- JavaScript Training Card -->
            <div class="service-card">
                <div class="service-icon">⚡</div>
                <h3>JavaScript Training</h3>
                <p>Master the fundamentals of JavaScript, the most widely used language for front-end and back-end web development. Gain hands-on experience with modern JavaScript frameworks.</p>
            </div>
            
            <!-- PHP Training Card -->
            <div class="service-card">
                <div class="service-icon">🐘</div>
                <h3>PHP Training</h3>
                <p>Learn the ins and outs of PHP, a powerful language for building dynamic server-side applications. Understand how to work with databases and create efficient back-end solutions.</p>
            </div>
            
            <!-- Full-Stack Web Development Card -->
            <div class="service-card">
                <div class="service-icon">🌐</div>
                <h3>Full-Stack Web Development</h3>
                <p>Become a full-stack developer by mastering both front-end and back-end technologies. Build complete web applications from scratch using JavaScript and PHP.</p>
            </div>
        </div>
    </section>
</template>
<style>
/* Services Section */
.services {
    background-color: #fff;
    padding: 60px 20px;
    text-align: center;
}

.services h2 {
    color: #333;
    font-size: 2.5em;
    margin-bottom: 20px;
}

.services p {
    color: #666;
    font-size: 1.1em;
    max-width: 800px;
    margin: 0 auto 30px;
    line-height: 1.6;
}

/* Service Card Container */
.service-card-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
}

/* Service Card Styles */
.service-card {
    background: linear-gradient(135deg, #4CAF50, #8BC34A); /* Default green gradient */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    padding: 20px;
    width: 300px;
    text-align: left;
    transition: transform 0.3s;
    color: #fff;
    position: relative;
}

.service-card:hover {
    transform: translateY(-5px);
}

.service-icon {
    font-size: 2.5em;
    margin-bottom: 10px;
}

.service-card h3 {
    font-size: 1.5em;
    margin-bottom: 10px;
}

.service-card p {
    font-size: 1em;
    margin-bottom: 0;
}

/* Custom Gradients for Each Card */
.service-card:nth-child(1) {
    background: linear-gradient(135deg, #f39c12, #f1c40f); /* JavaScript Gradient */
}

.service-card:nth-child(2) {
    background: linear-gradient(135deg, #3498db, #2ecc71); /* PHP Gradient */
}

.service-card:nth-child(3) {
    background: linear-gradient(135deg, #e9e106, #cde808); /* Full-Stack Development Gradient */
}

/* Responsive Design */
@media (max-width: 768px) {
    .service-card-container {
        flex-direction: column;
        align-items: center;
    }

    .service-card {
        width: 90%;
    }
}


</style>