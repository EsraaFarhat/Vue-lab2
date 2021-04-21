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
                <tr class="alert alert-info text-center">
                    <td colspan="1"><button class="btn btn-primary" @click.prevent="addStudent">Add</button></td>
                    <td colspan="2"><h3> Total number of student {{students.length}}</h3>
                       </td>
                </tr>
            </tbody>
        </table>
    </div>
    
</template>
<script>
import students from '../students.js'

export default {
    data(){
        return {
            students: students,
            dummyStudents:[
                {name:"Aya", city:"Cairo"},
                {name:"Ahmed", city:"Alex"},
                {name:"Ali", city:"Cairo"},
                {name:"Mohamed", city:"Mansoura"},
            ],
            index:0,
            targetStudent: null,
            id: null,
        }
    },
    methods:{
        addStudent(){
            if(this.index >= this.dummyStudents.length) return;

            this.targetStudent= this.dummyStudents[this.index];
            this.id = this.students[this.students.length-1].id + 1;

            this.students.push({id: this.id ,name: this.targetStudent.name, city: this.targetStudent.city});
            
            this.index++;
        }
    }
}
</script>