<template>
  <section
    id="ingredients"
    class="hide-overflow"
  >
    <v-layout>
      <v-flex
        xs12
        md6
        text-xs-center
        pa-5
        align-content-space-between
        justify-center
      >

        <base-heading>
          Our Ingredients
        </base-heading>

        <base-text class="mb-1">
          Peek's Golden Butt contains only these ingredients: Zinc Oxide*, Bentonite Clay*, Chamomile Extract*
        </base-text>
        <base-text class="mb-5 font-italic">
          *Organic Ingredients
        </base-text>


          <v-container
            grid-list-md
            pa-3
          >
            <v-layout wrap>
              <v-flex
                v-for="ingredient in ingredients"
                :key="ingredient"
                xs12
                md6
                pa-2
              >

                  <v-img
                    :src="require(`@/assets/${ingredient.img}.jpeg`)"
                    max-height="300"
                  />

                    <div class="title pt-3"
                      v-text="ingredient.name"
                    />
                    <div class="body-1" v-html="ingredient.blurb" />

              </v-flex>
            </v-layout>
          </v-container>

      </v-flex>
      <v-flex
        hidden-sm-and-down
        md6
      >
        <v-img
          :src="require('@/assets/IMG_5302.jpg')"
          height="100%"
        />
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  data: () => ({
    ingredients: [
      {
        name: 'Chamomile',
        img: 'project1',
        blurb: 'A subtle and pleasant smell'
      },
      {
        name: 'Clay',
        img: 'project2',
        blurb: 'Soothes and nourishes'
      },
      {
        name: 'Coconut Oil',
        img: 'project3',
        blurb: 'Hydrates skin'
      },
      {
        name: 'Grapefruit Seed Extract',
        img: 'project4',
        blurb: 'Heals and fortifies'
      }
    ]
  })
}
</script>
