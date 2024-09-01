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

                    <div class="row">
                        <div class="col-4">

                            <div class="jumbo">

                                <div class="green-line"></div>
                                <h6>ALWATS THE BEST WAY YOU NEED IT</h6>
                                <h1>THE BEST <span>BUSINESS</span> CONSULTING</h1>
                                <div>
                                    <button>READ MORE</button>
                                    icon
                                </div>

                            </div>

                        </div>
                    </div>

                </div>
            </div>
        </div>

    </header>

</template>

<style lang="scss" scoped>

    header {
        background-image: url(/public/img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg);
        background-repeat: no-repeat;
        background-position: right top;
        height: 950px;
        background-size: 1400px;

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

        .jumbo {
            margin-top: 300px;

            .green-line {
                width: 50px;
                border-bottom: 5px solid #2b7a70;
                display: inline-block;
                margin-left: 5px;
            }

            h1 {
                font-size: 73px;
                font-weight: 700;
                line-height: 65px;
                padding: 20px 0px;
                padding-left: 4px;

                span {
                    padding-left: 7px;
                }
            }

            h6 {
                font-size: 14px;
                display: inline-block;
                padding-left: 15px;
            }

            button {
                background-color: #39febe;
                padding: 10px 45px;
                border: none;
                font-size: 12px;
                margin-top: 15px;
            }
        }
    }

    

</style>