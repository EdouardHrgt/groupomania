<template>
  <div id="app">
    <transition
      name="router-anim"
      enter-active-class="animate__animated animate__fadeIn animate__faster"
      leave-active-class="animate__animated animate__fadeOut animate__faster"
    >
      <router-view />
    </transition>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Overpass:wght@300;600&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;500;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@700&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css');

:root {
  --font-1: 'Overpass', sans-serif;
  --font-2: 'ubuntu', sans-serif;
  --font-3: 'Cairo', sans-serif;
  --black: #0e0e0e;
  --white: #ffffff;
  --primary: #323277;
  --secondary: #37ae5f;
  --ternary: #262a5a;
  --dark-blue: #151734;
  --gray: #e9e9e9;
  --red: #dd4124;
  --green: #00d646;
  --light-gray: #f0f0f0;
  --gradient: linear-gradient(43deg, #4158d0 0%, #c850c0 46%, #ffcc70 100%);
  --gradient-2: linear-gradient(90deg, #ff9a8b 0%, #ff6a88 55%, #ff99ac 100%);
  --transp1: rgba(38, 42, 90, 0.6);
  --transp2: rgba(0, 0, 0, 0.3);
  --transp3: rgba(0, 0, 0, 0.7);
  --transp5: rgba(38, 42, 90, 0.5);
  --transp4: rgba(230, 230, 230, 0.2);
  --transp6: rgba(255, 255, 255, 0.8);
  --transp7: rgba(0, 0, 0, 0.8);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: var(--font-1);
}
a,
li,
ul,
button,
input {
  text-decoration: none;
  list-style: none;
  outline: none;
  border: none;
}
#app {
  width: 100%;
  min-height: 100vh;
  background-color: var(--primary);
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 800 800'%3E%3Cg fill='none' stroke='%23323277' stroke-width='1'%3E%3Cpath d='M769 229L1037 260.9M927 880L731 737 520 660 309 538 40 599 295 764 126.5 879.5 40 599-197 493 102 382-31 229 126.5 79.5-69-63'/%3E%3Cpath d='M-31 229L237 261 390 382 603 493 308.5 537.5 101.5 381.5M370 905L295 764'/%3E%3Cpath d='M520 660L578 842 731 737 840 599 603 493 520 660 295 764 309 538 390 382 539 269 769 229 577.5 41.5 370 105 295 -36 126.5 79.5 237 261 102 382 40 599 -69 737 127 880'/%3E%3Cpath d='M520-140L578.5 42.5 731-63M603 493L539 269 237 261 370 105M902 382L539 269M390 382L102 382'/%3E%3Cpath d='M-222 42L126.5 79.5 370 105 539 269 577.5 41.5 927 80 769 229 902 382 603 493 731 737M295-36L577.5 41.5M578 842L295 764M40-201L127 80M102 382L-261 269'/%3E%3C/g%3E%3Cg fill='%23514EB7'%3E%3Ccircle cx='769' cy='229' r='5'/%3E%3Ccircle cx='539' cy='269' r='5'/%3E%3Ccircle cx='603' cy='493' r='5'/%3E%3Ccircle cx='731' cy='737' r='5'/%3E%3Ccircle cx='520' cy='660' r='5'/%3E%3Ccircle cx='309' cy='538' r='5'/%3E%3Ccircle cx='295' cy='764' r='5'/%3E%3Ccircle cx='40' cy='599' r='5'/%3E%3Ccircle cx='102' cy='382' r='5'/%3E%3Ccircle cx='127' cy='80' r='5'/%3E%3Ccircle cx='370' cy='105' r='5'/%3E%3Ccircle cx='578' cy='42' r='5'/%3E%3Ccircle cx='237' cy='261' r='5'/%3E%3Ccircle cx='390' cy='382' r='5'/%3E%3C/g%3E%3C/svg%3E");
}
/*LOADER*/
.loader {
  position: fixed;
  z-index: 101;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(1px);
}
.flex {
  display: flex;
  align-items: center;
  justify-content: center;
}

.custom_gradient {
  color: transparent;
  background: var(--gradient-2);
  background-clip: text;
}

/*TRANSITIONS*/
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.6s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.bounce-enter-active,
.bounce-leave-active {
  transition: all 0.6s;
}
.bounce-enter,
.bounce-leave-to {
  transform: scale(0);
}
.swapper-enter-active,
.swapper-leave-active {
  animation: translation 1.5s ease-in-out 0.3s forwards;
}
.list-move,
.list-enter-active,
.list-leave-active {
  transition: all 0.5s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(30px);
}
/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: white;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: gray;
}
</style>
