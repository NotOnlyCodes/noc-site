<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list dense>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-settings</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>NotOnlyCodes</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn text>
          <v-icon left>mdi-finance</v-icon>
          Data Visualization
        </v-btn>
        <v-btn text>
          <v-icon left>mdi-web</v-icon>
          Front-end Development
        </v-btn>
        <v-btn text>
          <v-icon left>mdi-wrench</v-icon>
          QA
        </v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-skype</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-telegram</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-email</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-container
        class="fill-height"
        fluid
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col class="shrink"></v-col>
        </v-row>
      </v-container>
    </v-content>

    <v-footer app>
      <span>&copy; NotOnlyCodes 2020</span>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-github</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-opera</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-npm</v-icon>
      </v-btn>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    props: {
      source: String,
    },

    data: () => ({
      drawer: false,
    }),

    /* created () {
      this.$vuetify.theme.dark = true
    }, */
  }
</script>