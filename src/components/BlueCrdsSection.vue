<script>
export default {
    data() {
        return {
            blueCards: [
                {
                    icon: '<i class="fa-solid fa-stopwatch-20"></i>',
                    title: "Team training",
                    second_title: "Find a partner",
                    text: "Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.",
                    arrow_text: "Find a partner"
                },
                {
                    icon: '<i class="fa-solid fa-dumbbell"></i>',
                    title: "Crossfit workout",
                    second_title: "Push your limits",
                    text: "Vestibulum, curabitur eu sem nibh ultrices sit nulla adipiscing. Nisl sit fames amet senectus eget sed duis vehicula. Tristique.",
                    arrow_text: "Learn about Crossfit"
                },
                {
                    icon: '<i class="fa-solid fa-weight-scale"></i>',
                    title: "Weight loss plan",
                    second_title: "Shed those pounds",
                    text: "At laoreet senectus volutpat diam vel sed sed amet pellentesque. Lobortis ut aliquam risus purus. A tellus ut etiam.",
                    arrow_text: "Schedule a workout"
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container-fluid">
        <div class="container">
            <div class="row row-cols-3">
                <div class="col" v-for="(card, i) in blueCards" :key="`cards${i}`">
                    <a href="#0">
                        <div class="my-card">
                            <div v-html="card.icon"></div>
                            <h4>{{ card.title }}</h4>
                            <h5>{{ card.second_title }}</h5>
                            <p>{{ card.text }}</p>
                            <div>{{ card.arrow_text }}<i class="fa-solid fa-chevron-right ms-2"></i></div>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    background-color: $my-black-color;
    padding: 90px;

    .container {

        .col {
            display: flex;
            justify-content: center;

            a {
                text-decoration: none;
                color: $my-white-color;
                border: 4px solid $my-blu-color;
                padding: 50px 20px;
                width: 92%;
                height: 530px;
                display: flex;
                justify-content: center;
                align-items: center;
                transition: transform 0.3s ease-in-out;

                &:hover {
                    transform: scale(1.05);
                    /* Alza il bordo in modo tridimensionale al passaggio del mouse */
                }

                .my-card {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    text-align: center;
                    line-height: 30px;

                    div {
                        &:first-child {
                            font-size: 4rem;
                            margin: 30px 0;
                        }

                        &:last-child {
                            margin: 30px 0;
                        }
                    }

                    h5 {
                        color: $my-yellow-color;
                        margin-bottom: 30px;
                    }

                    p {
                        margin-bottom: 20px;
                    }
                }
            }
        }
    }
}
</style>