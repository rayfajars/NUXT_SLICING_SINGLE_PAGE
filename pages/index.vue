<template>
  <div>
    <NavbarSection />
    <HeroSection />
    <SelectWorkSpace />
    <InfoSection />
    <ListCoworkingSection />
    <FooterSection />
  </div>
</template>

<script>
import ListCoworkingSection from '~/components/ListCoworkingSection.vue'
import InfoSection from '~/components/InfoSection.vue'
import SelectWorkSpace from '~/components/SelectWorkSpace.vue'
import HeroSection from '~/components/HeroSection.vue'

export default {
  name: 'IndexPage',
  components: {
    ListCoworkingSection,
    InfoSection,
    SelectWorkSpace,
    HeroSection,
  },
}
</script>
