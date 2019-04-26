<template>
  <div>
    <h1 class="text-center">Create A Post</h1>
    <form @submit.prevent="addPost">
      <div class="row">
        <div class="offset-md-3 col-md-6">
          <div class="form-group">
            <label>Post Title:</label>
            <input type="text" class="form-control" v-model="post.title">
          </div>
        </div>
      </div>
      <div class="row">
        <div class="offset-md-3 col-md-6">
          <div class="form-group">
            <label>Post Body:</label>
            <textarea class="form-control" v-model="post.body" rows="5"></textarea>
          </div>
        </div>
      </div>
      <br>
      <div class="form-group">
        <div class="row">
          <div class="offset-md-3 col-md-6">
            <button class="btn btn-success btn-block">Create</button>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      post: {}
    };
  },
  methods: {
    addPost() {
      let uri = "/api/post/create";
      this.axios.post(uri, this.post).then(response => {
        this.$router.push({ name: "posts" });
      });
    }
  }
};
</script>