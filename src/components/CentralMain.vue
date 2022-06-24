<!-- this is my component with call back axios -->

<template>

    <div class="bg-main py-3">
        <!-- container of my main page musicList -->
        <div class="container py-3">
            <!-- row for my colls of bootstrap -->
           <div class="row row-cols-5">
            <!-- col where i will do v-for -->
            <div class="col" v-for="(author,i) in musicList" :key="i">
                ciao
                <img src="" alt="">
            </div>
           </div>
        </div>
    </div>
</template>

<script>
//invoco la chiamata di axios
import axios from "axios";

export default{
    name:"CentralMain",
    data(){
        return{
            musicList:[],
            success:true,
        }
    },
    methods:{

        // function for using callback axios
        fetchMusics(){
            axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((axiosResp)=>{
                    this.musicList = axiosResp.data.response
                })
        
        },
    mounted(){
        this.fetchMusics()
        console.log(this.fetchMusics())
    }
        
    }
};
</script>


<style scoped>
.bg-main{
    background-color: #1E2D3B;
}
</style>