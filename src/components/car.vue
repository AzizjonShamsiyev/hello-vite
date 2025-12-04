<template>
    <div id="app">
        <p id="show">{{ message }}</p>
        <!-- <img :src="imgSrc" alt="Car image" width="300"> -->
        <img style="width: 240px; height: auto;" v-bind:src="imgSrc" alt="Car image">
        <p>
            <input type="button" value="car switch" @click="changeWords">
            </input>
        </p>
    </div>
</template>
<script setup>
    import {ref} from 'vue';
    const message = ref("weilan");
    const carLink1 = "https://cdn.pixabay.com/photo/2015/01/19/13/51/car-604019_1280.jpg";
    const carLink2 = "https://www.audi.cn/content/dam/OneWeb/faw_vw/models/a5spb/a5_spb_power.jpg";
    const imgSrc=ref(carLink1);
    function changeWords(){
        if( message.value==="Audi"){
            message.value="weilan";
            imgSrc.value="https://cdn.pixabay.com/photo/2015/01/19/13/51/car-604019_1280.jpg";
            return;
        }
        else if( message.value==="weilan"){
            message.value="BMW";
            imgSrc.value="https://i.ytimg.com/vi/sUxJT3M42do/maxresdefault.jpg";
            return;
        }
        else{
            message.value="Audi";
            imgSrc.value="https://www.audi.cn/content/dam/OneWeb/faw_vw/models/a5spb/a5_spb_power.jpg";
            return;
        }
    }
</script>
<style>
#show{
    width: 300px;
    height: 50px;
    background-color: #85ce5b;
    border: 2px solid #93e490;
    padding: 10px 10px;
    text-align: justify;
}
</style>