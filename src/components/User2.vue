<template>
  <div class="component">
      <h2>This is the main user component</h2>
      <p><button @click="resetName">Reset Name</button></p>
      <p><button @click="resetAge">Reset Age</button></p>
      <p><button @click="resetGender">Reset Gender</button></p>
      <div class="row">
        <div class="col-xs-12 col-med-6">
            <user-detail2
            :age="age"
            :name="name"
            :gender="gender">
            </user-detail2>
        </div>
        <div class="col-xs-12 col-med-6">
            <user-edit2
            :age="age"
            :name="name"
            :gender="gender"
            :updateGender="updateGender"
            @changeName="name = $event"
            @changeAge="age = $event">
            </user-edit2>
        </div>
      </div>
  </div>
</template>

<script>
import UserDetail2 from './UserDetail2'
import UserEdit2 from './UserEdit2'

export default {
  data() {
      return {
          age: 21,
          name: "Robert",
          gender: "Male"
      }
  },
  methods: {
      resetName() {
          this.name = "Robert"
      },
      resetAge() {
          this.age = 21
      },
      resetGender() {
          this.gender = "Male"
      },
      updateGender() {
          this.gender = "Female"
      }
  },
  components: {
      UserDetail2,
      UserEdit2
  }
}
</script>


<style scoped>
    div {
        padding: 1em;
    }
</style>
