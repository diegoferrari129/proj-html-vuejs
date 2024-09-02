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
                padding: 10px 5px;
                font-weight: 500;
                font-size: 13px;
                
                &:hover {
                    font-weight: 950;
                    color: white;
                }
                
                a {
                    text-decoration: none;
                    color: #fa8b8e;
                }
            }

        }
    }
    
</style>