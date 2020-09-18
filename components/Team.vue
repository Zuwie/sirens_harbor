<template>
  <div v-editable="blok">
    <v-container>
      <h2 class="text-center text-h2 mb-10">{{ blok.headline }}</h2>
      <v-row>
        <member
          v-for="blok in blok.band"
          :key="blok._uid"
          :blok="blok"
        ></member>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Member from '@/components/Member'

export default {
  components: { Member },
  props: ['blok'],
}
</script>
