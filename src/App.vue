<script setup>
import Header from "./components/Header.vue";
import Introduction from "./components/Introduction.vue";
import AboutMe from "./components/AboutMe.vue";
import Experience from "./components/Experience.vue"
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue"
</script>

<template>
  <Header></Header>
  <Introduction></Introduction>
  <AboutMe id="about-me"></AboutMe>
  <Experience id="experience"></Experience>
  <Projects id="projects"></Projects>
  <Contact id="contact"></Contact>
  <Footer></Footer>
  <el-backtop />
</template>

<style scoped>
#about-me,
#experience,
#projects,
#contact {
  scroll-margin-top: 100px;
}
</style>
