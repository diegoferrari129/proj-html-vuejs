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

    <footer>

        <div class="container-fluid">
            <div class="row">
                <div class="col-12">

                    <div class="top-footer">
                        
                        <div> <!-- logo -->
                            <img src="/public/img/logotype-2-139x23.png" alt="">
                        </div>
                        
                        <div class="footer-menu"> <!-- menu -->
                            <Navbar
                            v-for="link, index in menu" :key="index"
                            :menuData="link"
                            />
                        </div>
                        
                        <div> <!-- icons -->
                            <i class="fa-brands fa-instagram" style="color: #ffffff;"></i>

                            <i class="fa-brands fa-linkedin-in" style="color: #ffffff;"></i>

                            <i class="fa-brands fa-facebook-f" style="color: #ffffff;"></i>

                            <i class="fa-brands fa-twitter" style="color: #ffffff;"></i>
                        </div>

                    </div>

                </div>
            </div>
        </div>

    </footer>

    <div class="py-5">

        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="footer-line"></div>

                    <div class="bottom-footer">

                        
                        <div>

                            <div> <!-- info -->
                                Terms of use
                            </div>
                            <div>
                                Privacy Environmental Policy
                            </div>
                        </div>
                        
                        <div> <!-- copyright -->
                            Copyright
                            <i class="fa-regular fa-copyright fa-xs" style="color: #626173;"></i>
                            2020 Phlox Consulting. All Rights REserved.
                        </div>

                    </div>

                </div>
            </div>
        </div>

    </div>
    
</template>

<style lang="scss" scoped>

    footer {
        padding-top: 60px;
    }

    .top-footer, .bottom-footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0px 20px;
    }

    .top-footer {
        i {
            padding: 10px;
        }
    }

    .bottom-footer {
        color: #626173;
        font-size: 13px;
        padding-top: 30px;
    }



    .footer-line {
        border-bottom: 1px solid #626173;
        margin: 0px 20px;
    }

    .footer-menu {
        display: flex;
        
    }

</style>