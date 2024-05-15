<script setup>
import { ref } from 'vue';
import axios from 'axios'

const formData = ref({
    name: '',
    email: '',
    message: ''
    
});

const errorMessage = ref('');

async function submitForm() {
    try {
        const response = await axios.post('https://formspree.io/f/mrgvzjyj', formData);
        console.log('Form submitted successfully:', response.data)
        formData.value = { name: '', email: '', message: '' };

    } catch (error) {
                console.error('Error submitting form:', error);
                // Handle error (e.g., display an error message)
                formData.value = { name: '', email: '', message: '' };
                errorMessage.value = 'There was an error submitting the form. Please try again.';
                // Clear the error message after 5 seconds
                setTimeout(() => {
                    errorMessage.value = '';
                }, 5000); // 5000 milliseconds = 5 seconds
            }
}

</script>

<template>
    <section class="section" id="contact">
        <div class="container">
            <div class="row">
                <div class="contact-left">
                    <h1 class="section-title">Contact Me</h1>
                    <p>uccodetech@gmail.com</p>
                    <p>+2349063324523</p>
                    <div class="social-icons">
                        <a href="https://www.facebook.com"><img width="48" height="48" src="https://img.icons8.com/color/48/facebook-new.png" alt="facebook-new"/></a>
                        <a href="https://www.twitter.com"><img width="48" height="48" src="https://img.icons8.com/color/48/twitter--v1.png" alt="twitter--v1"/></a>
                        <a href="https://www.instagram.com"><img width="48" height="48" src="https://img.icons8.com/fluency/48/instagram-new.png" alt="instagram-new"/></a>
                        <a href="https://www.likedin.com"><img width="48" height="48" src="https://img.icons8.com/color/48/linkedin.png" alt="linkedin"/></a>
                    </div>
                    <a href="images/my-cv2.pdf" download class="btn btn2">Download CV</a>
                </div>
                <div class="contact-right">
                    <form @submit.prevent="submitForm">
                        <input type="text" v-model="formData.name" name="Name"  placeholder="Your Name" required>
                        <input type="email" v-model="formData.email" name="email"  placeholder="Your Email" required>
                        <textarea name="message" v-model="formData.message" rows="6"  placeholder="Your Message"></textarea>
                        <button type="submit" class="btn btn2">Submit</button>
                    </form>
                    <p v-if="errorMessage" class="error-message">{{ errorMessage }}</p>
                </div>
            </div> 
        </div>
    </section>
</template>

<style scoped>
.contact-left {
    flex-basis: 35%;
}

.contact-right {
    flex-basis: 60%;
}
  
.contact-left p {
    margin-top: 30px;
}

.social-icons {
    margin-top: 30px;
}

.social-icons a {
    text-decoration: none;
    display: inline-block;
    margin-right: 15px;
    transition: transform 0.5s;
    &:hover {
        color: #ff004f;
        transform: translateY(-5px); 
    }
}

.social-icons a img {
    width: 30px;
    height: 30px;
}

.btn.btn2 {
    display: inline-block;
    background: #ff004f;
}

.contact-right form {
    width: 100%;
}

form input, form textarea {
    width: 100%;
    border: 0;
    outline: none;
    background: #262626;
    padding: 15px;
    margin: 15px 0;
    color: #fff;
    font-size: 18px;
    border-radius: 6px;
}

form .btn2 {
    padding: 14px, 60px;
    font-size: 18px;
    margin-top: 20px;
    cursor: pointer;
}

.error-message {
    color: red;
    margin-top: 10px;
}
</style> 