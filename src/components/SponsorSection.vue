<script>
export default {
    data() {
        return {
            cardsSponsor: [
                {
                    image: "../src/assets/imgs/sponsor-1-2x-200x103.png",
                    text: "Tristique aliquam in nullam habitasse nunc, amet vel consectetur. Nulla in suspendisse dolor, aliquet.",
                    arrow_text: "Visit Yoga Studio",
                },
                {
                    image: "../src/assets/imgs/sponsor-2-2x-200x103.png",
                    text: "Feugiat etiam dui mauris pharetra mauris sed pharetra. Convallis sapien ornare cras faucibus nulla porta dui a.",
                    arrow_text: "Join Fitness Center",
                },
                {
                    image: "../src/assets/imgs/sponsor-3-2x-200x103.png",
                    text: "Nisl at quam adipiscing montes, nec, adipiscing commodo aliquam tincidunt. Ligula in habitant et sagittis imperdiet.",
                    arrow_text: "Learn about FC",
                },
                {
                    image: "../src/assets/imgs/sponsor-4-2x-200x103.png",
                    text: "Proin in viverra maecenas et mattis ut nibh enim. Gravida ultricies mi porta lacus. Et posuere velit sed nec eleifend.",
                    arrow_text: "Visit Power Gym",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="row row-cols-4">
            <div class="col" v-for="(card, i) in cardsSponsor" :key="`cards${i}`">
                <a href="#0">
                    <div>
                        <img :src="card.image" alt="image not found">
                    </div>
                    <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                        <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                    </div>
                    <p>{{ card.text }}</p>
                    <div>{{ card.arrow_text }}<i class="fa-solid fa-chevron-right ms-2"></i></div>
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container {
    padding: 100px 0;
    .row {
        .col {
            text-align: center;
            height: 350px;
            padding: 0 20px;

            a {
                text-decoration: none;
                color: $my-black-color;
                height: 100%;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;


                img {
                    width: 156px;
                    margin: 1rem 0;
                }

                .chevron {
                    font-size: 1.3rem;
                    color: $my-blu-color;

                    .my-margin {
                        margin-left: -5px;
                    }
                }

                p {
                    color: $my-gray-color;
                    margin-bottom: 2rem;
                }
            }
        }
    }
}
</style>