<template>
<div class="container">
  <MyItem
    v-for="item in myRentals"
    :key="item.id"
    :item="item"
  />
</div>
</template>

<script>
import {mapState} from 'vuex'
import MyItem from "~/components/MyItem";
export default {
  name: "my-items",
  components: {MyItem},
  computed: {
    ...mapState(['myRentals'])
  }

}
</script>

<style scoped>

</style>
