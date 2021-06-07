<template>
    <div id="content_container">
        <div class="content">
            <h2>--> Content goes here </h2>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Content'
}
</script>

<style lang="scss" scoped>
    @import "../style/mixin.scss";
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');

    #content_container {
        background-color: #1c1c1c;
        // height: 100px;
    }

    .content {
        @include wrapper_80;
        color: white;
        padding: 25px;
    }
</style>