<!-- my html -->
<template>
    <div class="my-bg d-flex justify-content-between">
        <img class="my-img" src="/img/favicon-32x32.png" alt="">

        <div>
            <SearchMusicGenre></SearchMusicGenre>
        </div>
    </div>
</template>

<!-- my vuecli -->
<script>
import SearchMusicGenre from "./SearchMusicGenre.vue";
export default {
    data (){
        return{

        }
    },
    components:{
        SearchMusicGenre
    }
}

</script>

<!-- my scss -->
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