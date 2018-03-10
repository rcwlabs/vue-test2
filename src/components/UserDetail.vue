<template>
    <div>
        <h3>User Detail</h3>
        <p>User Name: {{name}}</p>
        <p>User Age: {{age}}</p>
        <button @click="nameWasReset">Reset Name</button>
    </div>
</template>

<script>
export default {
    props: {
        name: String,
        age: Number
    },
    methods: {
        nameWasReset() {
            this.name = 'Robert';
            this.$emit('nameWasReset', this.name);
        }
    }
}
</script>

