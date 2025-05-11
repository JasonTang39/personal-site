<template>
    <div>
        <div style="font-size: clamp(30px, 3vw, 40px); font-weight: bolder; margin-bottom: 30px; text-align: center;">
            Contact 📬 
        </div>
        <div style="font-size: clamp(15px, 4vw, 20px); margin-bottom: 30px; text-align: center;">
            Feel free to contact me via the following platforms.
        </div>

        <div style="display: flex; justify-content: center; align-items: center; gap: 40px;">
            <font-awesome-icon :icon="['fab', 'linkedin-in']" size="2x" style="color: black; cursor: pointer;"
                @click="goToLinkedIn" />
            <font-awesome-icon :icon="['fab', 'github']" size="2x" style="color: black; cursor: pointer;"
                @click="goToGitHub" />
            <font-awesome-icon :icon="['fas', 'square-envelope']" size="2x" style="color: black; cursor: pointer;" @click="goToEmail"/>
            <font-awesome-icon :icon="['fab', 'instagram']" size="2x" style="color: black; cursor: pointer;" />
        </div>
    </div>
</template>

<script setup>
const goToLinkedIn = () => {
    window.open('https://www.linkedin.com/in/%E9%94%A6%E6%9D%B0-%E5%94%90-0b1036362/', '_blank');
}

const goToGitHub = () => {
    window.open('https://github.com/JasonTang39', '_blank');
}

const goToEmail = () => {
    window.location.href = 'mailto:jinjietang@outlook.com';
}
</script>

<style scoped>

</style>