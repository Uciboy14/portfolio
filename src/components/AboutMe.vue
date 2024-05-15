<script setup>
import { ref } from 'vue'
import user from "../assets/images/user1.jpeg"

const tabs = ref(['Skills', 'Experience', 'Education']
)

const tabContent = ref([
  [
    { 'Web Development': 'Web App development' }, 
    { 'Mobile Development': 'Mobile development' }, 
    { 'Software Development': 'Designing softwares' }
  ],
  [
    { '2021 - Current': 'Alx Alunmui Traning' }, 
    { '2019 - 2021': 'Team Lead at StartApp LLC.' }, 
    { '2016 - 2017': 'Internship at Radical X Software company' }
  ],
  [
    { '2016': 'Web Development Training at 3MITT Institute' }, 
    { '2018': 'BSc Micheal Okpara University Umudike' }, 
    { '2022': 'Alx Institute of Software Engineer' }
  ]
]);

function getCategoryName(category) {
    return Object.keys(category)[0];
}

function getCategoryValue(category) {

    return Object.values(category)[0];
}

    
const activeIndex = ref(0)


function setActiveTab(index) {
    activeIndex.value = index;
}


</script>


<template>
    <section class="section" id="about">
        <div class="container">
            <div class="row">
                <div class="about-col-1">
                    <img :src="user" alt="">
                </div>
                <div class="about-col-2">
                    <h1 class="section-title">About Me</h1>
                    <p>As a seasoned developer with a diverse skill set, David is a force to be reckoned with in the
                        tech industry.
                        With expertise spanning web development, app development, and software development, David brings
                        a unique blend of creativity, technical prowess, and innovation to every project.</p>
                    <div class="tab-titles">
                        <p 
                            v-for="(tab, index) in tabs" 
                            :key="index"
                            :class="{'tab-links': true, 'active-links': activeIndex === index}"
                            @click="setActiveTab(index)"
                            >
                            {{ tab }}
                        </p>
                    </div>
                    <div class="tab-contents">
                        <ul v-for="(content, index) in tabContent"
                            :key="index"
                            v-show="activeIndex === index"
                            >
                            <li v-for="(item, key, itemIndex) in content"
                                :key="itemIndex"
                                >
                               <span>{{ getCategoryName(item) }}</span><br>
                                {{ getCategoryValue(item) }}
                            </li> 
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>  

<style scoped>
#about { 
    padding: 80px 0;
    color: #ababab;
}


.about-col-1 {
    flex-basis: 35%;
}

.about-col-1 img {
    width: 100%;
    border-radius: 15px;
}

.about-col-2 {
    flex-basis: 60%;
}

.section-title {
    font-size: 55px;
    font-weight: 600;
    color: #fff;
}

.tab-titles {
    display: flex;
    margin: 20px 0 40px;
}

.tab-links {
    margin-right: 50px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    position: relative;
}
 
.tab-links::after {
    content: '';
    width: 0;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left: 0;
    bottom: -8px;
    transition: 0.5s ;
}

.tab-links.active-links::after {
    width: 50%;
} 

.tab-contents ul li {
    list-style: none;
    margin: 10px 0;
}

.tab-contents ul li span {
    color: #b54769;
    font-size: 14px;
    font-weight: 600;
} 

</style>