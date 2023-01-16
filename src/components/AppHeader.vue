<script>
export default {
    data(){
        return{
            menuItems: [
                {
                    lable: 'Characters',
                    url: '#',
                    active: true
                },
                {
                    lable: 'Comics',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Tv',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Games',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Collectibles',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Videos',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    lable: 'News',
                    url: '#',
                    active: false
                },
                {
                    lable: 'Shop',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script> 

<template lang="">
    <header class="container">
        <div class="navbar">
            <div class="logo">
                <a href="#">
                    <img src="https://www.dccomics.com/sites/all/themes/dc_comics_bp/logo.png" alt="DC comics">
                </a>
            </div>
            <nav>
                <ul>
                    <li v-for="(item, index) in menuItems" :key="index" :class="item.active ? 'active' : ''">
                        <a href="item.url" :class="item.active ? 'active' : ''">
                            {{item.lable}}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/_variables.scss' as *;
@use '../styles/partials/_mixins.scss' as *;
    .navbar {
        @include flex-center;
        justify-content: space-between;
        height: 107px;
        margin: 1rem 0;

        nav {
        @include flex-center;
        height: 100%;

            ul {
                list-style: none;
                display: flex;
                height: 100%;

                li {
                    @include flex-center;
                    padding: 10px;
                    height: 100%;
                }
                li.active{
                    border-bottom: 3px solid rgb(12, 124, 236);
                }
                a {
                    &.active{
                        color: rgb(12, 124, 236); 
                    }
                }
            }
        } 
    }
</style>