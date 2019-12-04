<template>
  <div class="test">
      <input type="text" v-model="title"><br>
    <h1>{{title}}</h1>
    <p v-if="showName">{{ user.firstName }}</p>
    <p v-else>nobody</p>
    <ul>
        <li v-for="item in items">{{ item.title }}</li>
    </ul>
    <button v-on:click="greet('Hello Wolrd')">Say Greeting</button>
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
      showName: true,
      items: [
          {title: 'Item one'},
          {title: 'Item two'},
          {title: 'Item three'},
      ]
    }
  },
  methods: {
      greet: function(greeting) {
          alert(greeting)
      }
  }
};
</script>

<style scoped>
</style>