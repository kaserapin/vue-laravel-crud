<template>
  <div class="row justify-content-center">
    <div class="col-md-12">
      <h1 class="text-center mt-5">{{description}}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      description:
        "This is an app that is built using laravel backend api and vue js for frontend."
    };
  },
  mounted() {
    console.log("Component mounted.");
  }
};
</script>