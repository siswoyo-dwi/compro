<template>
    <!-- About Us Section -->
    <section id="about" class="section about">
        <h2>About Us</h2>
        <p>MIB LABS is a dedicated bootcamp program that offers comprehensive training in JavaScript and PHP fundamentals. Our goal is to empower aspiring developers with essential skills to build dynamic web applications. Here’s why learning these languages with us is beneficial:</p>
        
        <div class="card-container">
            <!-- JavaScript Card -->
            <div class="card">
                <h3>JavaScript</h3>
                <p>JavaScript is the language of the web, essential for front-end and back-end development. It allows you to create interactive and dynamic web applications.</p>
                <ul>
                    <li>Highly versatile: Used for both client-side and server-side development (Node.js)</li>
                    <li>Vibrant ecosystem with numerous libraries and frameworks (React, Vue.js, etc.)</li>
                    <li>Widely in-demand skill for web developers</li>
                </ul>
            </div>

            <!-- PHP Card -->
            <div class="card">
                <h3>PHP</h3>
                <p>PHP is a powerful server-side scripting language that powers a large portion of websites globally, making it a valuable skill for back-end development.</p>
                <ul>
                    <li>Widely used for building dynamic websites and applications</li>
                    <li>Has a simple learning curve, ideal for beginners in web development</li>
                    <li>Integrates seamlessly with databases like MySQL</li>
                </ul>
            </div>
        </div>
    </section>
</template>
<style>

/* About Us Section */
.about {
    background-color: #f9f9f9;
    padding: 60px 20px;
    text-align: center;
}

.about h2 {
    color: #333;
    font-size: 2.5em;
    margin-bottom: 20px;
}

.about p {
    color: #666;
    font-size: 1.1em;
    max-width: 800px;
    margin: 0 auto 30px;
    line-height: 1.6;
}

/* Card Container */
.card-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
}
/* Card Styles */
.card {
    background: #f9f9f9; /* Default background */
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 15px;
    flex: 0 0 300px;
    margin: 0 10px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
}

/* Gradient for JavaScript Card */
.card:nth-child(odd) {
    background: linear-gradient(135deg, #f39c12, #f1c40f); /* Yellow-Orange gradient */
}

/* Gradient for PHP Card */
.card:nth-child(even) {
    background: linear-gradient(135deg, #3498db, #2ecc71); /* Blue-Green gradient */
}

.card:hover {
    transform: translateY(-5px);
}

.card h3 {
    font-size: 1.5em;
    margin-bottom: 10px;
}

.card p {
    margin-bottom: 10px;
}

.card ul {
    padding-left: 20px;
    list-style: disc;
}

.card ul li {
    margin-bottom: 5px;
}
/* Responsive Design */
@media (max-width: 768px) {
    .card-container {
        flex-direction: column;
        align-items: center;
    }

    .card {
        width: 90%;
    }
}

</style>
