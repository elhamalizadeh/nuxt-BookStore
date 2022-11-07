<template>
  <div>
    <section class="main-content columns">
      <aside class="column is-2 section">
        <p class="menu-label is-hidden-touch">
          General
        </p>
        <ul class="menu-list">
          <li
            v-for="(item, key) of items"
            :key="key"
          >
            <NuxtLink
              :to="item.to"
              exact-active-class="is-active"
            >
              <b-icon :icon="item.icon" /> {{ item.title }}
            </NuxtLink>
          </li>
        </ul>
      </aside>

      <div class="container column is-10">
        <Nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        },
        {
          title: 'pages',
          icon: 'home',
          to: { name: 'pages' }
        },
        {
          title: 'Admin',
          icon: 'home',
          to: { name: 'admin' }
        },
        {
          title: 'users',
          icon: 'home',
          to: { name: 'users' }
        },
        {
          title: 'redirect',
          icon: 'home',
          to: { name: 'redirect' }
        }
      ]
    }
  }
}
</script>
