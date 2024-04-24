<script>
export default {
  methods: {
    save() {}
  }
}
</script>

<template>
  <!-- OK -->
  <input @keydown.ctrl.enter.exact="save()" />
  <!-- OK -->
  <input @keydown.stop />
  <!-- ERROR - Fails with vue/use-v-on-exact -> Consider to use '.exact' modifier on the @keydown.stop line -->
  <input
    @keydown.ctrl.enter.exact="save()"
    @keydown.stop
  />
</template>
