<template>
  <v-container
    v-scroll="onScroll"
    app
    fluid
    fill-height
    style="align-items: start;"
    :class="{ 'pr-0': $vuetify.breakpoint.smAndDown }"
  >
    <NavigationDrawer
      :drawer="drawer"
      @close="drawer = false"
      @register="$router.push({ path: '/', hash: 'register' })"
      @about="$router.push({ path: '/', hash: 'about-us' })"
      @list="drawer = false"
    />
    <TopBar
      value="/search"
      @closeDrawer="drawer=!drawer"
    />

    <v-btn
      v-show="$vuetify.breakpoint.smAndDown"
      light
      tile
      outlined
      class="pa-0 mb-0 ml-0 mt-1 mr-1"
      width="72"
      height="72"
      @click.stop="drawer = !drawer"
    >
      <v-icon>mdi-menu</v-icon>
    </v-btn>
    <v-content>
      <v-row>
        <v-col cols="12">
          <v-card>
            <v-card-text :class="$vuetify.breakpoint.mdAndUp ? 'px-3' : 'pl-3'">
              <ProjectList />
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-content>
    <v-fab-transition>
      <v-btn
        v-if="$vuetify.breakpoint.mdAndUp"
        v-show="offsetTop > 600"
        color="accent"
        dark
        fixed
        bottom
        right
        contained
        fab
        @click="$vuetify.goTo(0)"
      >
        <v-icon color="primary">
          mdi-arrow-up
        </v-icon>
      </v-btn>
    </v-fab-transition>
  </v-container>
</template>
<script>
import { zones } from '~/assets/data'
import ProjectList from '~/components/projectList/ProjectList'
import NavigationDrawer from '~/components/navigation/NavigationDrawer'
import TopBar from '~/components/navigation/TopBar'
export default {
  components: {
    ProjectList,
    TopBar,
    NavigationDrawer
  },
  data () {
    return {
      zones,
      drawer: false,
      offsetTop: 0
    }
  },
  watch: {
    '$route.params' () {}
  },
  mounted () {},
  methods: {
    onScroll (e) {
      this.offsetTop = e.target.scrollingElement.scrollTop
    }
  }
}
</script>
