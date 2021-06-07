<template>
    <div id="footer_links">
        <div class="footer_content">
            <ul>
                <li>
                    <a href="#">DC COMICS</a>
                </li>
                <li>
                    <a href="#">Characters</a>
                </li>
                <li>
                    <a href="#">Comics</a>
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
                    <a href="#">Videos</a>
                </li>
                <li>
                    <a href="#">News</a>
                </li>
            </ul>
                
            <ul>
                <li>
                    <a href="#">Shop</a>
                </li>
                <li>
                    <a href="#">Shop DC</a>
                </li>
                <li>
                    <a href="#">Shop DC collectibles</a>
                </li>
            </ul>
            <ul>
                <li>
                    <a href="#">DC</a>
                </li>
                <li>
                    <a href="#">Terms of Use</a>
                </li>
                <li>
                    <a href="#">Privacy policy (New)</a>
                </li>
                <li>
                    <a href="#">Ad Choises</a>
                </li>
                <li>
                    <a href="#">Advertising</a>
                </li>
                <li>
                    <a href="#">Jobs</a>
                </li>
                <li>
                    <a href="#">Subscriptions</a>
                </li>
                <li>
                    <a href="#">Talent Workshops</a>
                </li>
                <li>
                    <a href="#">CPSC Certificates</a>
                </li>
                <li>
                    <a href="#">Ratings</a>
                </li>
                <li>
                    <a href="#">Shop Help</a>
                </li>
                <li>
                    <a href="#">Contact Us</a>
                </li>
            </ul>
            <ul>
                <li>
                    <a href="#">Sites</a>
                </li>
                <li>
                    <a href="#">DC</a>
                </li>
                <li>
                    <a href="#">MAD Magazine</a>
                </li>
                <li>
                    <a href="#">DC Kids</a>
                </li>
                <li>
                    <a href="#">DC Universe</a>
                </li>
                <li>
                    <a href="#">DC Power Visa</a>
                </li>
            </ul>
        </div>
        
    </div>
</template>

<script>
export default {
    name: 'FooterLinks'
}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');

    #footer_links {
        background-image: url("../assets/img/footer-bg.jpg") ;
    }
    
    .footer_content {
        @include wrapper_80;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        align-content: flex-start;
        height: 300px;
        padding-top: 20px;
        background: url("../assets/img/dc-logo-bg.png") right center no-repeat;
        font-family: 'Roboto', sans-serif;

        ul {
            list-style: none;
            margin: 5px 20px;
        };
    }

    li {
        a {
            font-size: 12px;
            color: #7d7a77;
            &:hover {
                text-decoration: underline;
            }
        }
    }
    
    li:first-child {
        a {
            font-size: 16px;
            font-weight: 700;
            text-transform: uppercase;
            color: white;
        };
        margin: 10px 0;
    }

    a {
        text-decoration: none;
    }

</style>