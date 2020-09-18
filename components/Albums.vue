<template>
  <div v-editable="blok">
    <v-container>
      <h2 class="text-center text-h2 mb-10">{{ blok.headline }}</h2>
      <v-row>
        <album
          v-for="blok in blok.albums"
          :key="blok._uid"
          :blok="blok"
        ></album>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Album from '@/components/Album'

export default {
  components: { Album },
  props: ['blok'],
}
</script>
