<script >
export default {
    data() {
        return {
            navItem: [
                {
                    label: 'Home'
                },
                {
                    label: 'Service',
                    children: true,
                    drop: 'dropdown',
                    dropContent: [ 'All Service','Service Single Page' ]
                },
                {
                    label: 'About',
                    children: true,
                    drop: 'dropdown',
                    dropContent: [ "About me", "Our Sponsor", "Contact"]
                },
                {
                    label: 'Videos',
                    children: true,
                    drop: 'dropdown',
                    dropContent: [ 'All Playlis', 'Playlist Page', 'Video Single Page' ]
                },
                {
                    label: 'Blog'
                },
                {
                    label: 'Store',
                    children: true,
                    drop: 'dropdown',
                    dropContent: [ 'Simple Product', 'Variable Product' ]
                }
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
                    <a href="#0"><img src="../assets/imgs/logo.png" alt="logo img"></a>
                </div>


                <!-- navbar -->
                <div class="navbar-container d-flex justify-content-between align-items-center">
                    <ul class="list-unstyled d-flex">
                        <li v-for="(item, i) in navItem" :key="`item${i}`">
                            <div :class="item.drop">
                                <a href="#0" class="dropa">{{ item.label }}
                                    <span v-if="item.label === 'Store'"
                                        class="badge text-bg-warning text-lowercase">New</span>
                                    <span v-if="item.children"><i class="fa-solid fa-chevron-down ms-2"></i></span>
                                </a>
                                <div class="dropdown-content">
                                    <a v-for="(dropItem, i) in item.dropContent" :key="`dropItem${i}`" href="#0">
                                    {{ dropItem }}</a>
                                </div>
                            </div>
                        </li>
                    </ul>

                    <button class="my-btn">Schedule a workout</button>

                    <div><a href="#0"><i class="fa-solid fa-magnifying-glass mx-3"></i></a></div>

                    <div><a href="#0"><i class="fa-solid fa-cart-shopping mx-3 text-light"></i></a></div>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    color: $my-white-color;
    background-color: $my-black-color;

    .container {
        height: 100px;

        a {
            color: $my-white-color;
            text-decoration: none;
            padding: 40px 5px;
        }

        .navbar-container {
            height: 100%;

            a,
            div a {
                color: $my-gray-color;
            }

            ul {
                margin: 0;

                li {
                    margin: 0 5px;

                    &:first-child a {
                        color: $my-white-color;
                    }

                    a {
                        color: $my-gray-color;

                        &:hover {
                            transition: 0.5s;
                            color: $my-white-color;
                        }
                    }

                    .dropdown {
                        position: relative;
                        display: inline-block;

                        &:hover .dropdown-content {
                            opacity: 1;
                            transition: opacity 0.6s;
                        }

                        .dropa {
                            height: 100px;
                            padding: 40px 10px;
                            border: none;

                            .badge {
                                background-color: $my-yellow-color !important;
                                border-radius: 2px;
                            }
                        }

                        .dropdown-content {
                            opacity: 0;
                            transition: opacity 0.3s ease-in-out;
                            position: absolute;
                            top: 62px;
                            background-color: $my-black-color;
                            min-width: 150px;
                            box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
                            z-index: 4;
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
                font-size: .8rem;

                &:hover {
                    transition: 0.5s;
                    background-color: $my-red-color;
                }
            }

            a {
                color: $my-gray-color;

                &:hover {
                    transition: 0.5s;
                    color: $my-white-color;
                }
            }
        }
    }
}
</style>