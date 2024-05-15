<template>
    <section class="section" id="portfolio">
        <div class="container">
            <h1 class="section-title">My Work</h1>
            <div class="work-list">
                <div class="work">
                    <img src="../assets/images/work-1.png" alt="">
                    <div class="layer">
                        <h3>Social Media App</h3>
                         <p>The app connects you to the talented people around the world.
                            Download it from play store.
                         </p>
                         <a href="#">Check</a>
                    </div>
                </div>
                <div class="work">
                    <img src="../assets/images/work-2.png" alt="">
                    <div class="layer">
                        <h3>Ecommerce Web App</h3>
                         <p>The wwebsite that sells computer and hardware resources, with nice shopping cart and a checkout page..
                         </p>
                         <a href="#">Check</a>
                    </div>
                </div>
                <div class="work">
                    <img src="../assets/images/work-3.png" alt="">
                    <div class="layer">
                        <h3>Online Shopping App</h3>
                         <p>The app is an onlie shopping app where all kinds of products are sold.
                            Download it from play store.
                         </p>
                         <a href="#">Check</a>
                    </div>
                </div>
            </div>
            <a href="" class="btn">See more</a>
        </div>
    </section>
</template>

<style scoped>
#portfolio {
    padding: 50px 0;
}

.work-list {
    display: flex;
    grid-template-columns: repeat(auto-fit, minimax(250px, 1fr));
    grid-gap: 40px;
    margin-top: 50px;
}

.work {
    border-radius: 10px;
    position: relative;
    overflow: hidden;
}

.work img {
    width: 100%;
    border-radius: 10px;
    display: block;
    transition: transform 0.5s;
}

.layer {
    width: 100%;
    height: 0;
    background: linear-gradient(rgba(0,0,0,0.6), #ff004f);
    border-radius: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 0 40px;
    text-align: center;
    transition: height, 0.5s;
}

.layer h3 {
     font-weight: 500px;
     margin-bottom: 20px;
}

.layer a {
    margin-top: 20px;
    color: black;
    text-decoration: none;
    font-size: 18px;
    line-height: 60px;
    background: #fff;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    text-align: center;
} 


.work:hover img {
    transform: scale(1.1);
}

.work:hover .layer {
    height: 100%;
}


</style>