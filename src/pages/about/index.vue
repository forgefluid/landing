<route lang="yaml">
  meta:
    footer:
      enabled: false
  </route>

<script setup lang="ts">
import { founders, longTeam } from '/@src/data/blocks/advanced/team'
import { values } from '/@src/data/blocks/advanced/values'
import { genericLargeGallery } from '/@src/data/blocks/gallery'
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

    <Section color="grey">
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

    <!-- <Section color="grey">
      <Container>
        <SectionTitle
          title="Meet the Team"
          subtitle="Talent & Glory"
        />

        <TeamBlockC
          :items="longTeam"
          bubbles
          :limit="20"
        />
      </Container>
    </Section>

    <GalleryBlockB
      :items="genericLargeGallery"
      :limit="2"
    /> -->

    <FooterD
      text="ForgeFluid | Intelligent Task Automation Platform"
      color="light"
      :social-links="socialLinks"
    />
  </div>
</template>
