<script>
import ServiceSection from "./ServiceSection.vue"
import SocialSection from "./SocialSection.vue"
import MailingSection from "./MailingSection.vue";
import BlueCardsSection from "./BlueCardsSection.vue";
import ArticlesSectionVue from "./ArticlesSection.vue";
import BuySection from './BuySection.vue'

export default {
    components: {
        ServiceSection,
        SocialSection,
        MailingSection,
        BlueCardsSection,
        ArticlesSectionVue,
        BuySection,
    }
}
</script>

<template>
    <div class="service-section-container container-fluid">
        <ServiceSection />
    </div>
    <SocialSection />
    <MailingSection />
    <BlueCardsSection />
    <ArticlesSectionVue />
    <BuySection />
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.service-section-container {
    background: rgb(26, 20, 195);
    background: linear-gradient(140deg, rgba(26, 20, 195, 1) 20%, rgba(186, 4, 43, 1) 80%);
    padding-bottom: 160px;
}
</style>