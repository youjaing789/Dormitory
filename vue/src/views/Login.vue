<template>
    <div class="login-container">
               
        <div style="width: 400px; margin: 150px auto">
            <div style="color: black; font-size: 30px; text-align: left; padding: 30px 0">登陆</div>
            <el-form ref="form" :model="form" :rules="rules" size="large">
                <el-form-item prop="username">
                    <el-input v-model="form.username" clearable prefix-icon="avatar"></el-input>
                </el-form-item>
                <el-form-item prop="password">
                    <el-input v-model="form.password" prefix-icon="lock" show-password></el-input>
                </el-form-item>
                <el-form-item :model="form" prop="identity">
                    <el-radio v-model="form.identity" label="stu" style="color: grey">学生</el-radio>
                    <el-radio v-model="form.identity" label="dormManager" style="color: grey">宿舍管理员</el-radio>
                    <el-radio v-model="form.identity" label="admin" style="color: grey">后勤管理中心</el-radio>
                </el-form-item>
                <el-form-item>
                    <el-button :disabled="!disabled" style="width: 20%" type="primary" @click="login">登 录</el-button>
                </el-form-item>
            </el-form>
        </div>
    </div>
    
</template>
<script src="@/assets/js/Login.js"></script>
<style scoped>
.login-container {
    position: fixed;
    height: 100%;
    width: 100%;
    top: 0;
    left: 0;
    background: linear-gradient(
            135deg,
            hsl(170deg, 80%, 70%),
            hsl(190deg, 80%, 70%),
            hsl(250deg, 80%, 70%),
            hsl(320deg, 80%, 70%),
            hsl(320deg, 80%, 70%),
            hsl(250deg, 80%, 70%),
            hsl(190deg, 80%, 70%),
            hsl(190deg, 80%, 70%),
            hsl(170deg, 80%, 70%)
    );
    background-size: 600%;
    animation: myanimation 15s linear infinite;
}

@keyframes myanimation {
    0% {
        background-position: 0 0;
    }
    100% {
        background-position: 100% 100%;
    }
}

</style>