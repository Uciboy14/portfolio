<template>
    <div class="header-text">
        <p>Web Developer</p>
        <h1>Hi, I'm <span class="red">Emezi<br></span>Uchechi David</h1>
    </div>
</template>

<style scoped>

.header-text {
    margin-top: 20%;
    font-size: 30px;
    line-height: 1.5;
}

.header-text h1 {
    font-size: 60px;
    margin-top: 20px ;
}

.header-text h1 .red {
    color: #ff004f;
} 

@media only screen and (max-width: 600px) {
    
    .header-text {
      margin-top: 10%;
      font-size:  16px;
    }

    .header-text h1 {
      font-size: 30px;
    }
}


</style>