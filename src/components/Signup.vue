<template>
  <div>
    EMAIL: <input type="text" v-model="email" /><br/>
    PASSWORD: <input type="text" v-model="password" /><br/>
    <button @click="signup">signup</button>
  </div>
</template>
<script>

import axios from 'axios';

export default {
  name: 'Signup',
  data() {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    signup(){
      let newUser = {
        email: this.email,
        password: this.password
      }
      axios.post('http://localhost:5000/', newUser)
    }
  }
}
</script>


 