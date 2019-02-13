<template>
  <v-toolbar
    v-scroll="onScroll"
    :color="isTransparent ? 'transparent' : '#F5F5F5'"
    app
    flat
  >
  <v-hover>
    <v-img
      :src="`${hover? require('@/assets/peeksgolden_logo-red.svg'): require('@/assets/peeksgolden_logo.svg')}`"
      max-height="50px"
      position="top left"
      contain
      slot-scope="{ hover }"
    />
  </v-hover>
    <v-spacer />
    <v-menu class="hidden-md-and-up">
        <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
        <v-list>
          <v-list-tile v-for="item in items">
            <v-list-tile-content>
              <v-list-tile-title v-on:click="scrollTo" :value="item.target">{{ item.name }}</v-list-tile-title>
             </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-menu>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn
        flat
        v-for="item in items"
        v-on:click="scrollTo"
        :value="item.target"
        class="caption"
      >
        {{ item.name }}
      </v-btn>
    </v-toolbar-items>

  </v-toolbar>
</template>

<script>
import * as easings from 'vuetify/es5/util/easing-patterns'
import goTo from 'vuetify/lib/components/Vuetify/goTo'
export default {
  components: {
    SocialMedia: () => import('@/components/SocialMedia')
  },

  props: {
    large: {
      type: Boolean,
      default: false
    }
  },

  data: () => ({
    duration: 300,
    offset: 0,
    easing: 'easeInOutCubic',
    easings: Object.keys(easings),
    isTransparent: true,

    items: [
      {
        name: 'Welcome',
        target: '#welcome',
      },
      {
        name: 'Ingredients',
        target: '#ingredients',
      },
      {
        name: 'About Us',
        target: '#about',
      },
      {
        name: 'Get In Touch',
        target: '#get-in-touch',
      }
    ]
  }),

  computed: {
    options () {
      return {
        duration: this.duration,
        offset: this.offset,
        easing: this.easing
      }
    }
  },

  methods: {
    onScroll () {
      this.isTransparent = window.pageYOffset < 200
    },
    scrollTo (event) {
      //console.log(event.target.value);
      this.$vuetify.goTo(event.target.value);
    }
  }
}
</script>
