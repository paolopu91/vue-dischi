<template>
    <div>
        ciao questo è il main 
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