<template>
  <div class="component">
      <h3>User Edit</h3>
      <hr />
      <p>
        User Name: {{name}} | 
        <button @click="changeName">Change Name</button>
      </p>
      <p>
        User Age: {{age}} | 
        <button @click="changeAge">Change Age</button>
      </p>
      <p>
        User Gender: {{gender}} | 
        <button @click="updateGender">Change Gender</button>
      </p>
  </div>
</template>

<script>
export default {
  props: {
      age: Number, 
      name: String, 
      gender: String,
      updateGender: Function
  },
  methods: {
      changeName() {
          this.name = "Nellie",
          this.$emit('changeName', this.name)
      },
      changeAge() {
          this.age = 32,
          this.$emit('changeAge', this.age)
      }
  }
}
</script>

