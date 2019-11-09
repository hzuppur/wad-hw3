<template>
  <section id="container">
    <section id="main">
      <div class="content">
        <ProfileTab class="tab" id="profile-container" v-bind:class="{ active: profileActive}"/>
        <CoursesTab class="tab" id="courses-container" v-bind:class="{ active: !profileActive}"/>
      </div>
      <div class="controls">
        <button @click="toggleProfile" class="pill" id="profile-button" v-bind:class="{ active: profileActive}">
          Profile
        </button>
        <button @click="toggleCourses" class="pill" id="courses-button" v-bind:class="{ active: !profileActive}">
          Courses
        </button>
      </div>
    </section>
  </section>
</template>

<script>
  import ProfileTab from "./ProfileTab";
  import CoursesTab from "./CoursesTab";
  export default {
    name: "MainPage",
    components: {CoursesTab, ProfileTab},
    data: () => {
      return {
        profileActive: true,
      };
    },
    methods: {
      toggleProfile: function () {
        this.profileActive = true;
      },
      toggleCourses: function () {
        this.profileActive = false;
      }
    }
  }
</script>

<style scoped>

</style>