<script>
export default {
    data() {
        return {
            cardsVideos: [
                {
                    image: "../src/assets/imgs/video2-2x.jpg",
                    title: "Thighs & glute workout",
                    text: "Increase your mobility",
                },
                {
                    image: "../src/assets/imgs/video7-2x.jpg",
                    title: "Lift, firm & perk up",
                    text: "Feel young again",
                },
                {
                    image: "../src/assets/imgs/video9-2x.jpg",
                    title: "Slim & trim your waist",
                    text: "Shed those extra pounds",
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container-fluid d-flex">
        <div class="container-l">
            <div class="card text-bg-dark">
                <img src="../assets/imgs/service15-2x.jpg" class="card-img" alt="img not found">
                <div class="card-img-overlay">
                    <div>
                        <button class="btn-play rounded-circle"><i class="fa-solid fa-play"></i></button>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-r">
            <h3 class="my-2">Tune up your workouts</h3>
            <h1 class="my-2">The best health & fitness advice online</h1>
            <h4 class="my-2">Arcu eu facilisi ut quisque placerat nunc habitant. Magna semper mauris, venenatis, leo integer
                sit pellentesque.</h4>
            <div>
                <button class="my-btn ms-0 m-3"><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="d-flex justify-content-between align-items-center px-2">
            <h3 class="m-0">Featured playlists</h3>
            <a href="#0">View all videos <i class="fa-solid fa-chevron-right ms-2"></i></a>
        </div>
        <div class="row row-cols-3 py-5">
            <div class="col" v-for="(card, i) in cardsVideos" :key="`card${i}`">
                <div class="card">
                    <a href="#0" class="img-position">
                        <img :src="card.image" class="card-img-top" alt="...">
                        <button class="btn-play rounded-circle"><i class="fa-solid fa-play"></i></button>
                    </a>
                    <div class="card-body text-center">
                        <h4 class="card-title">{{ card.title }}</h4>
                        <p class="card-text">{{ card.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    .container-l {
        width: 50%;

        .card {
            width: 100%;
            border: 0;
            border-radius: 0 0 40px 0;
            transition: transform 0.6s, box-shadow 0.3s;
            margin-top: -60px;
            margin-left: -25px;

            img {
                border-radius: 0 0 40px 0;
                height: 780px;
                object-fit: cover;
            }

            .card-img-overlay {
                display: flex;
                justify-content: center;
                align-items: center;
                z-index: 2;

                .btn-play {
                    border: 0;
                    color: $my-blu-color;
                    padding: 35px 40px;
                    background-color: $my-white-color;
                    font-size: 1.1rem;
                    transition: 0.3s;

                    &:hover {
                        transition: 0.3s;
                        color: $my-red-color;
                    }
                }
            }
        }
    }

    .container-r {
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 50%;
        padding: 0 100px;

        h3 {
            color: $my-blu-color;
        }

        h1 {
            color: $my-black-color;
            font-size: 3.8rem;
            padding: 2rem 0;
        }

        h4 {
            color: $my-gray-color;
        }

        .chevron {
            font-size: 1.7rem;
            color: $my-yellow-color;

            .my-margin {
                margin-left: -6px;
            }
        }

        .my-btn {
            background-color: red;
            font-size: 1rem;
            padding: 16px 40px;

            &:hover {
                transition: 0.5s;
                background-color: $my-red-color;
            }
        }
    }
}

.container {
    padding: 110px 0;

    a {
        text-decoration: none;
        color: $my-black-color;
        transition: 0.3s;

        &:hover {
            transition: 0.3s;
            color: $my-blu-color;
        }

        i {
            font-size: .7rem;
        }
    }

    .col {
        display: flex;
        justify-content: center;

        .card {
            border: 0;
            width: 406px;

            .img-position {
                position: relative;

                img {
                    border-radius: 0 0 20px 0;
                }

                .btn-play {
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    border: 0;
                    color: $my-blu-color;
                    padding: 15px 20px;
                    background-color: $my-white-color;
                    font-size: .8rem;
                }
            }
            
            .card-body {
                p {
                    color: $my-blu-color;
                }
            }
        }
    }
}
</style>