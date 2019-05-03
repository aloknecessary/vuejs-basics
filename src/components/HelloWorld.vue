<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <span>Created for testing purpose @Alok</span>
    <br/><br/>
    <h3>Rendering a list below:</h3>
    <ul>
      <li
        v-for="item in foodList"
        v-bind:key="item.id"
      >{{item.id}} - {{item.text}}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String,
    },
    data() {
      return {
        foodList:[{ id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to eat' }]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 20px;
    line-height: 1.5;
  }
  li {
    display: block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
