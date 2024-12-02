<route lang="yaml">
  meta:
    footer:
      enabled: false
  </route>

<script setup lang="ts">
import { privacy } from '/@src/data/pages/privacy'
import { socialLinks } from '/@src/data/blocks/advanced/social'
</script>

<template>
  <div>
    <TermsBlock
      title="Privacy Policy"
      subtitle="You must read through the entire Privacy Policy below and agree with all the details before you use any of our sites."
      updated="Dec 05, 2024"
      image="/assets/illustrations/hero/terms-hero.svg"
      dark-image="/assets/illustrations/hero/terms-hero.svg"
      image-height="1152"
      image-width="517"
      :terms="privacy"
    />

    <FooterD
      text="ForgeFluid | Intelligent Task Automation Platform"
      color="light"
      :social-links="socialLinks"
    />
  </div>
</template>
