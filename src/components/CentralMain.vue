<!-- this is my component with call back axios -->

<template>
    <div class="bg-main py-3">
        <div class="container py-3">
           <div class="row row-cols-5">
            <div class="col">
                ciao
                <img src="" alt="">
            </div>
           </div>
        </div>
        
    </div>
</template>

<script>
import axios from "axios";

export default{
    name:"CentralMain",
    props:{

    },
    data(){
        return{
            musicList:[],
        }
    },
    methods:{
        fetchMusics(){
            axios
                .get("https://flynn.boolean.careers/exercises/api/array/music")
                .then((axiosResp)=>{
                    this.musicList = axiosResp.data.response
                })
        
        },
        
    }
};
</script>


<style scoped>
.bg-main{
    background-color: #1E2D3B;
}
</style>