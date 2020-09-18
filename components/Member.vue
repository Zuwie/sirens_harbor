<template>
  <v-col v-editable="blok">
    <v-card class="mx-auto" max-width="400" height="100%">
      <v-img
        class="white--text align-end"
        height="200px"
        :src="blok.image.filename"
      >
        <v-card-title>{{ blok.headline }}</v-card-title>
      </v-img>

      <v-card-text class="text--primary">
        <div>{{ blok.body }}</div>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: 'Member',
  props: ['blok'],
}
</script>
