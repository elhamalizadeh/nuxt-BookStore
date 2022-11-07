<template>
  <div>
    <h1 class="header">List of users</h1>
      <div class="col-6 gy-5" v-for="user in users" :key="user.id">
 <usercardview :user="user" />
    </div>
    </div>
</template>
<script>
import axios from 'axios'
import { ref } from 'vue'
import usercardview from '@/components/usercardview.vue'
export default {
  name: 'users',
  components: {
    usercardview
  },
  setup () {
    const users = ref([])
    function getusers () {
      axios.get('https://jsonplaceholder.typicode.com/users').then(function (response) {
        users.value = (response.data)
      }).catch(function (error) {
        console.log(error)
      })
    }
    getusers()
    return { users }
  }
}
</script>
