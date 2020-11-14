<template functional>
    <div class="spinner--merge">
        <span style="--counter:0"></span>
        <span style="--counter:1"></span>
        <span style="--counter:2"></span>
        <span style="--counter:3"></span>
    </div>
</template>

<style type="text/css">
    .spinner--merge{
        position: absolute;
        width: 8em;
        height: 8em;
        animation: spin-merge;
        animation-iteration-count: infinite;
        animation-timing-function: ease-in-out;
        animation-duration: 2s;
        animation-delay: 2s;
    }
    .spinner--merge span{
        --width: 2em;
        --height: 2em;
        display: block;
        width: var(--width);
        height: var(--height);
        top: 0;
        left: 0;
        background-color: var(--spinner-color, #fff);
        position: absolute;
        animation: spin-merge__ball;
        animation-iteration-count: infinite;
        animation-timing-function: ease-in-out;
        animation-duration: 2s;
        animation-delay: calc(var(--counter) * 0.5s);
        border-radius: 50%;
    }
    @keyframes spin-merge{
        0%,100%{
            width: 8em;
            height: 8em;
        }
        50%{
            width: 2em;
            height: 2em;
        }
    }
    @keyframes spin-merge__ball{
        0%,100% {
            top: 0;
            left: 0;
        }
        25% {
            top: 0;
            left: calc(100% - var(--width));
        }
        50% {
            top: calc(100% - var(--height));
            left: calc(100% - var(--width));
        }
        75% {
            top: calc(100% - var(--height));
            left: 0;
        }
    }
</style>