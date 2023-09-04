<script>
import ServiceSection from "./ServiceSection.vue"
import SocialSection from "./SocialSection.vue"
import MailingSection from "./MailingSection.vue";
import BlueCardsSection from "./BlueCardsSection.vue";
import ArticlesSectionVue from "./ArticlesSection.vue";
import BuySection from './BuySection.vue'
import SponsorSection from './SponsorSection.vue'
import WorkoutSection from "./WorkoutSection.vue";

export default {
    components: {
        ServiceSection,
        SocialSection,
        MailingSection,
        BlueCardsSection,
        ArticlesSectionVue,
        BuySection,
        SponsorSection,
        WorkoutSection,
    }
}
</script>

<template>
    <ServiceSection />
    <SocialSection />
    <MailingSection />
    <BlueCardsSection />
    <ArticlesSectionVue />
    <BuySection />
    <SponsorSection />
    <WorkoutSection />
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

</style>