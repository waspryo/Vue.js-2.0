<template>
  <div class="test">
    <h1>{{title}}</h1>
    <p v-if="showName">{{ user.firstName }}</p>
    <p v-else="showName">nobody</p>
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
      },
      showName: true
    }
  }
};
</script>

<style scoped>
</style>