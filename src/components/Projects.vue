<template>
    <div style="justify-content: center; display: flex;flex-direction: column;  align-items: center;">
        <div style="font-size: clamp(30px, 3vw, 40px); font-weight: bolder; margin-bottom: 30px;">
            Projects 💻
        </div>
        <div style="display: flex; flex-direction: column; justify-content: center; gap: 30px; margin-bottom: 120px;">
            <ProjectCard v-for="(project, index) in projects" :key="index" :name="project.name"
            :description="project.description" :tags="project.tags" :imageUrl="project.imageUrl" :githubUrl="project.githubUrl"/>
        </div>
    </div>
</template>

<script setup>
import ProjectCard from './ProjectCard.vue';
import project1Img from '../assets/images/project1.png'
import OutdoorSportsSmartHelmet from '../assets/images/outdoor-sports-smart-helmet.png'
import { ref } from 'vue'

const projects = ref([
    {
        name: "Second-hand book trading website",
        description: "A campus-oriented secondhand textbook trading platform designed to reduce paper waste and improve resource utilization. The platform supports book listing, search, and transactions, offering a multi-user experience. An admin dashboard is included to ensure transaction safety and content compliance.",
        tags: ["Vue.js", "Element Plus","ASP.NET Web API", "MySQL"],
        imageUrl: project1Img,
        githubUrl: "https://github.com/Kettkk/hdu-bookhub"
    },
    {
        name: "Outdoor Sports Smart Helmet",
        description: "A wearable helmet for outdoor activities like hiking and camping, designed to monitor biometric and environmental data. It connects to an Android app for real-time updates and features a camera for object detection and video recording to enhance safety and capture experiences.",
        tags: ["Vue.js", "SpringBoot", "MySQL","Android","Python"],
        imageUrl: OutdoorSportsSmartHelmet,
        githubUrl: "https://github.com/Kettkk/Helmi"
    }
])
</script>

