<template>
  <v-app :dark="darkTheme">
    <v-navigation-drawer
      v-model="drawer"
      :drawer="false"
      :clipped="clipped"
      temporary
      fixed
      app
      right
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar :clipped-left="clipped" fixed app dark>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-switch
        v-model="darkTheme"
        label="Dark Mode"
        @change="switchTheme"
      ></v-switch>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>

    <v-main>
      <nuxt />
    </v-main>

    <v-footer padless app :absolute="!fixed">
      <v-card flat tile dark width="100%" class="lighten-1 text-center">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          &copy; {{ new Date().getFullYear() }} — <strong>Sirens Harbor</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      darkTheme: false,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      right: true,
      title: 'Sirens Harbor',
      icons: ['mdi-home', 'mdi-email', 'mdi-calendar', 'mdi-delete'],
    }
  },
  mounted() {
    this.darkTheme = localStorage.getItem('darkTheme') === 'true'
    this.switchTheme()
  },
  methods: {
    switchTheme() {
      this.$vuetify.theme.dark = this.darkTheme
      localStorage.setItem('darkTheme', this.darkTheme)
    },
  },
}
</script>
