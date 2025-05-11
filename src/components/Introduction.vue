<template>
    <div class="introduction-container">
        <div style="font-size: clamp(40px, 8vw, 90px); font-weight: bolder;">
            Jason Tang
        </div>
        <div style="font-size: clamp(10px, 3vw, 30px); ">
            Taizhou University Computer Science and Technology Student
        </div>

        <el-avatar style="width: 220px; height: 220px;" :src="icon" />
    </div>
</template>

<script setup>
import icon from '../assets/images/icon.png'

</script>

<style scoped>
.introduction-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-top: 150px;
    margin-bottom: 100px;
}

.el-avatar el-avatar--circle{
    border: 0;
}
</style>