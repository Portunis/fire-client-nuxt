<template>
<div>

  <div class="container">

    <Hero/>
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardSections"
      :key="cardInfo.id"
      :cardsSection="cardInfo"
    />
  </div>
</div>
</template>

<script>
import {largeCardSections, smallCardSections} from '@/assets/data.js'
import Hero from "~/components/Hero";
import LargeCardDisplay from "~/components/LargeCardDisplay";
import SmallCardDisplay from "~/components/SmallCardDisplay";

export default {
  layout: 'default',
  components: {SmallCardDisplay, LargeCardDisplay, Hero},
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections
    }
  }

}
</script>
