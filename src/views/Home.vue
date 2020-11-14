<template>
    <div class="home">
        <div class="container">
            <spinner-merge class="component"></spinner-merge>
        </div>
        <div class="container">
            <spinner-line-bounce class="component"></spinner-line-bounce>
        </div>
    </div>
</template>

<script type="text/javascript">
    import spinnerMerge from "@/components/spinner-merge"
    import spinnerLineBounce from "@/components/spinner-line-bounce"
    export default{
        components: {
            spinnerMerge,
            spinnerLineBounce
        }
    }
</script>

<style type="text/css">
    .home{
        min-height: 100vh;
        animation: colorChange 8s infinite;
    }
    .component{
        top: calc(10% * var(--counter));
    }
    .container{
        font-size: 16px;
        display: flex;
        height: 33.3vh;
        justify-content: center;
        align-items: center;
        --spinner-color: #000;
    }
    @keyframes colorChange{
        0%, 100%{
            background-color: red;
        }
        20%{
            background-color: yellow;
        }
        40%{
            background-color: green;
        }
        60%{
            background-color: blue;
        }
        80%{
            background-color: violet;
        }
    }
</style>