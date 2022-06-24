<template>
    <div class="bg-main py-3">
        <div class="container py-3">
            ciao <br>
            questo <br>
            è   <br>
            il <br>
            main <br>
        </div>
        
    </div>
</template>

<script>
import axios from "axios"

export default{
    name:"CentralMain",
    props:{

    },
    data(){
        return{

        }
    },
    methods:{
        fetchMusics(){
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then(function(axiosResp){
                console.log(axiosResp);
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