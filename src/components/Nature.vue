<template>
    <div>
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
                            <p><i></i><i></i></p>
                        </div>
                        <div class="arrow">
                            <p><i></i><i></i></p>
                        </div>
                    </div>
                </section>
                <footer>
                    <a href="#">Inspiration</a>
                    <a href="#">Github</a>
                </footer>
            </article>
        </main>
    </div>
</template>

<style lang="scss" scoped>
// Estoy en Test
    // @import '../scss/responsive';

    .container {
        margin: 1em 3.5em;
        // height: 100vh;

        .row {
            display: grid;
            grid-gap: 50px;
            grid-template-columns: minmax(300px, 500px) 1fr 100px;
            // grid-template-rows: repeat(4, auto);
            grid-template-areas:
                "img other ejeY"
                "img other ejeY"
                "img other ejeY"
                "footer footer footer";
            align-content: center;
            justify-content: center;

            @media (max-width: 1080px) {
                 
                grid-template-areas:
                    
                    "other other ejeY"
                    "img img ejeY"
                    
                    "footer footer footer";
                // background: red;
            }


            .img {
                // background: #000;
                width: 100%;
                height: 100%;
                grid-area: img;
                border-radius: 5px;
                display: grid;
                justify-content: center;
                align-content: center;

                img {
                    width: 100%;
                    // height: 100%;
                    border-radius: 5px;
                }
            }

            .others {
                display: grid;
                align-content: space-between;
                grid-area: other;

                .area {
                    display: flex;
                    padding: 30px 0;

                    p {
                        color: grey;

                        span {
                            color: black;
                            font-weight: bold;
                        }

                        &:nth-child(1) {
                            margin-right: 20px;
                        }
                    }

                }

                h1 {
                    font-family: 'Times New Roman', Times, serif;
                    font-size: 6em;
                    padding: 20px 0;
                }

                .card__bottom {
                    display: grid;
                    grid-template-columns: repeat(2, minmax(250px, 1fr));
                    grid-template-rows: auto;
                    grid-gap: 20px;

                    .card {
                        color: white;
                        background: #ef5e3d;
                        display: flex;
                        justify-content: space-between;
                        align-items: center;
                        padding: 0 10%;
                        height: 8em;
                        border-radius: 7px;
                        box-shadow: 2px 3px 15px #ef5e3d54;
                        transition: all ease-in-out .3s;
                        cursor: pointer;

                        &:hover {
                            transform: translateY(-5px);
                        }

                        img {
                            width: 80px;
                            filter: grayscale(1) contrast(100);
                            opacity: .5;
                        }

                        &:nth-child(1) {
                            background: #3b42a1;
                            box-shadow: 2px 3px 15px #3b42a149;
                        }
                    }
                }
            }

            .arrow {
                p {
                    padding: 18px;
                    border-radius: 50%;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    border: 1px solid rgba(255, 255, 255, 0.568);

                    i {
                        position: absolute;
                        height: 2px;
                        width: 10px;
                        background: #fff;
                        transform: translate(0, 3px) rotate(-40deg);

                        &:nth-child(1) {
                            transform: translate(0, -3px) rotate(40deg);
                        }

                    }
                }
            }

            .eje__y {
                // width: 100px;
                grid-area: ejeY;
                // background: red;

                display: grid;
                justify-content: center;
                align-content: space-between;

                .arrows {
                    padding: 30px;

                    .arrow {
                        cursor: pointer;

                        p {
                            border: none;

                            i {
                                background: #000;
                            }
                        }

                        transform: rotateZ(-90deg);

                        &:nth-child(2) {
                            transform: rotateZ(90deg);
                        }

                    }

                }

                .count {
                    writing-mode: vertical-rl;
                    text-orientation: mixed;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    padding: 100% 0;
                    transform: rotateZ(-180deg);

                    span {
                        margin: 15px;
                        font-weight: bold;

                        &:nth-child(2) {
                            height: 2px;
                            width: 40%;
                            background: #eee;
                            transform: rotateZ(90deg);
                        }

                    }
                }

            }

            .guide__travel {
                width: 240px;
                // background:red;
                padding: 20px 0;
                display: flex;
                justify-content: space-between;
                align-items: center;

                img {
                    width: 25px;
                    filter: grayscale(1);
                }

                span {
                    width: 10%;
                    height: 3px;
                    background: #eee;
                    border-radius: 5px;
                }

                p {
                    color: #DDE0E1;
                }

            }

            footer {
                grid-area: footer;
                padding: 0 0 1.5em 0;
                a {
                    margin-right: 3em;
                    text-decoration: none;
                    font-weight: bold;
                    color: #000;
                }
            }

        }
    }
</style>