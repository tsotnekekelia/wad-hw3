<template>
    <div id="courses-container" class="tab active">
        <h1 class="title">Courses</h1>
        <table id="courses">
            <thead>
            <tr>
                <th>#</th>
                <th>Course Title</th>
                <th>Semester</th>
                <th>Grade</th>
            </tr>
            </thead>
            <tbody v-for="(course, index) in courses" v-bind:key="course.name">
            <tr>
                <td>{{index}}</td>
                <td>{{course.name}}</td>
                <td>{{course.semester}}</td>
                <td>{{course.grade}}</td>
            </tr>
            </tbody>
        </table>
        <button @click="toggleAdding()" id="add-course-button" class="blue-button">+</button>
        <span v-if="courseOpen" id="add-course">
                                <input class="input" type="text" placeholder="Course title" id="title">
                                <input class="input" type="number" min="1" max="8" placeholder="Semester" id="semester">
                                <input class="input" type="number" min="0" max="100" placeholder="Grade" id="grade">
                                <button class="green-button" id="save-course">Save</button>
                                <button class="grey-button" id="cancel-course">Cancel</button>
                            </span>
    </div>
</template>

<script>
    export default {
        name: "Courses",
        data: function () {
            return {
                courseOpen: false,
                courses: [
                    {
                        name: "Agile Software Development",
                        semester: 1,
                        grade: 82
                    },
                    {
                        name: "System modeling",
                        semester: 1,
                        grade: 85
                    },
                    {
                        name: "Object-oriented programming",
                        semester: 2,
                        grade: 99
                    },
                    {
                        name: "Estonian language A2",
                        semester: 2,
                        grade: 65}
                ]
            }
        },
        methods: {
            toggleAdding: function () {
                this.courseOpen = !this.courseOpen
            },
            addRow: function () {

            }
        }
    }
</script>

<style scoped>

    #courses{
        margin-bottom: 30px;
    }

    input, button{
        margin: 0 5px;
    }
</style>