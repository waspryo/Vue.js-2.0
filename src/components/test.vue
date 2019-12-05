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
    <br>
    <input type="text" v-on:keyup="pressKey">
  </div>
</template>

<script>
import func from '../../vue-temp/vue-editor-bridge'
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
      },
      pressKey: function(e) {
          console.log(e.target.value)
      },
      enterHit: function() {
          console.log('You hit enter')
      }
  }
};
</script>

<style scoped>
</style>