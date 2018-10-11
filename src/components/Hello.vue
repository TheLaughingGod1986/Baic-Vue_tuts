<template>
  <div class="justify-content-center align-items-center container ">

    <div class="row">
      <div class="col-12">
        <h1>{{ msg }}</h1>
        <p>{{ secondmsg}}</p>
      </div>
    </div>

    <hr/>

    <div class="row">
      <div class="col-12 align-content-center">
        <h2>Total articles: {{ users.length }}</h2>
        <ul class="list-group">
          <li class="list-group-item" v-for="user in users">
            <div class="d-flex w-100 justify-content-between">
              <h5>{{user.firstname}} {{user.lastname}}</h5>
              <small>3 days ago (todo)</small>
            </div>
            <div class="text-justify">
              <p>artical body test here (todo)</p>
              <small>Author (todo)</small>
            </div>
          </li>
        </ul>
      </div>
    </div>

    <hr/>

    <div class="row">
      <div class="col-12 align-content-center">
        <form v-on:submit="sub" action="#" method="post">
          <div class="form-group">
            <div class="col-6">
              <label>Add first name:</label>
              <b-form-input type="text" v-model="input_val_firstName"
                            placeholder="Enter your first name"></b-form-input>
            </div>
            <div class="col-6">
              <label>Add second name:</label>
              <b-form-input type="text" v-model="input_val_secondName"
                            placeholder="Enter your second name"></b-form-input>
            </div>
            <div class="col-6">
              <button type="submit" class="btn btn-primary">Add article</button>
            </div>
          </div>
        </form>
      </div>
    </div>

    <div class="row">
      <div class="col-12 align-content-center">
        <h2>Preview article</h2>
        <strong>Name:</strong>
        <span v-text="input_val_firstName"></span>
        <span v-text="input_val_secondName"></span>
        <h3>log:{{log}}</h3>
      </div>
    </div>

    <hr/>

    <div class="row">
      <div class="col-12 align-content-center">
        <!--<div>-->
        <!--<button onclick="addData()" class="btn btn-primary">Add article</button>-->
        <!--</div>-->
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    methods: {
    },
    name: 'Hello',
    data() {
      return {
        msg: 'Display articles',
        secondmsg: 'This is a blog built in Vue.js.',
        log: "",
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
            firstname: 'Tom',
            lastname: 'bull'
          },
          {
            firstname: 'John',
            lastname: 'Porter'
          }
        ],
        input_val_firstName: '',
        input_val_secondName: '',
        counter: 0
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
