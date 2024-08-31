<script>
export default {
    props: {
            menuData: Object,
        }
}
</script>

<template>

    <div class="menu">
        <ul>
            <li>
                <a
                    :href="menuData.url"
                    :class="menuData.current ? 'active' : ''">

                    {{ menuData.label }}
                </a>
            </li>
        </ul>
    </div>

</template>

<style lang="scss" scoped>
@use '/src/styles/variables.scss' as *;

    .menu {
        ul {
            list-style-type: none;
            display: flex;

            li{
                padding: 10px 15px;
                font-weight: 500;
                
                &:hover {
                    font-weight: 720;
                }
                
                a {
                    text-decoration: none;
                    color: black;
                }
            }
            
            .active {
                color: $active__color;
                padding-top: 15px;
                border-top: 5px solid black;
                font-weight: 720;
            }
        }
    }
    
</style>