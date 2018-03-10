<template>
  <div class="component">
      <h3>User Edit</h3>
      <p>Edit me</p>
      <p>User age: {{age}}</p>
      <button
        @click="editAge">
        Edit Age
      </button>
  </div>
</template>

<script>
export default {
  props: ['age'],
  methods: {
    editAge() {
      this.age = 30;
      this.$emit('ageWasEdited', this.age);
    }
  }
}
</script>

<style scoped>
  div {
    background-color: lightgreen;
  }
</style>
