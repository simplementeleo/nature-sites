<template>
    <div>
        <header>
            <nav>
                <div class="logo">
                    <h2>Viajeros.</h2>
                </div>
                <ul>
                    <li>
                        <router-link to="/">Inicio</router-link>
                    </li>
                    <!-- <li>f
                        <router-link to="/about">Contacto</router-link>
                    </li> -->
                </ul>
            </nav>
        </header>
    </div>
</template>

<style lang="scss" scoped>
    header {
        // border: 1px solid red;

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2em 0;

            .logo {
                color: black;

            }

            ul {
                list-style: none;
                display: flex;
                color: black;
                justify-content: space-around;

                li {
                    margin-right: 40px;
                    font-weight: bold;

                    a {
                        text-decoration: none;
                        font-weight: bold;
                        color: #2c3e50;
                        border-bottom: 0;
                        transition: all ease-in-out .3s;
                        border-bottom: 2px solid transparent;

                        &.router-link-exact-active {
                            
                            border-bottom: 2px solid black;
                            
                        }

                    }
                }

            }
        }
    }
</style>


