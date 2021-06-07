<template>
    <div id="header">
        <img src="../assets/img/dc-logo.png" alt="Dc Logo">
        <!--<ul class="inline_list">
             <li>
                <a href="#">Characters</a>
            </li>
            <li>
                <a href="#" class="active">Comics</a>
            </li>
            <li>
                <a href="#">Movies</a>
            </li>
            <li>
                <a href="#">TV</a>
            </li>
            <li>
                <a href="#">Games</a>
            </li>
            <li>
                <a href="#">Collectables</a>
            </li>
            <li>
                <a href="#">Videos</a>
            </li>
            <li>
                <a href="#">Fans</a>
            </li>
            <li>
                <a href="#">News</a>
            </li>
            <li>
                <a href="#">Shop</a>
            </li> 
        </ul>-->
        <ul class="inline_list">
            <li v-for="(link,index) in links" :key="index">
                <a :href="link.url"
                :class="{active: link.active}"
                >
                {{ link.text }}
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Header',
    data: function() {
    return {
        links:[
            {
                text: "characters",
                url: "#characters",
                active: false
            },
            {
                text: "Comics",
                url: "#Comics",
                active: true
            },
            {
                text: "Movies",
                url: "#Movies",
                active: false
            },
            {
                text: "TV",
                url: "#TV",
                active: false
            },
            {
                text: "Games",
                url: "#Games",
                active: false
            },
            {
                text: "Collectibles",
                url: "#Collectibles",
                active: false
            },
            {
                text: "Videos",
                url: "#Videos",
                active: false
            },
            {
                text: "Fans",
                url: "#Fans",
                active: false
            },
            {
                text: "News",
                url: "#News",
                active: false
            },
            {
                text: "Shop",
                url: "#Shop",
                active: false
            }
        ]
    }
}
}

</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');
    #header {
        font-family: 'Roboto', sans-serif;
        display: flex;
        align-items: center;
        justify-content: space-between;
        @include wrapper_70;
        height: 100px;
        img {
            height: 70px;
            margin-right: 350px;
        };
    }
    .inline_list {
        display: flex;
        justify-content: space-between;
        align-items: center;
        list-style: none;
        width: 60%;
        
        li {
            display: inline-block;
            text-transform: uppercase;
        };
    }

    a {
        text-decoration: none;
        font-size: 12px;
        font-weight: 600;
        color: black;

        &:hover {
            color: #0282f9;
            border-bottom: 5px solid #0282f9;
            padding-bottom: 36px;
        };
    }
    .active {
        color: #0282f9;
        border-bottom: 5px solid #0282f9;
        padding-bottom: 36px;
    }


</style>