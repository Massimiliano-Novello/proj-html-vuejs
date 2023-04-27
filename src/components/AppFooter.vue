<script>
export default {
    name: "AppFooter",
}
</script>

<template>
    <footer>
        <div class="footer-top d-flex justify-content-center align-items-center">
            <img src="../assets/img/avada-charity-sticky-header-logo-retina.png" alt="">
        </div>
        <div class="footer-bottom">
            <div class="copyrigth d-flex justify-content-center align-items-center">
                <i class="fa-regular fa-copyright"></i>
                <span class="ms-2">copyrigth 2012 - 2020 AVADA THEME BY THEME FUSION | ALL RIGHTS RESERVED | POWERED BY WORDPRESS</span>
            </div>
            <div class="footer-icon d-flex justify-content-center mt-3">
                <ul class="footer-list d-flex">
                    <li class="ms-3">
                        <a href="">
                            <i class="fa-brands fa-facebook-f"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-brands fa-instagram"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-brands fa-twitter"></i>
                        </a>
                    </li>
                    <li>
                        <a href="">
                            <i class="fa-brands fa-youtube"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
footer {

    .footer-top {
        height: 100px;

        img {
            width: 300px;
        }
    }

    .footer-bottom {
        background-color: #ebcac5;
        padding: 30px 0;
        .copyrigth {
            font-size: .7rem;
            color: gray;
        }

        .footer-icon {
            .footer-list {
            list-style-type: none;

            a {
                text-decoration: none;
                i {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: 50px;
                    height: 50px;
                    margin-right: 2rem;
                    background-color: lightyellow;
                    color: #fcd66c;
                    font-size: 1.5rem;
                    border-radius: 50%;
                }
            }

        }
        }
    }
}
</style>