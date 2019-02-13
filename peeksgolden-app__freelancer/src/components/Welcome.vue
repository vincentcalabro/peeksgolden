<template>
  <section
    id="welcome"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/DSC01700_3.jpg')"
          height="100vh"
          position="center center"
        />
      </v-flex>

      <v-flex
        xs12
        md6
        align-center
        layout
        :pa-5="$vuetify.breakpoint.smAndDown"
        wrap
      >


        <v-layout
          align-content-space-between
          justify-center
          column
        >
          <v-flex
            xs12
            hidden-md-and-up
          >
            <v-img
              :src="require('@/assets/Cover_Pic.png')"
              height="35vh"
            />
          </v-flex>
          <v-flex
            xs10
            md8
            :pl-5="$vuetify.breakpoint.mdAndUp"
            text-xs-center
            text-sm-center
            text-md-left
          >
            <base-heading>Peek's Golden Butt Cream</base-heading>
            <base-text>
              Ultimate comfort for your little ones little butt.
            </base-text>
            <base-btn class="mt-4">
              Learn More
            </base-btn>
          </v-flex>
        </v-layout>


      </v-flex>
    </v-layout>
  </section>
</template>
