<template>
  <div>
    <v-container>
      <h2 class="text-center text-h2 mb-10">{{ blok.headline }}</h2>
      <v-row>
        <album
          v-for="album in blok.albums"
          :key="album._uid"
          :headline="album.name"
          :body="album.body"
          :image="album.image"
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
