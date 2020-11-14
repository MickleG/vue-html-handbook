<template functional>
    <div class="spinner--line-jump">
        <span class="dot" style="--count:0"></span>
        <span class="dot" style="--count:1"></span>
        <span class="dot" style="--count:2"></span>
        <span class="dot" style="--count:3"></span>
    </div>
</template>

<style type="text/css">
    .spinner--line-jump {
         position: absolute;
         width: 8em;
         height: 3em;
    }
    .spinner--line-jump .dot {
         position: absolute;
         left: calc(var(--count) * 3em - 1.5em);
         top: 50%;
         width: 2em;
         height: 2em;
         border-radius: 50%;
         background-color: var(--spinner-color, #fff);
         margin: 0 auto;
         animation-duration: 2s;
         animation-iteration-count: infinite;
         animation-timing-function: ease-in-out;
         animation-delay: calc(var(--count) * (1s / 2));
         animation-name: spinner--line-jump-animation;
    }
    @keyframes spinner--line-jump-animation {
         0% {
             top: 50%;
        }
         12.5% {
             top: 0px;
        }
         25% {
             top: 50%;
        }
    }
</style>