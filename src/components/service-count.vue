<template>
  <span>[ {{count}} ]</span>
</template>

<script>
export default {
  props: ['region', 'service', 'collection'],
  computed: {
    count () {
      return this.$store.getters.collItem(this.region, this.service, this.collection).items.length
    }
  }
}
</script>
