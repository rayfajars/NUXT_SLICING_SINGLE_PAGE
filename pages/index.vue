<template>
  <div>
    <NavbarSection />
    <SelectWorkSpace />
    <InfoSection />
    <ListCoworkingSection />
    <FooterSection />
  </div>
</template>

<script>
import NavbarSection from '~/components/NavbarSection.vue'
import ListCoworkingSection from '~/components/ListCoworkingSection.vue'
import FooterSection from '~/components/FooterSection.vue'
import InfoSection from '~/components/InfoSection.vue'
import SelectWorkSpace from '~/components/SelectWorkSpace.vue'

export default {
  name: 'IndexPage',
  components: {
    NavbarSection,
    ListCoworkingSection,
    FooterSection,
    InfoSection,
    SelectWorkSpace
},
}
</script>
