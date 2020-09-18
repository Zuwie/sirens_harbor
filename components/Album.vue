<template>
  <div class="col-sm-6">
    <v-card height="100%">
      <v-img :src="cover.filename" :height="300"></v-img>
      <v-card-text>
        <v-card-title>{{ title }}</v-card-title>
        <v-card-subtitle>{{ releaseDate }}</v-card-subtitle>
        <v-card-text>{{ description }}</v-card-text>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Album',
  props: {
    cover: {
      type: Object,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      default: 'Missing album-description',
    },
    releaseDate: {
      type: String,
      default: '',
    },
    youtubeSrc: {
      type: String,
      default: '',
    },
  },
}
</script>
