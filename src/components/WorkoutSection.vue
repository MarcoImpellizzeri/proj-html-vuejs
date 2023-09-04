<script>

export default {

}
</script>

<template>
    <div class="container-fluid">
        <a href="#0" class="square top">
            <i class="fa-solid fa-folder"></i>
            <p>Prebuilds</p>
        </a>
        <a href="#0" class="square bot">
            <i class="fa-solid fa-cart-shopping"></i>
            <p>Buy Now</p>
        </a>
        <div class="container d-flex">
            <div class="c-left py-5">
                <div>
                    <button class="btn-play rounded-circle"><i class="fa-solid fa-play"></i></button>
                </div>
                <h2 class="my-2">Crossfit workout of the day</h2>
                <h3>November 15th, 2019</h3>
                <a href="#0">View all videos <i class="fa-solid fa-arrow-right"></i></a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {


    background-image: url(../assets/imgs/banner14-2x.jpg);
    background-size: 2000px;
    background-position: center;
    background-repeat: no-repeat;
    height: 650px;
    position: relative;

    &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(145deg, rgba(1, 12, 168, 0.6) 20%, rgba(146, 1, 8, 0.6) 80%);
    }

    .square {
        z-index: 9999;
    }

    .container {
        justify-content: space-between;

        .c-left {
            z-index: 3;
            height: 650px;
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;

            div {
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

            h2 {
                color: $my-white-color;
                font-size: 3.5rem;
            }

            h3 {
                color: $my-yellow-color;
                font-size: 2.5rem;
                margin: 16px 0;
            }

            a {
                color: $my-white-color;
                text-decoration: none;
            }
        }
    }
}
</style>