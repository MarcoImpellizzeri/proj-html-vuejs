<script>

export default {
    data() {
        return {
            cardsData: [
                {
                    image: "../src/assets/imgs/service6-2x.jpg",
                    title: "Crossfit workout",
                    description: "Push your limits",
                },
                {
                    image: "../src/assets/imgs/box1-2x.jpg",
                    title: "New gym apparel",
                    description: "Look good, feel good",
                },
                {
                    image: "../src/assets/imgs/box3-2x.jpg",
                    title: "Team training",
                    description: "Find a partner",
                },
            ],
        };
    },
}
</script>

<template>
    <div class="container">
        <div class="row row-cols-3 pb-5">
            <div class="col" v-for="(card, i) in cardsData" :key="`card${i}`">
                <div class="card text-bg-dark">
                    <img :src="card.image" class="card-img" alt="...">
                    <div class="card-img-overlay">
                        <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                            <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                        </div>
                        <h3 class="card-title">{{ card.title }}</h3>
                        <h5 class="card-text">{{ card.description }}</h5>
                    </div>
                </div>
            </div>
            <div class="text-container d-flex flex-column align-items-center justify-content-center pt-5 mt-5">
                <h2>
                    “How you respond to the challenge
                    in the second half will determine what you become after the game,
                    whether you are a winner or a loser.”
                </h2>

                <div class="chevron mt-2"><i class="fa-solid fa-chevron-up"></i>
                    <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                </div>

                <div class="d-flex align-items-center">
                    <img class="rounded-circle" src="../assets/imgs/avatar-1-2x.jpg" alt="img avatar">
                    <h5>Brad Johnson</h5>
                    <h5>Las Vegas</h5>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.col {
    z-index: 3;
    margin-top: -80px;
    display: flex;
    justify-content: center;

    img {
        height: 100%;
    }

    .card {
        width: 400px;
        border: 0;
        border-radius: 0 0 40px 0;
        position: relative;
        transition: transform 0.6s, box-shadow 0.3s;

        &:hover {
            /* Effetto di ingrandimento */
            transform: scale(1.05);
            transition: transform 0.6s, box-shadow 0.3s;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.4);
        }

        &::before {
            content: "";
            border-radius: 0 0 40px 0;
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 60%;
            background: rgb(0, 0, 0);
            background: linear-gradient(0deg, rgba(0, 0, 0, 0.8519782913165266) 0%, rgba(241, 255, 0, 0) 100%);
            z-index: 2;
        }

        img {
            border-radius: 0 0 40px 0;
        }

        .card-img-overlay {
            padding: 2rem;
            display: flex;
            justify-content: end;
            flex-direction: column;
            z-index: 2;


            .chevron {
                .my-margin {
                    margin-left: -3px;
                }
            }

            h5 {
                color: $my-yellow-color;
            }
        }
    }
}

.text-container {
    padding: 48px 130px;
    width: 100%;

    h2 {
        color: $my-white-color;
        font-size: 2.6rem;
        text-align: center;
        line-height: 60px;
    }

    .chevron {
        font-size: 1.7rem;
        color: $my-yellow-color;

        .my-margin {
            margin-left: -6px;
        }
    }

    div {
        img {
            width: 60px;
            margin-right: 20px;
        }

        h5 {
            color: $my-white-color;
            margin-right: 20px;


            &:last-child {
                color: $my-gray-color;
            }
        }
    }
}
</style>