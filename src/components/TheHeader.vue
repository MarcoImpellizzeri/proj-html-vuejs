<script >
export default {

}
</script>

<template>
    <header>
        <div class="container-fluid">
            <div class="container d-flex justify-content-between align-items-center">

                <!-- logo e titolo -->
                <div class="d-flex align-items-center">
                    <img src="../assets/imgs/logo-fitnes.png" alt="logo img">
                    <h3 class="m-0">Avada Fitnes</h3>
                </div>


                <!-- navbar -->

                <div class="navbar-container d-flex justify-content-between align-items-center">
                    <ul class="list-unstyled d-flex">
                        <li><a href="#0">Home</a></li>
                        <li>Service <span><i class="fa-solid fa-chevron-down"></i></span></li>
                        <li>About <span><i class="fa-solid fa-chevron-down"></i></span></li>
                        <li>Videos <span><i class="fa-solid fa-chevron-down"></i></span></li>
                        <li>Blog</li>
                        <li>
                            Store <span class="badge text-bg-warning">New</span>
                            <span><i class="fa-solid fa-chevron-down"></i></span>
                        </li>
                    </ul>

                    <button class="btn btn-primary">Schedule a workout</button>

                    <div><i class="fa-solid fa-magnifying-glass"></i></div>

                    <div><i class="fa-solid fa-cart-shopping"></i></div>

                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
.container-fluid {
    color: white;
    background-color: black;

    .container {
        height: 100px;

        .navbar-container {
            height: 100%;

            ul {
                margin: 0;

                li {
                    margin-left: 15px;
                    margin-right: 15px;

                    a {
                        color: white;
                        text-decoration: none;
                        padding: 20px 10px 20px 10px;
                    }
                }
            }
        }
    }
}
</style>