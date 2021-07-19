<template>
  <div class="bodys">
    <div class="wrapper">
        <StaticPart />
        <Nearby />
    </div>
    <Docker />
  </div>
</template>
<script>
import StaticPart from './Staticpart'
import Nearby from './Nearby.vue'
import Docker from './Docker.vue'
export default {
  name: 'Home',
  components: { StaticPart, Nearby, Docker }
}
</script>
<style lang="scss" scoped>
.bodys {
  padding: 0.15rem 0.17rem;
}
.wrapper {
  overflow-y: auto;
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0.5rem;
  right: 0;
  padding: 0 0.18rem 0.1rem 0.18rem;
}

</style>
