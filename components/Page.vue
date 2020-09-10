<template>
  <div v-editable="blok" class="page">
    <v-img :src="blok.hero.filename"></v-img>

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
