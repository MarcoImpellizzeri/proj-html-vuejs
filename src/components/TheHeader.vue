<script >
export default {
    data() {
        return {
            navItem: [
                { label: 'Home' },
                { label: 'Service', children: true, drop: 'dropdown' },
                { label: 'About', children: true, drop: 'dropdown' },
                { label: 'Videos', children: true, drop: 'dropdown' },
                { label: 'Blog' },
                { label: 'Store', children: true, drop: 'dropdown' }
            ],
        }
    },
    methods: {

    }
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
                        <li v-for="(item, i) in navItem" :key="`item${i}`">
                            <div :class="item.drop">
                                <a href="#0" class="dropa">{{ item.label }}
                                    <span v-if="item.label === 'Store'" class="badge text-bg-warning">New</span>
                                    <span v-if="item.children"><i class="fa-solid fa-chevron-down ms-2"></i></span>
                                </a>
                                <div v-if="item.label === 'Service'" class="dropdown-content">
                                    <a href="#0">All Service</a>
                                    <a href="#0">Service Single Page</a>
                                </div>
                                <div v-if="item.label === 'About'" class="dropdown-content">
                                    <a href="#0">About me</a>
                                    <a href="#0">Our Sponsor</a>
                                    <a href="#0">Contact</a>
                                </div>
                                <div v-if="item.label === 'Videos'" class="dropdown-content">
                                    <a href="#0">All Playlist</a>
                                    <a href="#0">Playlist Page</a>
                                    <a href="#0">Video Single Page</a>
                                </div>
                                <div v-if="item.label === 'Store'" class="dropdown-content">
                                    <a href="#0">Simple Product</a>
                                    <a href="#0">Variable Product</a>
                                </div>
                            </div>
                        </li>
                    </ul>

                    <button class="my-btn">Schedule a workout</button>

                    <div><a href="#0"><i class="fa-solid fa-magnifying-glass mx-3"></i></a></div>

                    <div><a href="#0"><i class="fa-solid fa-cart-shopping mx-3"></i></a></div>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    color: white;
    background-color: $prymary-color;

    .container {
        height: 100px;

        .navbar-container {
            height: 100%;

            a {
                color: white;
                text-decoration: none;
                padding: 40px 5px;
            }

            ul {
                margin: 0;

                li {
                    margin: 0 5px;

                    .dropdown {
                        position: relative;
                        display: inline-block;

                        &:hover .dropdown-content {
                            opacity: 1;
                            transition: opacity 0.6s;

                        }

                        .dropa {
                            height: 100px;
                            color: white;
                            padding: 40px 16px;
                            font-size: 16px;
                            border: none;
                        }

                        .dropdown-content {
                            opacity: 0;
                            transition: opacity 0.3s ease-in-out;
                            position: absolute;
                            top: 62px;
                            background-color: $prymary-color;
                            min-width: 150px;
                            box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
                            z-index: 1;
                            border-radius: 0 0 5px 5px;

                            a {
                                color: white;
                                padding: 12px 16px;
                                text-decoration: none;
                                display: block;
                                font-size: .8rem;

                                &:last-child {
                                    border-radius: 0 0 5px 5px;
                                }
                                

                                &:hover {
                                    transition: 0.7s;
                                    background-color: $my-blu-color;
                                }
                            }
                        }
                    }
                }
            }

            .my-btn {
                background-color: $my-blu-color;
                font-size: .9rem;

                &:hover {
                background-color: $my-red-color;

                }
            }
        }
    }
}
</style>