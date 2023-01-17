<script>
export default {
    data(){
        return{
            menuItems: [
                {
                    lable: 'CHARACTERS',
                    url: '#',
                    active: true
                },
                {
                    lable: 'COMICS',
                    url: '#',
                    active: false
                },
                {
                    lable: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    lable: 'TV',
                    url: '#',
                    active: false
                },
                {
                    lable: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    lable: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    lable: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    lable: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    lable: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    lable: 'SHOP',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script> 

<template lang="">
    <header class="container-xl">
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
                            <strong>
                                {{item.lable}}
                            </strong> 
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

    img {
        width: 80px;
    }
    .navbar {
        height: 124px;
        padding: 0;

        nav {
        @include flex-center;
        height: $h-100;

            ul {
                list-style: none;
                display: flex;
                height: $h-100;
                margin: 0;

                li {
                    @include flex-center;
                    padding: 10px 15px;
                    height: $h-100;
                    border-bottom: 3px solid transparent;

                    &.active{
                    border-bottom: $boreder-blue;

                        a {
                            color: $sky-blue;
                        }
                    }

                    &:hover{
                        border-bottom: $boreder-blue;
                    }

                    a:hover{
                        color: $sky-blue; 
                    }
                }
            }
        } 
    }
</style>