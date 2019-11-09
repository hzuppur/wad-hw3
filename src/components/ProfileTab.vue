<template>
  <div>
    <div id="profile">
      <div class="avatar">
        <img alt="My picture" id="picture" src="./../assets/me.png">
      </div>
      <div class="info">
        <ul>
          <li id="name">{{ guy.firstname }} {{ guy.lastname }}</li>
          <li id="birthdate">{{ guy.birthdate }}</li>
          <li id="faculty">{{ guy.faculty }}</li>
        </ul>
      </div>
      <div id="gpa">
        <strong>{{ guy.gpa }}</strong>
      </div>
      <div class="clear-fix"></div>
    </div>
  </div>
</template>

<script>
  import User from "../classes/User"
  export default {
    name: "ProfileTab",

    data: function() {
      return {
        guy: new User('John', 'Doe', '11/10/1990', 'Software Engineering', 0)
      }
    },

    props: {
      gpa: Number
    },

    watch: {
      gpa: function (val) {
        this.guy.gpa = val;
      }
    }
  }
</script>

<style scoped>

</style>
