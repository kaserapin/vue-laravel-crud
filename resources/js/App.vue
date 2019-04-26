<template>
  <div class="navigation">
    <nav class="navbar navbar-expand-sm bg-light navbar-light shadow">
      <div class="container">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link to="/" class="nav-link">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/create" class="nav-link">Create Post</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/posts" class="nav-link">Posts</router-link>
          </li>
        </ul>
      </div>
    </nav>
    <br>
    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>


<script>
export default {};
</script>