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
            <div class="container-70 py-5">
                <h3 class="my-3">Join our mailing list today</h3>
                <h2 class="my-3">Insider offers & flash sales in your inbox every week.</h2>
                <div class="chevron my-3"><i class="fa-solid fa-chevron-up"></i>
                    <i class="fa-solid fa-chevron-up my-margin"></i><i class="fa-solid fa-chevron-up my-margin"></i>
                </div>
                <div class="d-flex my-2">
                    <input type="text" class="form-control ms-0 m-3" placeholder="Insert your email...*" aria-label="mail">
                    <button class="my-btn m-3">Subscribe</button>
                </div>
                <h4 class="my-3">Curabitur non nulla sit amet nisl tempus convallis quis ac lectus dolor sit amet,
                    consectetur adipiscing elit sed porttitor lectus.</h4>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    background-image: url(../assets/imgs/banner1-2x.jpg);
    background-size: 2010px;
    background-position: top right;
    background-repeat: no-repeat;
    height: 740px;
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

        .container-70 {
            z-index: 3;
            height: 700px;
            width: 70%;
            display: flex;
            flex-direction: column;
            justify-content: center;

            h3 {
                color: $my-red-color;
            }

            h2 {
                color: $my-white-color;
                font-size: 3.2rem;
                width: 85%;
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

            input {
                border-radius: 25px;
                border: 0;
            }

            .form-control:focus {
                box-shadow: none;
            }

            .my-btn {
                background-color: $my-blu-color;
                font-size: 1rem;
                padding: 16px 100px;

                &:hover {
                    transition: 0.5s;
                    background-color: $my-red-color;
                }
            }
        }
    }
}

.square {
    z-index: 9999;
}
</style>