<template>
    <div>
        <div class="social">
            <a href="#" class="button">SIGN-UP NOW!</a>
            <div class="networks">
                <h2>FOLLOW US</h2>
                <ul>
                    <li>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fab fa-pinterest-p"></i></a>
                    </li>
                    <li>
                        <a href="#"><i class="fas fa-map-marker-alt"></i></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'Social'
}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    div {
        background-color: #303030;
        height: 100px
    }
    .social {
        @include wrapper_70;
        display: flex;
        justify-content: space-between;
        align-items: center;
        // height: 100px;
    }
    .networks {
        display: flex;
        align-items: center;
    }
    .button {
        padding: 15px;
        text-decoration: none;
        font-size: 14px;
        font-weight: 700;
        border: 2px solid #0282f9;
        color: white;
        &:hover {
            text-decoration: underline;
        }

    }
    h2 {
        display: inline-block;
        color: #0282f9;
        margin-right: 20px;
    }
    ul {
        list-style: none;
        display: inline-block;
        font-size: 20px;
        color: #303030;
        li {
            height: 30px;
            width: 30px;
            margin: 0 10px;
            padding-top: 5px;
            display: inline-block;
            border-radius: 50%;
            text-align: center;
            background-color:#797979;
            a {
                color: #303030;
            }
        }
    }

</style>