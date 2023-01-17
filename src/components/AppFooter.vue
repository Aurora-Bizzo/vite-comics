<script>
export default {
    data(){
        return{
            topArray:[
                {
                    image:'buy-comics-digital-comics.png',
                    label:'DIGITAL COMICS'
                },
                {
                    image:'buy-comics-merchandise.png',
                    label:'DC MERCHANDISE'
                },
                {
                    image:'buy-comics-subscriptions.png',
                    label:'SUBSCRIPTION'
                },
                {
                    image:'buy-comics-shop-locator.png',
                    label:'COMIC SHOP LOCATOR'
                },
                {
                    image:'buy-dc-power-visa.svg',
                    label:'DC POWER VISA'
                }
            ],
            middleArray1: [
                'Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News' 
            ],
            middleArray2: [
                'Shop DC', 'Shop DC Collectibles'
            ],
            middleArray3: [
                'Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscription', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'
            ],
            middleArray4: [
                'DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'
            ],
        }
    }
}
</script>

<template lang="">
    <footer>
        <div class="top-footer">
            <div class="row">
                <div class="col-12">
                    <div class="container-xl">
                        <ul>
                            <li v-for="(item, index) in topArray">
                                <img :src="`src/assets/img/${item.image}`">
                                <span>{{item.label}}</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="middle-footer">
            <div class="container-xl">
                <div class="row">
                    <div class="column">
                        <h5>DC COMICS</h5>
                        <ul>
                            <li v-for="(item, index) in middleArray1">
                                {{item}}
                            </li>
                        </ul>
                        <h5>SHOP</h5>
                        <ul>
                            <li v-for="(item, index) in middleArray2">
                                {{item}}
                            </li>
                        </ul>
                    </div>
                    <div class="column">
                        <h5>DC</h5>
                        <ul>
                            <li v-for="(item, index) in middleArray3">
                                {{item}}
                            </li>
                        </ul>
                    </div>
                    <div class="column">
                        <h5>SITES</h5>
                        <ul>
                            <li v-for="(item, index) in middleArray4">
                                {{item}}
                            </li>
                        </ul>
                    </div>
                 </div>
            </div>
        </div>
        <div class="bottom-footer"></div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/_variables.scss' as *;
@use '../styles/partials/_mixins.scss' as *;

.top-footer {
    background-color: $sky-blue;

    img {
    width: 50px;
    max-height: 65px;
    }

    ul {
    display: flex;
    align-items: center;
    padding: 3rem;
    justify-content: space-between;
    }
}

span {
    color: #fff;
    padding: 1rem;
}

.column {
    width: fit-content;
}

.middle-footer {
    background-image: url(../assets/img/footer-bg.jpg);
    .row {
        padding: 2rem 0 2rem 0;
    }

    ul {
        margin: 0 1rem 1rem 0;
    }

    h5, li{
        color:#fff;
    }

    .container-xl{
        background-image: url(src/assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: right center;
    }
}
</style>