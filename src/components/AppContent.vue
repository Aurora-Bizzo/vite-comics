<script>
import comicsData from '../assets/data/dc-comics.js';
export default {
    data() {
        return {
            comics: comicsData
        }
    },
}
</script>

<template lang="">
    <div>
        <div class="jumbotron"></div>
        <div class="comics">
            <div class="container-xl">
                <div class="title">
                    <h2>CURRENT SERIES</h2>
                </div>
                <div class="content">
                    <div class="comic" v-for="(comic, index) in comics" :key="index">
                        <div class="thumb">
                            <img :src="comic.thumb" :alt="comic.series">
                        </div>
                        <div class="series">
                            {{comic.series}}
                        </div>
                    </div>
                    <div class="load-btn">
                        <button><strong>LOAD MORE</strong></button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/_variables.scss' as *;
@use '../styles/partials/_mixins.scss' as *;

.jumbotron {
    height: 400px;
    background-image: url(src/assets/img/jumbotron.jpg);
}

.comics {
    background-color: #232323;

    .title {
        position: relative;

        h2 {
            background-color: $sky-blue;
            width: 290px;
            padding: 15px;
            text-align: center;
            color: white;
            position: absolute;
            top: -35px;
        }
    }

    .content {
        @include flex-center;
        justify-content: space-between;
        flex-wrap: wrap;
        padding-top: 4rem;

        .comic {
            max-width: 193px;
            min-height: 387px;
        }

        .series {
            text-transform: uppercase;
            color: white;
            margin: 1rem 0 2rem 0;
        }

        .load-btn {
            width: 100%;
            margin: 2rem;
            @include flex-center;
            justify-content: space-around;
        }

        button {
            padding: 5px 50px;
            background-color: $sky-blue;
            border-color: $sky-blue;
            color: white;
        }
    }
}


</style>