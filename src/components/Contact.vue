<template>
    <!-- Contact Section -->
    <section id="contact" class="contact-section">
        <div class="container">
            <h2>Contact Us</h2>
            <p>If you have any questions or inquiries, feel free to reach out to us using the form below or contact us directly through our provided details.</p>
            
            <div class="contact-info">
            <div class="contact-item">
                <h3>Address</h3>
                <p>123 Business Street,<br> Jakarta, Indonesia 10110</p>
            </div>
            <div class="contact-item">
                <h3>Email</h3>
                <p>info@miblabs.com</p>
            </div>
            <div class="contact-item">
                <h3>Phone</h3>
                <p>+62 123 4567 890</p>
            </div>
            </div>
            
            <div class="contact-form">
                <div class="form-group">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message:</label>
                    <textarea id="message" name="message" rows="5" required></textarea>
                </div>
                <button style="margin: 15px;">Send Message</button>
            </div>
        </div>
    </section>
</template>
<style>
/* Basic styling for the contact section */
.contact-section {
  padding: 60px 20px;
  background-color: #f9f9f9;
}

.contact-section h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
}

.contact-section p {
  text-align: center;
  color: #666;
}

.container {
  max-width: 800px;
  margin: 0 auto;
}

.contact-info {
  display: flex;
  justify-content: space-around;
  margin-bottom: 30px;
}

.contact-item {
  text-align: center;
}

.contact-item h3 {
  color: #555;
  margin-bottom: 5px;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form-group {
  display: flex;
  flex-direction: column;
}

.form-group label {
  color: #333;
  margin-bottom: 5px;
}

.form-group input, 
.form-group textarea {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.contact-form button {
  padding: 10px;
  background-color: #007BFF;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.contact-form button:hover {
  background-color: #0056b3;
}

</style>