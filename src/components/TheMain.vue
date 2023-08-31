<script>

export default {

}
</script>

<template>
    <div class="first-section-container container-fluid">
        <div class="container">
            <div class="row row-cols-3">
                <div class="col">
                    <div class="card text-bg-dark">
                        <img src="../assets/imgs/service6-2x.jpg" class="card-img" alt="...">
                        <div class="card-img-overlay">
                            <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                                <i class="fa-solid fa-chevron-up my-margin"></i><i
                                    class="fa-solid fa-chevron-up my-margin"></i>
                            </div>
                            <h3 class="card-title">Crossfit workout</h3>
                            <h5 class="card-text">Push your limits</h5>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card text-bg-dark">
                        <img src="../assets/imgs/box1-2x.jpg" class="card-img" alt="...">
                        <div class="card-img-overlay">
                            <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                                <i class="fa-solid fa-chevron-up my-margin"></i><i
                                    class="fa-solid fa-chevron-up my-margin"></i>
                            </div>
                            <h3 class="card-title">Crossfit workout</h3>
                            <h5 class="card-text">Push your limits</h5>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <div class="card text-bg-dark">
                        <img src="../assets/imgs/box3-2x.jpg" class="card-img" alt="...">
                        <div class="card-img-overlay">
                            <div class="position-a">
                                <div class="chevron my-2"><i class="fa-solid fa-chevron-up"></i>
                                    <i class="fa-solid fa-chevron-up my-margin"></i><i
                                        class="fa-solid fa-chevron-up my-margin"></i>
                                </div>
                                <h3 class="card-title">Crossfit workout</h3>
                                <h5 class="card-text">Push your limits</h5>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.first-section-container {
    background: rgb(26, 20, 195);
    background: linear-gradient(140deg, rgba(26, 20, 195, 1) 20%, rgba(186, 4, 43, 1) 80%);
    height: 900px;

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
                transform: scale(1.06);
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

                .position-a {
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
    }
}
</style>