<!-- this is my component with call back axios -->

<template>

    <div class="bg-main py-3">
      
        <!-- container of my main page musicList -->
        <div class="container py-3">
            <!-- row for my colls of bootstrap -->
           <div class="row row-cols-5">
            <!-- col where i will do v-for -->
            <div class="my-col col" v-for="(author,i) in musicList" :key="i">
                <img :src="author.poster" alt="">
                <h2>{{author.title}}</h2>
                <h3>{{author.author}}</h3>
                <h4>{{author.year}}</h4>
            </div>
           </div>
        </div>
    </div>
</template>

<script>
//invoco la chiamata di axios
import axios from "axios";
import {state} from "../store"

export default{
    name: "CentralMain",
    data() {
        return {
            // my array empty
            musicList: [],
            success: true,
            searchGenre: "",
        };
    },
    methods: {
        // function for using callback axios
        fetchMusics(searchGenre) {
            axios.get("https://flynn.boolean.careers/exercises/api/array/music", {
                params:{
                    genre:searchGenre,
                }
            })
            .then((axiosResp) => {
                this.musicList= [];
                this.musicList = axiosResp.data.response;
            
            });
        },
        filterGenre(){
            const lista = []

            this.musicList.forEach(album => {
                if(!lista.includes(album.genre)){
                    lista.push(album.genre)
                }
            })

            return lista
         
        },
        filteredAlbums(){
            if(!state.selectedGenre){
                return this.musicList
            }
            return this.musicList.filter((album) =>{
                return album.genre === state.selectedGenre;
            })
        },
    },
    mounted() {
        console.log(this.fetchMusics());
        this.fetchMusics();
    },

};
</script>


<style scoped>
.bg-main{
    background-color: #1E2D3B;
    padding: 7rem 0;
    height: calc(100vh - 80px);
}
.my-col{
    text-align: center;
    padding: 1rem;
}
img{
    aspect-ratio: 1/1;
    height: 180px;
    max-width: 100%;
}
h2{
    font-size: 20px;
    text-align: center;
    color: white;
}
h3{
    font-size:15px;
    text-align: center;
    color: rgb(182, 182, 182);
}
h4{
    font-size: 10px;
    text-align: center;
    color: rgb(182, 182, 182);
}
.my-container{
    width: 300px;
}
</style>