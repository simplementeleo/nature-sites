<template>
    <div>
        <!-- Estoy en bulma -->
        <main class="container">
            <article class="row">
                <section class="img">
                    <img src="../assets/santorini.jpg" alt="">
                </section>
                <section class="others">
                    <div class="guide__travel">
                        <h4>Guía turística</h4>
                        <img src="../assets/compass.svg" alt="">
                        <span></span>
                        <p>Grecia</p>
                    </div>
                    <h1>Santorani</h1>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quis rerum harum ut saepe dicta.</p>
                    <div class="area">
                        <p>Area: <span>26.289 KM<sup>2</sup></span></p>
                        <p>Logitud máxima: <span>26.289 KM<sup>2</sup></span></p>
                    </div>

                    <div class="card__bottom">
                        <img src="../assets/santorini.jpg" class="img-hide" alt="">
                        <div class="card arrow">
                            <h3>Encontrar <br> hoteles</h3>
                            <p><i></i><i></i></p>
                        </div>
                        <div class="card">
                            <h3>Encontrar <br> vuelo</h3>
                            <img src="../assets/grecia.svg" alt="">
                        </div>
                    </div>
                </section>
                <section class="eje__y">
                    <div class="count">
                        <span>01</span>
                        <span></span>
                        <span>05</span>
                    </div>
                    <div class="arrows">
                        <div class="arrow">
                            <!-- Siguiente -->
                            <p><i></i><i></i></p>
                        </div>
                        <div class="arrow">
                            <!-- Anterior -->
                            <p><i></i><i></i></p>
                        </div>
                    </div>
                </section>

            </article>
            <footer>
                <a href="#">Inspiration</a>
                <a href="#">Github</a>
            </footer>
        </main>
    </div>
</template>

<style lang="scss" scoped>
    @import '../scss/responsive';
    @import '../scss/main';

</style>