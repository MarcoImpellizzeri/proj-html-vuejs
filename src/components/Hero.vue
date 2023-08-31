<script>

export default {

}
</script>

<template>
    <div class="container-fluid">
        <div class="container d-flex">
            <div class="c-left py-5">
                <h3 class="my-2">Certified fitness professional</h3>
                <h1 class="my-2">Take control of your health</h1>
                <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                    <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                </div>
                <h4 class="my-2">Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet.</h4>
                <div>
                    <button class="my-btn ms-0 m-3"><i class="fa-brands fa-youtube"></i> Visit my YouTube channel</button>
                    <button class="my-btn m-3">Buy Avada today <i class="fa-solid fa-arrow-right"></i></button>
                </div>
            </div>
            <div class="c-right py-5">
                <button class="btn-play rounded-circle"><i class="fa-solid fa-play"></i></button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    background-image: url(../assets/imgs/slider82x-scaled.jpg);
    background-size: 1950px;
    background-position: top right;
    background-repeat: no-repeat;
    height: 700px;
    z-index: 1;
    position: relative;

    &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 1600px;
        height: 100%;
        background: rgb(0, 0, 0);
        background: linear-gradient(90deg, rgba(0, 0, 0, 1) 43%, rgba(81, 0, 255, 0) 100%);
        z-index: 2;
    }

    .container {
        justify-content: space-between;
        .c-left {
            z-index: 3;
            height: 700px;
            display: flex;
            flex-direction: column;
            justify-content: center;

            h3 {
                color: $my-red-color;
            }

            h1 {
                color: $my-white-color;
                font-size: 4.5rem;
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
                background-color: $my-blu-color;
                font-size: 1rem;
                padding: 16px 40px;

                &:hover {
                    transition: 0.5s;
                    background-color: $my-red-color;
                }
            }

            .my-btn:last-child {
                background-color: $my-black-color;
                border: 1px solid $my-gray-color;
                color: $my-gray-color;

                &:hover {
                    transition: 0.5s;
                    background-color: $my-white-color;
                    color: $my-black-color;
                    border: 1px solid $my-white-color;
                }
            }
        }

        .c-right {
            z-index: 3;
            height: 700px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 30%;
            .btn-play {
                border: 0;
                color: $my-blu-color;
                padding: 35px 40px;
                background-color: $my-white-color;
                font-size: 1.1rem;

                &:hover {
                    transition: 0.5s;
                    color: $my-red-color;
                }
            }
        }

    }
}
</style>