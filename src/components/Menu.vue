<template>
    <header>

        <Head />
    </header>
    <div class="div3d">
        <Suspense>
            <TheExperience />
        </Suspense>
    </div>
    <div class="buttonDiv">
        <img style="width: 150px;" src="../assets/iphone14pro.png" alt="">
    </div>
    <div class="buttonDiv">
        <button class="sign">
            Sign up
        </button>
    </div>
</template>
<script setup lang="ts">
import Head from './menu/Head.vue';
import TheExperience from './menu/TheExperience.vue';
</script>
<style scoped>
.div3d {
    display: block;
    justify-content: center;
    align-items: center;
    left: -50%;
    margin-top: -10px;
}

.sign {
    display: flex;
    justify-content: center;
    background-color: #FFFAFA;
    padding: 10px 30px;
    font-size: 20px;
    border-radius: 50px;
    left: -50%;
}

.buttonDiv {
    margin-top: 5px;
    display: flex;
    justify-content: center;
    align-items: center;
    /* left: -50%; */
}

.buttonDiv button {
    filter: drop-shadow(0 0 0.30rem rgb(206, 65, 228));
    border: none;
    transition: .5s;
}

.buttonDiv button:hover {
    filter: drop-shadow(0 0 0.50rem rgb(201, 44, 225));
    transition: .5s;
}
</style>