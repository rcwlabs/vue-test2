<template>
  <div class="component">
      <h3>User Detail</h3>
      <hr />
      <p>User name: {{name}}</p>
      <p>User age: {{age}}</p>
      <p>User gender: {{gender}}</p>
  </div>
</template>

<script>
export default {
  props: ['age', 'name', 'gender']
}
</script>
