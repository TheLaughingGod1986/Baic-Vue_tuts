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
        <ul class="list-group">
          <li class="list-group-item" v-for="user in users">
            <div class="d-flex w-100 justify-content-between">
              <h5>{{user.firstname}} {{user.lastname}}</h5>
              <small>3 days ago</small>
            </div>
            <div class="text-justify">
            <p>Donec id elit non mi porta gravida at eget metus. Maecenas sed diam eget risus varius blandit.</p>
            <small>Donec id elit non mi porta.</small>
            </div>
          </li>
        </ul>
      </div>
    </div>

    <hr/>

    <div class="row">
      <div class="col-12 align-content-center">
        <form action="">
          <div class="form-group">
            <div class="col-6">
              <label>{{InputFirstN}}</label>
              <b-form-input type="text" v-model="input_val_firstName" placeholder="Enter your first name"></b-form-input>
            </div>
            <div class="col-6">
              <label>{{InputSecondN}}</label>
              <b-form-input type="text" v-model="input_val_secondName" placeholder="Enter your second name"></b-form-input>
            </div>

          </div>
        </form>
      </div>
    </div>

    <div class="row">
      <div class="col-12 align-content-center">
        <lable>{{OutputValue}}</lable>
        <span v-text="input_val_firstName"></span>
        <span v-text="input_val_secondName"></span>
      </div>

    </div>

    <hr/>

    <div class="row">
      <div class="col-12 align-content-center">
        <div>
          <button class="btn btn-primary" v-on:click="counter++">Click to count</button>
          {{counter}}
        </div>
      </div>
    </div>

  </div>
</template>

<script>
  export default {
    name: 'Hello',
    data() {
      return {
        msg: 'This is my vue playground',
        secondmsg: 'learning Vue JS and what I can do.',
        InputFirstN: 'Add first name:',
        InputSecondN: 'Add second name:',
        OutputValue: 'Output name:',
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
