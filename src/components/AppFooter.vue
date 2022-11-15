<script>
export default {
    name: 'AppFooter',
};
</script>

<template>
    <footer>
        <div class="container top">
            <div class="links">
                <div class="col left">
                    <ul>
                        <h4>Dc Comics</h4>
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>

                    <ul>
                        <h4>Shop</h4>
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Schop DC Collectibles</a></li>
                    </ul>
                </div>

                <div class="col center">
                    <ul>
                        <h4>dc</h4>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy policy (New)</a></li>
                        <li><a href="#">Ad Choice</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscription</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>

                <div class="col right">
                    <ul>
                        <h4>sities</h4>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </div>
            </div>

            <div class="logo">
                <img src="../assets/img/dc-logo-bg.png" alt="DC logo" />
            </div>
        </div>

        <div class="footer-bottom">
            <div class="container bottom">
                <div class="btn-sign-up">
                    <p>Sign-up now!</p>
                </div>

                <div class="socials">
                    <p>Follow us</p>
                    <img src="../assets/img/footer-facebook.png" alt="facebook" />
                    <img src="../assets/img/footer-twitter.png" alt="twitter" />
                    <img src="../assets/img/footer-youtube.png" alt="youtube" />
                    <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
                    <img src="../assets/img/footer-periscope.png" alt="periscope" />
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

footer {
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url(../assets/img/footer-bg.jpg);
}

.container.top {
    height: 370px;
    overflow: hidden;
    display: flex;
    justify-content: space-between;

    .links {
        display: flex;
        padding-top: 45px;
    }

    .logo {
        position: relative;

        img {
            position: absolute;
            right: 0;
            top: -30%;
        }
    }
}

.col {
    margin-right: 30px;

    h4 {
        margin-bottom: 15px;
        text-transform: uppercase;
        color: $footer-text;
    }

    ul {
        list-style: none;

        li {
            padding-bottom: 5px;

            a {
                font-size: 0.75rem;
                text-decoration: none;
                color: $text-links-footer;
                cursor: pointer;
                &:hover {
                    color: $footer-text;
                }
            }
        }
    }
}

.col.left {
    ul:first-child {
        margin-bottom: 30px;
    }
}

.footer-bottom {
    height: 105px;
    background-color: $footer-bottom;

    .container.bottom {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;

        .btn-sign-up {
            padding: 10px;
            border: 2px solid $dc-blue;
            color: $footer-text;
            cursor: pointer;

            p {
                text-transform: uppercase;
                font-weight: bold;
            }
        }

        .socials {
            display: flex;
            align-items: center;

            p {
                color: $dc-blue;
                font-size: 1.3rem;
                font-weight: bold;
                text-transform: uppercase;
                margin-right: 30px;
            }

            img {
                padding-right: 15px;
                cursor: pointer;
            }
        }
    }
}
</style>
