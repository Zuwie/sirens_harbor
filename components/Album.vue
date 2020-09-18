<template>
  <div v-editable="blok" class="col-sm-6">
    <v-hover v-slot:default="{ hover }">
      <v-card height="100%" :elevation="hover ? 16 : 2">
        <v-img :src="blok.cover.filename" :height="300"></v-img>
        <v-card-text>
          <v-card-title>{{ blok.title }}</v-card-title>
          <v-card-subtitle>{{ blok.release_date }}</v-card-subtitle>
          <v-card-text>{{ blok.description }}</v-card-text>
        </v-card-text>
      </v-card>
    </v-hover>
  </div>
</template>

<script>
export default {
  name: 'Album',
  props: ['blok'],
}
</script>
<style>
.v-card {
  transition: 0.2s;
}
</style>
