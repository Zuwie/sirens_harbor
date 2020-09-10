<template>
  <div v-editable="blok" class="page">
    <component
      :is="blok.component"
      v-for="blokItem in blok.body"
      :key="blokItem._uid"
      :blok="blok"
    >
    </component>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['blok'],
}
</script>
