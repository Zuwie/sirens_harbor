<template>
  <div v-editable="blok" class="page">
    <v-parallax
      dark
      height="800"
      :src="blok.hero.filename"
      :alt="blok.hero.alt"
      gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-1 mb-4">Sirens Harbor</h1>
          <h4 class="subheading">Build your application today!</h4>
        </v-col>
      </v-row>
    </v-parallax>

    <v-container>
      <component
        :is="blok.component"
        v-for="blok in blok.body"
        :key="blok._uid"
        :blok="blok"
      ></component>
    </v-container>
  </div>
</template>

<script>
export default {
  props: ['blok'],
}
</script>
