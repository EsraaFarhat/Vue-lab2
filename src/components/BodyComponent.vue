<template>
    <div class="row">
        <table class="table table-striped col-12">
            <thead>
                <tr>
                    <th>#</th>
                    <th>Name</th>
                    <th>City</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="student in students" :key="student.id">
                    <td>{{student.id}}</td>
                    <td>{{student.name}}</td>
                    <td>{{student.city}}</td>
                </tr>
                <tr>
                    <!-- <td colspan="1"><button class="btn btn-primary" @click.prevent="addStudent">Add</button></td> -->
                    <td colspan="1"><addComponent @addBtnClicked="addStudent"/></td>
                    <td colspan="2" class="alert alert-info text-center"><h5> Total number of student {{students.length}}</h5>
                       </td>
                </tr>
            </tbody>
        </table>
    </div>
    
</template>
<script>
import students from '../students.js'
import addComponent from './addComponent.vue'

export default {
    data(){
        return {
            students: students,
            id: null,
        }
    },
    methods:{
        addStudent(targetStudent){
            this.id = this.students[this.students.length-1].id + 1;

            this.students.push({id: this.id ,name: targetStudent.name, city: targetStudent.city});    
        }
    },
    components:{
        addComponent,
    }
}
</script>