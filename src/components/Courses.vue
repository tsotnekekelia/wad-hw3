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
            <tbody>
            <tr>
                <td>1</td>
                <td>Agile software development</td>
                <td>1</td>
                <td>82</td>
            </tr>
            <tr>
                <td>2</td>
                <td>System modeling</td>
                <td>1</td>
                <td>85</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Object-oriented programming</td>
                <td>2</td>
                <td>99</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Estonian language Level A2</td>
                <td>2</td>
                <td>65</td>
            </tr>
            </tbody>
        </table>
        <button id="add-course-button" class="blue-button">+</button>
        <span id="add-course">
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
        name: "Courses"
    }
</script>

<style scoped>

</style>