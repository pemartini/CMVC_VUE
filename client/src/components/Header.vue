<template>
  <v-card class="overflow-hidden"
  >
    <v-navigation-drawer
      v-model="drawer"
      mini-variant
      expand-on-hover
      src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
      fixed
      permanent
      dark
    >
       <v-list
          dense
          nav
          class="py-0"
        >
          <v-list-item two-line :class="'mini' && 'px-0'">
            <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Application</v-list-item-title>
              <v-list-item-subtitle>Subtext</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <v-divider></v-divider>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.route"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Mapa', icon: 'mdi-map', route: '/' },
          { title: 'Administração', icon: 'mdi-office-building', route: '/about' },
          { title: 'Conta', icon: 'mdi-account', route: '/conta' }
        ],
        mini: true,
      }
    },
    computed: {
        bg () {
          return this.background ? '../assets/viana_vertical.jpg' : undefined
        }
      }
  }
</script>