<!-- Questo qui sarà il componente del mio header -->

<template>
<div class="my-bg d-flex justify-content-start">
        <img class="my-img" src="/img/spotify-logo.png" alt="">
</div>
</template>

<script>
export default{
    name:"TheHeader",
    props:{

    },
    data(){
        return{

        }
    },
};
</script>

<style >
.my-bg{
    background-color: #2E3A46;
    height: 100%;
}
.my-img{
    width: 80px;
    height: 80px;
}
</style>