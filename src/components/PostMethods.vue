<template>
  <div>
      <p>Post methods Assignment</p>
      <form @submit="submitData" method="post">
          <input type="text" placeholder="Name" v-model="userData.Name">
          
          <br> <br>
          <input type="text" placeholder="NamPassword" v-model="userData.Password">
          <br>
          <button type="submit">submit</button>

      </form>
  </div>
</template>

<script>
import vue from 'vue'
import axios from 'axios'
import vueAxios from 'vue-axios'
vue.use(axios, vueAxios)
export default {
  name: "PostMethods",
  data() {
      return {
          
          userData: {
              Name: null,
              Password: null
          }
      }
  },
  methods: {
      submitData(e) {
          console.log("asdfghgfd")
          axios.post(`https://secure-refuge-14993.herokuapp.com/login?username=admin&password=admin`, this.userData).then((result)=> {
              console.log(result, "resulttttttt")
              console.log(this.userData)
          })
          console.log(this.userData)
      e.preventDefault()
      }
  }
}
</script>

<style>

</style>