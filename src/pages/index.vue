<route lang="yaml">
  meta:
    footer:
      enabled: false
  </route>

<script setup lang="ts">
// import { starterTemplates } from '/@src/data/pages/development'
import { techLogos } from '/@src/data/pages/logos'
import { socialLinks } from '/@src/data/blocks/advanced/social'
import { conferenceSchedule } from '/@src/data/pages/conference'
</script>

<template>
  <div>
    <HeroT1 />

    <Section
      color="grey"
      wave="wave-1"
      shape-color="white"
    >
      <Container>
        <TimelineTitle
          title="Crafting the beginning"
          subtitle="Craft"
          minititle="Explore our stack"
          color="secondary"
          :step="1"
        >
          <template #content>
            <div class="py-6 mx-auto max-w-9">
              <div class="columns b-columns-half-tablet-p">
                <div class="column is-6">
                  <p class="paragraph">
                    Craft smart contracts effortlessly with ForgeFluid. Our AI turns your ideas into secure, deployable
                    code for tokens, DAOs, and DeFi—fast and flawless.
                  </p>
                </div>
                <div class="column is-6">
                  <p class="paragraph">
                    Simplify contract creation. ForgeFluid delivers optimized, blockchain-ready code instantly,
                    empowering you to build with speed and precision.
                  </p>
                </div>
              </div>
            </div>
          </template>
        </TimelineTitle>

        <DevWindows />

        <TimelineTitle
          title="Tailor your Application"
          subtitle="Tailor"
          minititle="Works with many stacks"
          color="primary"
          :step="2"
        >
          <template #subheading>
            <div class="is-flex is-justify-content-center py-4">
              <AvatarGroup
                :avatars="techLogos"
                :limit="5"
                boxed
              />
            </div>
          </template>
          <template #content>
            <div class="py-6 mx-auto max-w-9">
              <div class="columns b-columns-half-tablet-p">
                <div class="column is-6">
                  <p class="paragraph">
                    Tailor your smart contracts with precision. ForgeFluid lets you customize libraries, frameworks, and
                    coding styles to match your exact needs.
                  </p>
                </div>
                <div class="column is-6">
                  <p class="paragraph">
                    Shape every detail. Adjust workflows, refine logic, and align your contracts with your vision
                    effortlessly.
                  </p>
                </div>
              </div>
            </div>
          </template>
        </TimelineTitle>

        <Timeline />

        <TimelineTitle
          title="Deploy with Confidence"
          subtitle="Deploy"
          color="accent"
          :step="3"
        >
          <template #content>
            <div class="py-6 mx-auto max-w-9">
              <div class="columns b-columns-half-tablet-p">
                <div class="column is-6">
                  <p class="paragraph">
                    Launch your smart contracts seamlessly with ForgeFluid. Our platform ensures every project is blockchain-ready, deployable across networks, and optimized for performance and security.
                  </p>
                </div>
                <div class="column is-6">
                  <p class="paragraph">
                    ForgeFluid simplifies deployment with one-click solutions and real-time validations. From testnets to mainnets, deploy smarter, faster, and with total assurance.
                  </p>
                </div>
              </div>
            </div>
          </template>
        </TimelineTitle>

        <GlobeStats />

        <TimelineTitle
          title="The Roadmap"
          subtitle="Schedule"
          minititle=""
          color="primary"
          :step="4"
        />
        <br>
        <EventSchedule :schedule="conferenceSchedule" />
      </Container>
    </Section>

    <!-- <Section>
      <template #background>
        <SectionMap light />
      </template>
      <Container>
        <CompanyGrid title="We help people work faster at" :logos="customerLogos" :limit="20" />
      </Container>
    </Section> -->

    <FooterD
      text="ForgeFluid | Intelligent Task Automation Platform"
      color="light"
      :social-links="socialLinks"
    />
  </div>
</template>
