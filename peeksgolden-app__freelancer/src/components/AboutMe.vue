<template>
  <section
    id="about"
    class="hide-overflow"
  >
    <v-layout
      white
      align-center
      justify-center
      fill-height
    >
    <v-flex
      hidden-sm-and-down
      md6
    >
      <v-img
        :src="require('@/assets/DSC0319.jpg')"
        height="100%"
      />
    </v-flex>
      <v-flex
        xs12
        md6
        pa-5
      >

        <base-heading class="info--text">
          About Us
        </base-heading>

        <base-text class="mb-5">
          We are a Mom & Pop owned shop. We developed Peek's Golden Butt to ensure only the best and most natural ingredients made it onto our baby's butt.
        </base-text>

        <base-subheading class="info--text">
          Our Guarantee
        </base-subheading>
        <base-text class="mb-5">
          If you don't think our butt cream is the best, send it back for a full refund.
        </base-text>

        <!--<v-alert
          outlined
          color="info"
        >
          <v-layout
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
            wrap
          >
            <v-flex
              xs6
              text-uppercase
              v-text="skill.name"
            />
            <v-flex
              xs6
              text-xs-right
              v-text="`${skill.value}%`"
            />
            <v-progress-linear
              :value="skill.value"
              color="info"
              height="8"
            />
          </v-layout>
        </v-alert>-->
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    skills: [
      {
        name: 'Web Design',
        value: 100
      },
      {
        name: 'Web Development',
        value: 75
      },
      {
        name: 'Web Support',
        value: 90
      }
    ]
  })
}
</script>
