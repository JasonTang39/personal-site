<template>
    <div class="header">
        <a href="#about-me">About Me</a>
        <a href="#experience">Experience</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
        <a :href="resume" download="resume.pdf">Resume</a>
    </div>

    <el-button class="menu-button" @click="drawer = true">
        <font-awesome-icon :icon="['fas', 'bars']" size="xl" />
    </el-button>

    <el-drawer v-model="drawer" size="40%">
        <div class="drawer">
            <a href="#about-me">About Me</a>
            <a href="#experience">Experience</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
            <a :href="resume" download="resume.pdf">Resume</a>
        </div>
    </el-drawer>
</template>

<script setup>
import resume from '../assets/pdfs/chineseResume.pdf'
import { ref } from 'vue'

const drawer = ref(false)
</script>

<style scoped>
.header {
    width: 100%;
    height: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 5vw;
    background-color: white;
    border-bottom: 1px solid #DDDDDD;
}

.menu-button{
    display: none;
    margin-top: 16px;
    margin-right: 16px; 
    margin-left: auto;  
}

.drawer {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;
}

a {
    text-decoration: none;
    color: inherit;
    font-size: clamp(15px, 2vw, 20px);
}

a:hover {
    color: #409EFF;
}

@media (max-width: 768px) {
    .header {
        display: none;
    }

    .menu-button {
        display: flex;
    }
}



</style>