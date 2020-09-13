<template>
  <div v-editable="blok">
    <v-container fill-height>
      <v-row>
        <v-col>
          <h1>{{ blok.headline }}</h1>
          <p>{{ blok.body }}</p>
        </v-col>
        <v-col>
          <v-img
            :src="blok.about_img.filename"
            :alt="blok.about_img.alt"
          ></v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  props: ['blok'],
}
</script>

<style scoped></style>
