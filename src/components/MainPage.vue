<template>
    <section id="container">
        <section id="main">
            <div class="controls">
                <button @click="toggleProfile" class="pill" id="profile-button" v-bind:class="{ active: profileActive}">
                    Profile
                </button>
                <button @click="toggleCourses" class="pill" id="courses-button"
                        v-bind:class="{ active: !profileActive}">
                    Courses
                </button>
            </div>
            <div class="content">
                <ProfileTab :gpa="gpa" class="tab" id="profile-container" v-bind:class="{ active: profileActive}"/>
                <CoursesTab @coursesChanged="coursesChanged" class="tab" id="courses-container"
                            v-bind:class="{ active: !profileActive}"/>
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
                courses: []

            };
        },
        methods: {
            toggleProfile: function () {
                this.profileActive = true;
            },
            toggleCourses: function () {
                this.profileActive = false;
            },

            coursesChanged: function (val) {
                this.courses = val;
            }
        },

        computed: {
            gpa: function () {
                return Math.round(this.courses.reduce(function (total, c) {
                    return total + (c.grade > 60 ? Math.floor((c.grade - 51) / 10) : c.grade > 50 ? 0.5 : 0)
                }, 0) / this.courses.length * 100) / 100

            }
        }
    }
</script>

<style scoped>

</style>
