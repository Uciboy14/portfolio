<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')

function Send(name, email, message) {
    console.log(name, message, email)
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
                    <form action="">
                        <input type="text" name="Name" v-model="name" placeholder="Your Name" required>
                        <input type="email" name="email" v-model="email"  placeholder="Your Email" required>
                        <textarea name="message" rows="6" v-model="message" placeholder="Your Message"></textarea>
                        <button type="submit" class="btn btn2" @click.prevent="Send">Submit</button>
                    </form>
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
</style> 