<template>
  <div> <h1>For Api Assignment</h1>
  

       <div v-for="post in posts" v-bind:key="post.id">
      <h2>{{ post.id }}</h2>
      <p>{{ post.title }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  data() {
    return {
      posts: [],
    };
  },



mounted() {
    console.log("sdfgh")
    this.getData()
    console.log(this.posts)
},

  methods: {
    async getData() {
      try {
        const response = await this.$http.get(
              `http://jsonplaceholder.typicode.com/posts`
        );
        // JSON responses are automatically parsed.
        this.posts = response.data;
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>

<style>
</style>