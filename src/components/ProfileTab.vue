<template>
  <div>
    <div id="profile">
      <div class="avatar">
        <img alt="My picture" id="picture" src="./../assets/me.png">
      </div>
      <div class="info">
        <ul>
          <li id="name">John Doe</li>
          <li id="birthdate">11/10/1990</li>
          <li id="faculty">Software Engineering</li>
        </ul>
      </div>
      <div id="gpa">
        <strong>2.75</strong>
      </div>
      <div class="clear-fix"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "ProfileTab",
  }
</script>

<style scoped>

</style>