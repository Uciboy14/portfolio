<script setup>

</script>

<template>
    <section class="section" id="services">
        <div class="container">
            <h1 class="section-title">My Services</h1>
            <div class="services-list">
                <div class="services-card">
                    <img src="../assets/images/code.png" alt="">
                    <h2>Web Development</h2>
                    <p>I specialize in website development both the frontend and backend aspect of it.</p>
                    <a href="#">Learn more</a>
                </div>
                <div class="services-card">
                    <img src="../assets/images/app.png" alt="">
                    <h2>Mobile Development</h2>
                    <p>I create mobile apps of all kinds, designed with rich user interfaces, latest icons and more</p>
                    <a href="#">Learn more</a>
                </div>
                <div class="services-card">
                    <img src="../assets/images/software.png" alt="">
                    <h2>Software Dev.</h2>
                    <p>I specialize in all kinds of software development.</p>
                    <a href="#">Learn more</a>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>

#services {
    padding: 30px 0;
}

.services-list {
    display: flex;
    grid-template-columns: repeat(auto-fit, minimax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}

.services-card {
    width: 100%;
    background: #262626;
    padding: 40px;
    font-size: 13px;
    font-weight: 300;
    border-radius: 10px;
    transition: background 0.5s, transform 0.5s;
    &:hover {
        background: #ff004f;
        transform: translateY(-10px);
    }
}

.services-card img {
    width: 60px;
    height: 50px;
    margin-bottom: 30px;
}

.services-card h2 {
    font-size: 30px;
    margin-bottom: 15px;
    font-weight: 600;
}

.services-card p {
    font-size: 15px;
    color: #fff; 
}

.services-card a {
    color: #fff;
    text-decoration: none;
    font-size: 12px;
    margin-top: 20px;
    display: inline-block;
    &:hover {
        color: #1d1717;
    }
}
</style>
