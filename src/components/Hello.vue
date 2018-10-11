<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>{{ secondmsg}}</h3>
    <div>
      <hr/>
      <ul>
        <li v-for="user in users">
          {{user.firstname}} {{user.lastname}}
        </li>
      </ul>
    </div>
    <hr/>

    <div>
      <strong>Input</strong>
      <label>
        <input type="text" v-model="input_val">
      </label>
    </div>

    <div>
      <strong>Output</strong>
      Input Value: <span v-text="input_val"></span>
    </div>
    <hr/>
    <div>
      <button class="btn btn-primary" v-on:click="counter++">Click to count</button>
      {{counter}}
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Hello',
    data() {
      return {
        msg: 'This is injected from js into the template',
        secondmsg: 'Test 2',
        users: [
          {
            firstname: 'Sebastian',
            lastname: 'Eschweiler'
          },
          {
            firstname: 'Bill',
            lastname: 'Smith'
          },
          {
            firstname: 'John',
            lastname: 'Porter'
          }
        ],
        input_val: '',
        counter: 0
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-position: inside;
  }
  a {
    color: #42b983;
  }
</style>
