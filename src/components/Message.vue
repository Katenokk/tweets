<template>
  <p v-if="!edit" className="message"> {{message}} </p>
  <input v-else type="text">
</template>

<script>
export default {
    props: {
        message: String,
        edit: Boolean
    },
    edit: false
}
</script>

<style>

</style>