<template>
  <div class="test">
    <h1>{{title}}</h1>
    <p>{{ user.firstName }}</p>
    <p v-text="user.firstName"></p>
  </div>
</template>

<script>
export default {
  name: "test",
  data() {
    return {
      title: "hello world",
      user: {
          firstName: 'Mike',
          lastName: 'Doe'
      }
    }
  }
};
</script>

<style scoped>
</style>