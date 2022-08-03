<template>
  <sidebar-menu :menu="menu" :link-component-name="'custom-link'" />


</template>
<script>
import { SidebarMenu } from 'vue-sidebar-menu'
import 'vue-sidebar-menu/dist/vue-sidebar-menu.css'



export default {
  components: {
    SidebarMenu
  },
  data() {
    return {
      menu: [
        {
          header: 'Main Navigation',
          hiddenOnCollapse: true
        },
        {
          href: '/dashboard',
          title: 'Dashboard',
          icon: 'fa fa-user'
        },
        {
          href: '/My Account',
          title: 'My Account',
          icon: 'fa fa-chart-area',
          child: [
            {
              href: '/dashboard',
              title: 'Sub Link'
            }
          ]
        },
        {
          title: 'dashboard',
          child: [
            {
              href: route('dashboard'),
              title: 'dashboard'
            },
            {
              href: route('dashboard'),
              title: 'dashboard'
            }
          ]
        }
      ]
    }
  }
}

import { createApp, h } from 'vue'
import link from '@inertiajs/inertia-vue3/src/link'

const customLink = {
  name: 'CustomLink',
  props: ['item'],
  render() {
    return h(link, this.$slots.default)
  },
  watch: {
    '$page.url'() {
      this.onRouteChange()
    }
  },
  inject: ['onRouteChange']
}

// const app = createApp(App)
// app.component('custom-link', customLink)
</script>