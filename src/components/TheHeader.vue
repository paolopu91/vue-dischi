<!-- Questo qui sarà il componente del mio header -->

<template>

<div class="my-bg d-flex justify-content-between">
        
        <img class="my-img" src="/img/favicon-32x32.png" alt="">
        <SearchMusicGenre></SearchMusicGenre>
         <!-- search bar
        <div class="container d-flex justify-content-end">
            <div class="my-container">
                <SearchMusicGenre @search="filterGenre"></SearchMusicGenre>
            </div>
        </div> -->
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
    components: {
        SearchMusicGenre 
        }
};
</script>

<style >
.my-bg{
    background-color: #2E3A46;
    height: 100%;
    padding: 0.5rem;
}
.my-img{
    width: 67px;
}
</style>