<template>
    <button class="btn btn-primary" @click.prevent="addEvent">Add</button>
</template>
<script>
export default {
     data(){
        return {
            dummyStudents:[
                {name:"Aya", city:"Cairo"},
                {name:"Ahmed", city:"Alex"},
                {name:"Ali", city:"Cairo"},
                {name:"Mohamed", city:"Mansoura"},
            ],
            index:0,
            targetStudent: null,
        }
    },
    methods:{
        addEvent(){
            if(this.index >= this.dummyStudents.length) return;

            this.targetStudent= this.dummyStudents[this.index];
            this.index++;
            this.$emit("addBtnClicked", this.targetStudent);
        }
    }
}
</script>