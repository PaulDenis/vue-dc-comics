<template>
    <div id="content_container">
        <div class="jumbotron"></div>
        <div class="content">
            <div class="label">Current Series</div>
            <div class="cards" v-for="(card, index) in cards" :key="index">
                <div class="card_image">
                    <div class="layover">
                        {{ card.price }}
                        <a href="#" class="small_btn">BUY</a>
                    </div>
                    <img :src="card.thumb" alt="Fumetto">
                </div>
                <p>{{ card.series }}</p>
            </div>
            <div class="load">LOAD MORE</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Content',
    data: function () {
    return {
        cards: [
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel"
        }
        ]
    }
}

}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');

    #content_container {
        background-color: #1c1c1c;
        // height: 100px;
    }
    .jumbotron {
        height: 400px;
        background-image: url('../assets/img/jumbotron.jpg');
    }

    .content {
        @include wrapper_70;
        display: flex;
        position: relative;
        justify-content: space-around;
        flex-wrap: wrap;
        padding: 50px;
        font-family: 'Roboto', sans-serif;
        color: white;
    }
    .cards {
        height: 200px;
        width: 200px;
        margin-bottom: 40px ;
        .card_image {
            position: relative;
            height: 175px;
            overflow: hidden;
            margin-bottom: 10px;
            
            &:hover .layover {
                display: inline-block;
                cursor: pointer;
            }
        }
        img {
            width: 175px;
            
        }
        p {
            text-transform: uppercase;
            font-size: 14px;
        }
    }
    .layover {
        display: none;
        position: absolute;
        height: 175px;
        width: 175px;
        background-color: rgba($color: #000000, $alpha: 0.5);
    }
    .label {
        display: inline-block;
        position: absolute;
        top: 0;
        left: 0;
        transform: translate(10%, -50%);
        height: 40px;
        line-height: 40px;
        padding: 0 25px;
        font-size: 18px;
        font-weight: 700;
        text-align: center;
        text-transform: uppercase;
        background-color: #0282f9;
        &:hover {
            cursor: pointer;
        }
    }
    .load {
        padding: 10px 50px;
        font-weight: 700;
        background-color: #0282f9;
        &:hover {
            cursor: pointer;
        }
    }
</style>