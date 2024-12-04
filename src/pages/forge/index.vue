<route lang="yaml">
  meta:
    footer:
      enabled: false
  </route>

<script setup lang="ts">
import { features2 } from '/@src/data/blocks/features'
import {
  pricingSplit,
  comparisonTable,
} from '/@src/data/blocks/advanced/pricing'
import { socialLinks } from '/@src/data/blocks/advanced/social'
</script>

<template>
  <div>
    <Section color="grey">
      <Container>
        <PageTitle
          title="Fuel Your Journey with $FORGE"
          subtitle="What is $FORGE token"
          text="$FORGE is the backbone of the ForgeFluid ecosystem, powering seamless transactions, unlocking premium features, and many more."
        />

        <FeatureBlockB
          alignment="centered"
          :features="features2"
          :columns="4"
          :limit="6"
          inverted
        />
      </Container>
    </Section>

    <Section color="grey">
      <Container>
        <PageTitle
          title="Choose the Plan That Fits Your Vision"
          subtitle="Plans Overview"
          text="Explore our tailored plans designed to empower every developer, from beginners to advanced professionals."
        />

        <PricingSplit
          :regular-plans="pricingSplit.regularPlans"
          :premium-plan="pricingSplit.premiumPlan"
          regular-label="Stake $FORGE"
          premium-label="Buy $FORGE"
          regular-sublabel=""
          premium-sublabel=""
        />
      </Container>
    </Section>

    <Section color="grey">
      <Container>
        <SectionTitle
          title="Compare and Choose"
          subtitle="Plan Comparison"
        />

        <ComparisonTable
          :labels="comparisonTable.labels"
          :plans="comparisonTable.plans"
        />
      </Container>
    </Section>

    <FooterD
      text="ForgeFluid | Intelligent Task Automation Platform"
      color="light"
      :social-links="socialLinks"
    />
  </div>
</template>
