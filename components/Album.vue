<template>
  <div v-editable="blok" class="col-sm-6">
    <v-card height="100%">
      <v-img :src="blok.filename" :height="300"></v-img>
      <v-card-text>
        <v-card-title>{{ blok.title }}</v-card-title>
        <v-card-subtitle>{{ blok.releaseDate }}</v-card-subtitle>
        <v-card-text>{{ blok.description }}</v-card-text>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Album',
  props: ['blok'],
}
</script>
