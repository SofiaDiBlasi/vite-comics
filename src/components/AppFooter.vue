<script>
    export default{
        name: "AppFooter",

        data() {
            return {
                listaComics : [
                    "CHARACTERS",
                    "COMICS",
                    "MOVIES",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ],
                listaShop : [
                    "Shop DC",
                    "Shop DC Collectibles"
                ],
                listaDc : [
                    "Terms Of Use",
                    "Privacy Policy (New)",
                    "Ad Choices",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talent Workshop",
                    "CPSC Certificates",
                    "Rating",
                    "Shop Help",
                    "Contact Us"
                ],
                listaSite : [
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa"
                ],
                iconeSocial : [
                    "./src/assets/footer-facebook.png",
                    "./src/assets/footer-twitter.png",
                    "./src/assets/footer-youtube.png",
                    "./src/assets/footer-pinterest.png",
                    "./src/assets/footer-periscope.png"
                ],
                iconeBarraBlu : [
                    {
                        img : "./src/assets/buy-comics-digital-comics.png",
                        text : "DIGITAL COMICS"
                    },
                    {
                        img : "./src/assets/buy-comics-merchandise.png",
                        text : "DC MERCHANDISE"
                    },
                    {
                        img : "./src/assets/buy-comics-subscriptions.png",
                        text : "SUBSCRIPTION"
                    },
                    {
                        img : "./src/assets/buy-comics-shop-locator.png",
                        text : "COMIC SHOP LOCATOR"
                    },
                    {
                        img : "./src/assets/buy-dc-power-visa.svg",
                        text : "DC POWER VISA"
                    }
                ]
            }
        }  
    }
</script>

<template>
    <footer>

        <!--sezione 1-->
        <section class="s1">

            <!--icone-->
            <div class="barraBlu">
                <div v-for="icone in iconeBarraBlu" :key="icone">
                    <img :src="icone.img" alt=""  width="50" height="50">
                    <span>{{ icone.text }}</span>
                </div>
            </div>
        </section>

        <!--sezione 2-->
        <section class="s2">

            <!--liste-->
            <div class="footerList">
                <!--lista 1-->
                <ul>
                    <h3>DC COMICS</h3>
                    <li v-for="comic in listaComics" :key="comic">
                        {{comic }}
                    </li>
                </ul>
                <!--lista 2-->
                <ul>
                    <h3>SHOP</h3>
                    <li v-for="shop in listaShop" :key="shop">
                        {{shop}}
                    </li>
                </ul>
                  <!--lista 3-->
                  <ul>
                    <h3>DC</h3>
                    <li v-for="dc in listaDc" :key="dc">
                        {{dc}}
                    </li>
                </ul>
                <!--lista 4-->
                <ul>
                    <h3>SITES</h3>
                    <li v-for="site in listaSite" :key="site">
                        {{site}}
                    </li>
                </ul>
            </div>

            <!--img in trasparenza-->
            <div class="imgContainer">
                <div class="transpBg">
                </div>
            </div>
        </section>

        <!--sezione 3-->
        <section class="s3">
            <!--contenitore-->
            <div class="containerS3">
                <!--sign up button-->
                <div>
                    <button class="signUp">SIGN-UP NOW!</button>
                </div>

                <!--link ai social-->
                <div>
                    <span class="followUs">FOLLOW US</span>
                    <img class="icone" v-for="icone in iconeSocial" :key="icone" :src="icone" alt="">
                </div>
            </div>
        </section>
    </footer>
</template>

<style>
    footer{
        width: 100%;
    }

    .s1{
        background-color: #0282f9;
        width: 100%;
        height: 9.6rem;
    }

    .s2{
        display: flex;
        background-image: url(../assets/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        width: 100%;
        height: 25rem;
    }

    .s3{
        background-color: #303030;
        width: 100%;
        height: 7rem;
    }

    .imgContainer{
        width: 50%;
        height: 25rem;
        overflow: hidden;
    }

    .transpBg{
        width: 70%;
        height: 500px;
        background-image: url(../assets/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-size: contain;
        position: relative;
        bottom: 50px;
    }

    .footerList{
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        width: 50%;
        height: 25rem;
        margin-left: 200px;
    }

    .footerList ul{
        width: 15%;
    }

    .footerList li{
        color: white;
        list-style: none;
    }

    .footerList h3{
        color: white;
    }

    .signUp{
        color: white;
        background-color: #303030;
        border-color: #0282f9;
        padding: 15px;
    }

    .containerS3{
        padding: 50px 30px 0px ;
        display: flex;
        justify-content: space-between;
    }

    .followUs{
        color:#0282f9;
    }

    .icone{
        margin:5px;
    }

    .barraBlu{
        display: flex;
        justify-content: center;
        text-align: center;
        padding: 50px;
    }
</style>

