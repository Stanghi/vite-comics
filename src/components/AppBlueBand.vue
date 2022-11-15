<script>
export default {
    name: 'AppBlueBand',
};
</script>

<template>
    <div class="band">
        <div class="container">
            <div class="box">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics" />
                <p>Digital Comics</p>
            </div>
            <div class="box">
                <img src="../assets/img/buy-comics-merchandise.png" alt="DC merchandise" />
                <p>DC merchandise</p>
            </div>
            <div class="box">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="subscription" />
                <p>subscription</p>
            </div>
            <div class="box">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="Comics shop locator" />
                <p>Comics shop locator</p>
            </div>
            <div class="box">
                <img class="visa-svg" src="../assets/img/buy-dc-power-visa.svg" alt="dc power visa" />
                <p>dc power visa</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

.band {
    display: flex;
    align-items: center;
    height: 155px;
    background-color: $dc-blue;

    .container {
        display: flex;
        justify-content: space-around;
        align-items: center;

        .box {
            display: flex;
            justify-content: center;
            align-items: center;

            img {
                height: 50px;
                margin-right: 15px;
            }

            p {
                font-size: 0.9rem;
                text-transform: uppercase;
                color: $text-white;
            }

            .visa-svg {
                transform: scale(0.7);
            }
        }
    }
}
</style>
