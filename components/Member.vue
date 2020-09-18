<template>
  <div v-editable="blok" class="col-sm-6">
    <v-card height="100%">
      <v-img class="white--text align-end" :src="blok.image.filename">
        <v-card-title>{{ blok.name }}</v-card-title>
      </v-img>
      <v-card-text>{{ blok.body }}</v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Member',
  props: ['blok'],
}
</script>
