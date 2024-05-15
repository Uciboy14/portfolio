<script setup>
import logo from "../../assets/images/logo.png"
import HeaderText from "./HeaderText.vue";
</script>

<template>
    <header class="section" id="header">
        <div class="container">
            <nav class="navbar-menu">
                <img :class="{ 'logo': true }" :src="logo" alt="logo">
                <ul class="nav">
                    <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">About</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Services</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Portfolio</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
                </ul>
            </nav>
            <HeaderText/>
        </div>
    </header>
</template>

<style scoped>

  
.navbar-menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.logo {
  width: 140px;
}

.navbar-menu .nav-item {
    display: inline-block;
    list-style: none;
    margin: 10px 20px;
}

.navbar-menu .nav-link {
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    position: relative;
}

.navbar-menu .nav-link::after {
    content: "";
    width: 0;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left: 0;
    bottom: -6px;
    transition: 0.5s;
}

.navbar-menu .nav-link:hover::after {
    width: 100%;
}


</style>