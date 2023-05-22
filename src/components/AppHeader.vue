<script>
    export default{
        name: "AppHeader",

      data() {
            return {
                links : [
                    "CHARACTERS",
                    "MOVIES",
                    "TV",
                    "GAMES",
                    "COLLECTIBLES",
                    "VIDEOS",
                    "FANS",
                    "NEWS",
                    "SHOP"
                ]
            }
        }  
    }
</script>

<template>
    <header>
        <!--div contenitore-->
        <div class="container">

            <!--parte sinistra con logo-->
            <div>
                <img class="logo" src="../assets/dc-logo.png" alt="">
            </div>

            <!--parte destra con link-->
            <div class="linkContainer">
                <ul>
                    <li class="link" v-for="link in links" :key="link">
                        {{link}}
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style>
    header{
        widows: 100%;
        height: 7.5rem;
    }

    .container{
        width: 1300px;
        height: 7.5rem;
        display: flex;
        justify-content: space-around;
    }

    .linkContainer{
        height: 100%;
        line-height: 95px;
    }

    .linkContainer ul{
        display: flex;
        align-items: center;
        height: 100%;
        margin: 0;
    }

    .link{
        list-style: none;
        height: 100%;
        margin: 0px 10px;
        
    }
</style>