<template>
   <div>
        <div class="input-group mb-3 w-100">
            <input type="text" class="form-control" placeholder="Filter genre" aria-label="Recipient's username" aria-describedby="button-addon2" v-model="searchGenre">
            <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="makeSearch">Search</button>
        </div>
   </div>
</template>


<script>
    export default{
        name:"SearchMusicGenre",

        data(){
            return{
                searchGenre:"",
            }
            },
            methods:{
                makeSearch(){
                    this.$emit("search", this.searchGenre)
                }
            },
        
   
   }
    
</script>



<style scoped>
</style>