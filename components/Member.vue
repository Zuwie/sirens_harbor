<template>
  <v-col>
    <v-card class="mx-auto" max-width="400" height="100%">
      <v-img class="white--text align-end" height="200px" :src="image.filename">
        <v-card-title>{{ headline }}</v-card-title>
      </v-img>

      <v-card-text class="text--primary">
        <div>{{ body }}</div>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: 'Member',
  props: {
    headline: {
      type: String,
      default: 'Headline missing',
    },
    body: {
      type: String,
      default: 'Body missing',
    },
    image: {
      type: Object,
      default: () => {
        return {
          filename: '',
        }
      },
    },
  },
}
</script>
