<route lang="yaml">
  meta:
    footer:
      enabled: false
  </route>

<script setup lang="ts">
import { founders } from '/@src/data/blocks/advanced/team'
import { values } from '/@src/data/blocks/advanced/values'
import { socialLinks } from '/@src/data/blocks/advanced/social'
</script>

<template>
  <div>
    <Section color="grey">
      <Container>
        <PageTitle
          title="Meet Our Founders"
          subtitle="The brains behind"
        >
          <template #content>
            <p class="paragraph mx-auto max-w-6">
              Discover the visionaries behind ForgeFluid. Our founders are innovators with a passion for blockchain and AI, dedicated to creating tools that empower developers to shape the future of decentralized technology.
            </p>
          </template>
        </PageTitle>

        <FoundersSection
          :founders="founders"
          :limit="3"
        />
      </Container>
    </Section>

    <Section
      color="grey"
      wave="wave-1"
      shape-color="white"
    >
      <Container>
        <div class="mb-6">
          <SectionTitle
            title="Our Values"
            subtitle="Philosophy"
          />
        </div>

        <ValuesSection
          :values="values"
          image-height="130px"
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
