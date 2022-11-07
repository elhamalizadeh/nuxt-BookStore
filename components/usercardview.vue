<template>
<div class="card">
  <div class="card-content">
    <div class="media">
      <div class="media-content">
        <p class="title is-4">{{user.name}}</p>
        <p class="subtitle is-6">{{user.username}}</p>
      </div>
    </div>

    <div class="content">
     Address: {{user.address}}
      <br>
      <time datetime="2016-1-1">{{user.email}}</time>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'CardView',
  props: {
    user: Object
  }

}
</script>
