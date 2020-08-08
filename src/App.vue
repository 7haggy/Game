<template>
    <div class="container" id="app">
        <h1 class="title">Simon Says</h1>
        <div class="circle-group">
            <div class="circle">
                <div class="blue"></div>
                <div class="red"></div>
                <div class="yellow"></div>
                <div class="green"></div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "App",
    };
</script>

<style lang="sass">
    .container
        max-width: 600px
        margin: 0 auto
        .title
            text-align: center
        .circle
            background: #fff
            position: relative
            float: left
            margin-right: 3em
            width: 295px
            height: 290px
            border-radius: 150px
            box-shadow: 2px 1px 12px #aaa;
            .blue, .red, .yellow, .green
                position: absolute
                width: 296px
                height: 290px
                opacity: 0.6
                border-radius: 150px

                &.red
                    right: 0
                    background: red
                    clip: rect(0px, 300px, 150px, 150px)
                &.green
                    right: 0
                    background: green
                    clip: rect(150px,300px, 300px, 150px)
                &.yellow
                    left: 0
                    background: yellow
                    clip: rect(150px, 150px, 300px, 0px)
                &.blue
                    background: blue;
                    clip: rect(0px, 150px, 150px, 0px);
</style>
