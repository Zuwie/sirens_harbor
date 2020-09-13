<template>
  <div>
    <v-container dark>
      <h2 class="text-center text-h2 mb-10">{{ blok.headline }}</h2>
      <v-row>
        <member
          v-for="member in blok.band"
          :key="member._uid"
          :headline="member.name"
          :body="member.body"
          :image="member.image"
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
