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
            <div class="c-buy py-5">
                <h2 class="my-2">“I’ve failed over and over again in my life. And that is why I succeed.”</h2>
                <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                    <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                </div>
                <h5 class="my-2">Arcu auctor gravida nisl, congue sit nisi tincidunt eget proin. In lacinia lacus donec sed
                    massa in ipsum eros, tristique. Gravida suspendisse etiam in iaculis</h5>
                <div>
                    <button class="my-btn ms-0 m-3">Buy Avada today <i class="fa-solid fa-chevron-right ms-2"></i></button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {

    .square {
        z-index: 9999;
    }

    background-image: url(../assets/imgs/banner2-2x.jpg);
    background-size: 1950px;
    background-position: top right;
    background-repeat: no-repeat;
    height: 700px;
    position: relative;

    &::before {
        content: "";
        position: absolute;
        bottom: 0;
        right: 0;
        width: 100%;
        height: 100%;
        background: rgb(0, 0, 0);
        background: linear-gradient(0deg, rgba(0, 0, 0, 0.856) 0%, rgba(241, 255, 0, 0) 100%);
    }

    .container {
        justify-content: space-between;

        .c-buy {
            z-index: 3;
            padding: 0 200px;
            height: 700px;
            width: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;

            h3 {
                color: $my-red-color;
            }

            h2 {
                color: $my-white-color;
                font-size: 3.4rem;
            }

            h5 {
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

                i {
                    font-size: .9rem;
                }
            }
        }

    }
}
</style>