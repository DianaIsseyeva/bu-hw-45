<template>
  <div class="row">
    <form @submit.prevent="handleSubmit">

      <v-input v-model="ifirstname" label="First name"></v-input>

      <v-input v-model="ilastname" label="Last name"/>
      
      <v-input v-model="icountry" label="Country"/>
      
      <v-input v-model="icity" label="City"/>

      <v-input v-model="iage" label="Age"/>

      <div class="btn">
        <button>Save data</button>
      </div>

    </form>

    <div>
      <h3>User data:</h3>
      <p>First name: {{ firstname }}</p>
      <p>Last name: {{ lastname }}</p>
      <p>Country: {{ country }}</p>
      <p>City: {{ city }}</p>
      <p>Age: {{ age }}</p>
    </div>
    
  </div>
</template>

<script>
import vInput from './v-input.vue'
  export default {
    components: {
      vInput
    },
    data() {
      return {
        firstname: '',
        lastname: '',
        country: '',
        city: '',
        age: '',
        ifirstname: '',
        ilastname: '',
        icountry: '',
        icity: '',
        iage: '',
      }
    },
    methods: {
      handleSubmit() {
        this.firstname = this.ifirstname
        this.lastname = this.ilastname
        this.country = this.icountry
        this.city = this.icity
        this.age = this.iage
        this.ifirstname = ''
        this.ilastname = ''
        this.icountry = ''
        this.icity = ''
        this.iage = ''
      }
    }
  }
</script>

<style>
  .row {
    display: flex;
    justify-content: center;
  }
  form {
    min-width: 300px;
    margin: 20px 50px;
    background: rgb(202, 166, 243);
    text-align: left;
    padding: 20px;
    border-radius: 10px;
  }
  label {
    color: rgb(102, 50, 139);
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 16px;
  }
  input {
    display: block;
    padding: 10px 5px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: grey;
  }
  button {
    background: rgb(146, 87, 195);
    border: 0;
    padding: 10px 40px;
    margin: 20px auto;
    color: white;
    border-radius: 20px;
  }
  .btn {
    text-align: center;
  }
</style>