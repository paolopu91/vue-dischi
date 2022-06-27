<template>
   <div>
        <div class="input-group mb-3 w-100">
            <input type="text" class="form-control" placeholder="Filter genre" aria-label="Recipient's username" aria-describedby="button-addon2" v-model="searchGenre">
            <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="searchClick">Search</button>
        </div>
   </div>
</template>


<script>
import {state} from "../store.js";


    export default{
        name:"SearchMusicGenre",

        props:{
            filterGenre: Array,
        },
        data(){
            return{
                searchGenre:"",
            }
            },
        computed:{
            genreFromState(){
                return state.filterGenre
            },
        },
        methods:{
            searchClick(){
                state.selectedGenre = this.searchGenre
            },
        },
        
   
   };
    
</script>