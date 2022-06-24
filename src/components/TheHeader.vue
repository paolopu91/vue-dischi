<!-- Questo qui sarà il componente del mio header -->

<template>

<div class="my-bg d-flex justify-content-between">
        
        <img class="my-img" src="/img/spotify-logo.png" alt="">
        <SearchMusicGenre class="d-none" />
</div>
</template>

<script>
import SearchMusicGenre from './SearchMusicGenre.vue';
export default{
    name: "TheHeader",
    props: {},
    data() {
        return {};
    },
    components: { SearchMusicGenre }
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
    border-radius: 50%;
}
</style>