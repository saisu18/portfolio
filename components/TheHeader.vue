<template>
  <div>
    <v-toolbar flat fixed>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title v-text="title" />
      <v-tabs>
        <v-tab v-for="(item, i) in items" :key="i">
          <v-tooltip bottom>
            <template #activator="{ on, attrs }">
              <v-btn icon nuxt :to="item.to" v-bind="attrs" v-on="on">
                <v-icon>{{ item.icon }}</v-icon>
              </v-btn>
            </template>
            <span>{{ item.title }}</span>
          </v-tooltip>
        </v-tab>
      </v-tabs>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" fixed temporary>
      <v-list nav dense>
        <v-list-item-group>
          <v-list-item v-for="(item, i) in items" :key="i" :to="item.to">
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      title: 'S.Saisu Websites',
      items: [
        {
          icon: 'mdi-home',
          title: 'ホーム',
          to: '/',
        },
        {
          icon: 'mdi-account',
          title: 'About Me',
          to: '/about',
        },
        {
          icon: 'mdi-star',
          title: 'My Skill Set',
          to: '/skill',
        },
        {
          icon: 'mdi-email-edit',
          title: 'Contact',
          to: '/contact',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.v-toolbar__title {
  overflow: visible !important;
  margin-right: 50px !important;
}
.v-app-bar__nav-icon {
  @include display_pc {
    display: none !important;
  }
}
.v-tabs {
  display: none;

  @include display_pc {
    display: block !important;
  }
}
</style>
