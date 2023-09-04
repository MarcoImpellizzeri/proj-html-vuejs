<script>
export default {
    data() {
        return {
            socialIcons: [
                {
                    iconCode: '<i class="fa-brands fa-facebook-f"></i>',
                    nameSocial: "Facebook",
                },
                {
                    iconCode: '<i class="fa-brands fa-twitter"></i>',
                    nameSocial: "Twitter",
                },
                {
                    iconCode: '<i class="fa-brands fa-instagram"></i>',
                    nameSocial: "Instagram",
                },
                {
                    iconCode: '<i class="fa-brands fa-youtube"></i>',
                    nameSocial: "YouTube",
                },
                {
                    iconCode: '<i class="fa-brands fa-linkedin-in"></i>',
                    nameSocial: "Linkedin",
                }
            ],
            postsList: [
                {
                    postTitle: "The best protein shake",
                },
                {
                    postTitle: "Ultimate cardio workout",
                },
                {
                    postTitle: "New juices available now",
                },
                {
                    postTitle: "Tips to find training partners",
                },
                {
                    postTitle: "20 best healthy recipes",
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container-fluid">
        <div class="container footer-container">
            <div class="row row-cols-3">
                <div class="col left-col">
                    <img src="../assets/imgs/logo.png" alt="image not found">
                    <p>Ac aliquam neque sagittis diam faucibus vitae purus turpis phasellus. Pellentesque consectetur
                        amet purus ultrices mauris.</p>
                    <ul class="social-list">
                        <li v-for="(icon, i) in socialIcons" :key="`icon${i}`">
                            <div class="badge my-badge">{{ icon.nameSocial }}</div>
                            <a href="#0" v-html="icon.iconCode"></a>
                        </li>
                    </ul>
                </div>
                <div class="col mid-col">
                    <h5 class="text-uppercase">Recent posts</h5>
                    <ul>
                        <li class="post-list" v-for="(post, i) in postsList" :key="`post${i}`">
                            <a href="#0">
                                <i class="fa-solid fa-chevron-right"></i> {{ post.postTitle }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col right-col">
                    <h5 class="text-uppercase">Contact informations</h5>
                    <span>4746 Tipple Road Michigan 48449</span>
                    <span>Mobile: 1.800.000.0000</span>
                    <span>Email : info@your-company.com</span>
                </div>
            </div>
        </div>

        <hr>

        <div class="container copyright">
            <span>© Copyright 2012 - 2023 | Avada Theme by <a href="#0">ThemeFusion</a> | All Rights Reserved | Powered by
                <a href="#0">WordPress</a></span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.container-fluid {
    background-color: $my-black-color;

    .footer-container {
        padding: 150px 0;

        .row {
            .left-col {
                text-align: center;

                p {
                    padding: 20px;
                    margin: 0;
                    color: $my-white-color;
                }

                .social-list {
                    list-style: none;
                    display: flex;
                    justify-content: center;
                    padding: 0;

                    li {
                        display: flex;
                        flex-direction: column;
                        justify-content: center;
                        margin-top: 15px;

                        .my-badge {
                            background-color: #35363A;
                            font-size: .7rem;
                            opacity: 0;
                            transition: opacity 0.4s ease-in-out;
                        }

                        a {
                            text-decoration: none;
                            color: $my-red-color;
                            transition: opacity 0.4s ease-in-out;
                        }

                        &:hover .my-badge {
                            opacity: 1;
                            transition: opacity 0.4s ease-in-out;
                        }
                    }
                }
            }

            .mid-col {
                text-align: center;

                h5 {
                    margin-top: 5px;
                    color: $my-white-color;
                    margin-bottom: 50px;
                }

                .post-list {
                    list-style: none;
                    margin: 20px 0;
                    text-align: center;

                    a {
                        text-decoration: none;
                        color: $my-white-color;
                        transition: 0.4s;
                        font-size: 1.1rem;

                        &:hover {
                            color: $my-blu-color;
                            transition: 0.4s;
                        }
                    }
                }
            }

            .right-col {
                color: $my-white-color;
                text-align: center;
                display: flex;
                flex-direction: column;

                h5 {
                    margin-top: 5px;
                    margin-bottom: 50px;
                }

                span {
                    font-size: 1.1rem;

                    &:nth-child(2) {
                        color: $my-gray-color;
                        margin-bottom: 20px;
                    }
                }
            }
        }
    }

    hr {
        color: $my-gray-color;
    }

    .copyright {
        padding: 47px 0;
        background-color: $my-black-color;
        color: $my-gray-color;
        text-align: center;

        a {
            text-decoration: none;
            color: $my-white-color;
            transition: 0.4s;

            &:hover {
                color: $my-blu-color;
                transition: 0.4s;
            }
        }
    }
}
</style>