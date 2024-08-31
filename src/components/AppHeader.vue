<script>
import Navbar from './Navbar.vue';
import menu from '../data/menu-navbar.json'

export default {
    components: {
        Navbar,
    },

    data() {
        return {
            menu: menu
        }
    },
}

</script>

<template>

    <header class="pt-2">

        <div class="container-fluid">
            <div class="row">
                <div class="col-10 offset-1">

                    <div class="header-content">
                        
                        <div class="header-logo"> <!-- logo -->
                            <img src="/public/img/logotype.png" alt="logo">
                        </div>
                        
                        <div class="header-menu"> <!-- menu -->
                            <Navbar
                            v-for="link, index in menu" :key="index"
                            :menuData="link"
                            />
                        </div>

                    </div>

                </div>
            </div>
        </div>

    </header>

</template>

<style lang="scss" scoped>

    .header-content {
        display: flex;
        justify-content: space-between;

        .header-logo {
            width: 100px;
    
            img {
                width: 100%;
            }
        }

        .header-menu {
            display: flex;
        }
    }
    

</style>