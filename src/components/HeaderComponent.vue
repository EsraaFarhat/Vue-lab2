<template>
    <div class="jumbotron">
       <h2>Header Component</h2> 
       <p :class="['lead', branch=='Mansoura' ? 'mans' : '', branch=='Smart' ? 'smart' : '', branch=='Alex' ? 'alex' : '',]">{{iti}} {{branch}} {{branchPostfix}}</p>
    </div>
</template>
<script>
export default {
   data(){
       return{
           iti: "ITI",
           branchPostfix: "branch",
       }
   },
   props:[
       "branch"
    ],
}
</script>
<style scoped>
    .mans{
        color: red;
    }
    .alex{
        color: blue;
    }
    .smart{
        color:brown;
    }
</style>