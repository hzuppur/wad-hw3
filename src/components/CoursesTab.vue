<template>
  <div>
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
    <br>
    <br>
    <div>
      <button class="blue-button" id="add-course-button">+</button>
      <span id="add-course">
                                <input class="input" id="title" placeholder="Course title" type="text">
                                <input class="input" id="semester" max="8" min="1" placeholder="Semester" type="number">
                                <input class="input" id="grade" max="100" min="0" placeholder="Grade" type="number">
                                <button class="green-button" id="save-course">Save</button>
                                <button class="grey-button" id="cancel-course">Cancel</button>
                            </span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "CoursesTab"
  }
</script>

<style scoped>

</style>