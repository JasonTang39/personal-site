<template>
    <el-card class="project-card" shadow="hover" :body-style="{ padding: '0px' }" @click="goToProjectRepository">
        <el-container>
            <el-aside class="project-image" style="overflow: hidden; width: 45%;">
                <el-image style="width: 100%; height: 100%;" :src="imageUrl" fit="fill" />
            </el-aside>
            <el-main>
                <div style="font-size: 20px; font-weight: bold;">
                    {{ name }}
                </div>
                <div style="font-size: 15px; line-height: 25px;">
                    {{ description }}
                </div>
                <div style="display: flex; flex-wrap: wrap; gap: 10px;">
                    <el-tag type="primary" round v-for="(tag, index) in tags" :key="index">{{ tag }}</el-tag>
                </div>
            </el-main>
        </el-container>
    </el-card>
</template>



<script setup>
const { githubUrl } = defineProps({
    name: {
        type: String,
        required: true
    },
    description: {
        type: String,
        required: true
    },
    tags: {
        type: Array,
        required: true
    },
    imageUrl: {
        type: String,
        required: true
    },
    githubUrl: {
        type: String,
        required: true
    }
})


const goToProjectRepository = () => {
    window.open(githubUrl, '_blank')
}
</script>

<style scoped>
.project-card {
    width: 100%;
    max-width: 700px;
    cursor: pointer;
    border-radius: 20px;
}

.el-main {
    display: flex; 
    flex-direction: column;
    justify-content: center;
    gap: 20px;
}

@media (max-width: 768px) {
  .project-image {
    display: none;
  }
}
</style>