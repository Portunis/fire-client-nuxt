<template>
<div>

  <div class="container">
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo.slice(0.1)"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardInfo.slice(0.1)"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</div>
</template>

<script>
import  { largeCardSections, smallCardSections} from '@/assets/data.js'
import LargeCardDisplay from "~/components/LargeCardDisplay";
import SmallCardDisplay from "~/components/SmallCardDisplay";
export default {
  name: "index",
  layout: 'default',
  components: {SmallCardDisplay, LargeCardDisplay},
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style scoped>

</style>
