<template>
  <section
    id="benefits"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/IMG_5302.jpg')"
          height="100%"
        />
      </v-flex>
      <v-flex
        xs12
        md6
        text-xs-center
        pa-5
      >
        <v-layout
          align-center
          justify-center
          fill-height
          wrap
        >
          <v-flex xs12>

            <base-heading>
              Benefits
            </base-heading>

            <base-text class="mb-5">
              Clay soothes and nourishes, while Zinc creates a moisture barrier to prevent the onset of new rashes.
            </base-text>
          </v-flex>
          <v-flex
            v-for="(service, i) in services"
            :key="i"
            md6
            text-xs-center
            mb-3
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="#92918e"
              size="150"
              tile
            >
              <v-icon
                dark
                size="100"
                v-text="service.icon"
              />
            </v-avatar>
            <base-text>
              <div class="title"
                v-text="service.name"
              />
              <div class="body-1" v-html="service.blurb" />
            </base-text>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    services: [
      {
        name: 'Chamomile',
        icon: 'mdi-flower',
        blurb: 'A subtle and pleasant smell'
      },
      {
        name: 'Beeswax',
        icon: 'mdi-alpha-b-box-outline',
        blurb: 'Natural moisture barrier'
      },
      {
        name: 'Zinc',
        icon: 'mdi-hammer',
        blurb: 'Naturally prevents irritation'
      },
      {
        name: 'Clay',
        icon: 'mdi-square',
        blurb: 'Soothes and nourishes'
      }
    ]
  })
}
</script>
