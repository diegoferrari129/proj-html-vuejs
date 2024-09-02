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
                            :class="{ active: link.current }" 
                            />
                        </div>

                    </div>

                    <div class="row">
                        <div class="col-4">

                            <div class="jumbo">

                                <div class="green-line"></div>
                                <h6>ALWATS THE BEST WAY YOU NEED IT</h6>
                                <h1>THE BEST <span>BUSINESS</span> CONSULTING</h1>
                                <div class="d-flex aligni-items-center">
                                    <button>READ MORE</button>
                                    <div class="jumbo-icon" >
                                        <i class="fa-solid fa-play" style="color: #63E6BE;"></i>
                                    </div>
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
@use '/src/styles/variables.scss' as *;

    header {
        background-image: url(/public/img/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg);
        background-repeat: no-repeat;
        background-position: right top;
        height: 950px;
        background-size: 1370px;

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

                .active {
                    color: $active__color;
                    border-top: 5px solid white;
                    font-weight: 900;
                }

                
            }
        }

        .jumbo {
            margin-top: 300px;

            .green-line {
                width: 50px;
                border-bottom: 5px solid #39febe;
                display: inline-block;
                margin-left: 5px;
            }

            h1 {
                font-size: 80px;
                font-weight: 700;
                line-height: 70px;
                padding: 20px 0px;
                padding-left: 4px;

                span {
                    padding-left: 7px;
                }
            }

            h6 {
                font-size: 14px;
                display: inline-block;
                padding-left: 20px;
                word-spacing: 2px;
            }

            button {
                background-color: #39febe;
                padding: 0px 50px;
                border: none;
                font-size: 12px;
                margin-top: 15px;
            }

            .jumbo-icon {
                border-radius: 50%;
                display: flex;
                align-items: center;
                justify-content: center;
                background-color: #1f1e38;
                width: 40px;
                height: 40px;
                border: 1px solid white;
                margin-left: 35px;
                margin-top: 25px;
            }
        }
    }

    

</style>