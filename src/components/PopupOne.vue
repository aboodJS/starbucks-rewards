<template>
  <slot></slot>
  <ul>
    <li id="one">1</li>
    <li id="two">2</li>
    <li id="three">3</li>
  </ul>
  <div class="flex w-[30rem] justify-center text-3xl gap-3">
    <a href="#one">1</a><a href="#two">2</a><a href="#three">3</a>
  </div>
</template>

<style scoped>
ul {
  scroll-behavior: smooth;
  overscroll-behavior-inline: contain;
  overflow-x: scroll;
  scroll-snap-type: x mandatory;
  width: 100vw;
  height: 35vh;
  display: flex;
  anchor-name: --myCarousel;
}

ul::scroll-button(*) {
  border: 0;
  font-size: 2rem;
  background: none;
  color: rgb(0 0 0 / 0.7);
  cursor: pointer;
}

ul::scroll-button(*):hover,
ul::scroll-button(*):focus {
  color: rgb(0 0 0 / 1);
}

ul::scroll-button(*):active {
  translate: 1px 1px;
}

ul::scroll-button(*):disabled {
  color: rgb(0 0 0 / 0.2);
  cursor: unset;
}

ul::scroll-button(left) {
  content: '<<';
  right: calc(anchor(left) - 70px);
  bottom: calc(anchor(top) + 13px);
}

ul::scroll-button(right) {
  content: '>>';
  left: calc(anchor(right) - 70px);
  bottom: calc(anchor(top) + 13px);
}

li {
  scroll-snap-align: center;
  flex: 0 0 100%;
}

li:nth-child(odd) {
  background-color: cyan;
}

li:nth-child(even) {
  background-color: rgb(210, 229, 229);
}
</style>
