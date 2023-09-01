<script>
export default {
    data() {
        return {
            cardsVideos: [
                {
                    image: "../src/assets/imgs/blog4-2x-600x386.jpg",
                    title: "The best protein shake",
                },
                {
                    image: "../src/assets/imgs/blog1-2x-600x386.jpg",
                    title: "Ultimate cardio workout",
                },
                {
                    image: "../src/assets/imgs/blog3-2x-600x386.jpg",
                    title: "New juices available now",
                }
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="d-flex justify-content-between align-items-center px-2">
            <h3 class="m-0">Latest articles</h3>
            <a href="#0">Read all articles <i class="fa-solid fa-chevron-right ms-2"></i></a>
        </div>
        <div class="row row-cols-3 py-5">
            <div class="col" v-for="(card, i) in cardsVideos" :key="`card${i}`">
                <div class="card">
                    <a href="#0" class="image-container">
                        <img :src="card.image" class="card-img-top" alt="img not foud">
                        <div class="overlay"></div>
                    </a>
                    <div class="card-body text-center">
                        <h4 class="card-title"><a href="#0">{{ card.title }}</a></h4>
                        <p class="card-text">By <a href="#0">admin</a> |November 26th, 2019| <a href="#0">Gym</a></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

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

            a {

                img {
                    border-radius: 0;
                }
            }

            .image-container {
                position: relative;
                overflow: hidden;

                .overlay {
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    width: 100%;
                    height: 100%;
                    background: rgb(65, 84, 255);
                    background: linear-gradient(0deg, rgba(65, 84, 255, 0.61) 0%, rgba(241, 255, 0, 0) 100%);
                    opacity: 0;
                    transition: opacity 0.3s ease;
                }

                &:hover .overlay {
                    opacity: 1;
                }
            }
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
            color: $my-gray-color;
        }
    }
}
</style>