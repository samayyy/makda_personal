<template>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    </template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'otp',
          to: '/otp1'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'login1',
          to: '/login1'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'home',
          to: '/home'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'allbets',
          to: '/allbets'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'allresults',
          to: '/allresults'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'pastresults',
          to: '/pastresults'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'games',
          to: '/games'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'patti5',
          to: '/patti5'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'patti8',
          to: '/patti8'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'wallet',
          to: '/wallet'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'wallet',
          to: '/withdraw'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'wallet',
          to: '/deposit'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'

    }
  }
}
</script>
