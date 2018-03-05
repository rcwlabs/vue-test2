<template>
    <div>
        <h3>User Detail</h3>
        <p>User Name: {{name}}</p>
    </div>
</template>

<script>
export default {
  props: {
      name: String
  }
}
</script>

