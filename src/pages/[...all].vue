<!-- <template lang="pug">
div
  div 404
  div Oops
  div Page Not Found
</template> -->
<template lang="pug">
div(class="not_found_box")
  div(class="not_found") 404
  div(class="not_found_tip") Oops,Page Not Found
</template>

<style>
.not_found_box {
  width: 100vw;
  height: 100vh;
  position: relative;
  background-color: #000;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  font-family: Barlow;
  overflow: hidden;
}

.not_found_tip {
  font-size: 28px;
  text-align: center;
  font-weight: 700;
  line-height: normal;
  display: block;
  color: inherit;
}

.not_found,
.not_found::after {
  height: 86px;
  font-size: 152px;
  font-weight: bold;
  border: 0;
  letter-spacing: 3px;
  line-height: 88px;
  outline: transparent;
  position: relative;
  margin-bottom: 50px;
}

.not_found::after {
  --slice-0: inset(50% 50% 50% 50%);
  --slice-1: inset(80% -6px 0 0);
  --slice-2: inset(50% -6px 30% 0);
  --slice-3: inset(20% -6px 85% 0);
  --slice-4: inset(40% -6px 43% 0);
  --slice-5: inset(80% -6px 5% 0);
  content: '404';
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, transparent 3%, transparent 3%, transparent 5%, #000 5%);
  text-shadow: -3px -3px 0px #08fffbd2, 3px 3px 0px #f00044de;
  clip-path: var(--slice-1);
  animation: 3.8s glitch infinite;
  animation-timing-function: steps(2, end);
}

@keyframes glitch {
  0% {
    clip-path: var(--slice-2);
    transform: translate(-20px, -10px);
  }

  10% {
    clip-path: var(--slice-3);
    transform: translate(10px, 10px);
  }

  20% {
    clip-path: var(--slice-1);
    transform: translate(-10px, 10px);
  }

  30% {
    clip-path: var(--slice-3);
    transform: translate(0px, 5px);
  }

  40% {
    clip-path: var(--slice-2);
    transform: translate(-5px, 0px);
  }

  50% {
    clip-path: var(--slice-3);
    transform: translate(5px, 0px);
  }

  60% {
    clip-path: var(--slice-4);
    transform: translate(5px, 10px);
  }

  70% {
    clip-path: var(--slice-2);
    transform: translate(-10px, 10px);
  }

  80% {
    clip-path: var(--slice-5);
    transform: translate(20px, -10px);
  }

  90% {
    clip-path: var(--slice-1);
    transform: translate(-10px, 0px);
  }

  100% {
    clip-path: var(--slice-3);
    transform: translate(0);
  }
}
</style>
