<template>
    <div class="about-me-container">
        <div style="font-size: clamp(30px, 3vw, 40px); font-weight: bolder; margin-bottom: 30px;">
            About Me 🧑‍💻
        </div>

        <div class="about-me-content">
            <div style=" width: 100%; max-width: 700px; font-size: clamp(15px, 2vw, 20px); line-height: 30px; padding-right: 20px;padding-left: 20px;">
                👋 Hi there!<br>
                I'm a computer science undergraduate passionate about using technology to make the world a better
                place.<br>
                <br>
                🌍 Tech for Good<br>
                I care deeply about supporting marginalized communities, protecting the environment, and building tools
                that
                bring real value to people's lives.<br>
                <br>
                💡 Let's Connect<br>
                I'm always eager to learn, collaborate, and create with purpose. Let's build something meaningful
                together!
            </div>

            <el-image class="my-photo" style="width: 250px; height: 300px" src="" :fit="fit" />
        </div>

    </div>
</template>

<script setup>

</script>

<style scoped>
.about-me-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 150px;
}

.about-me-content {
    display: flex;
    gap: 100px;
}

@media (max-width: 768px) {
    .my-photo {
        display: none;
    }
}
</style>