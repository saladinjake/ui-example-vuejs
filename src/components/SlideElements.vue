<div id="app">
  <div class="buttons">
    <button
      @click="removeSlide"
      :disabled="slides <= 2"
    >Remove Slide</button>
    <button
      @click="addSlide"
      :disabled="slides >= 10"
    >Add Slide</button>
  </div>
  <div class="slides">
    <transition-group 
      name="slide"
      mode="out-in"
      enter-class="slide-in"
      leave-class="slide-out"
      enter-active-class="animated slide-in-active"
      leave-active-class="animated slide-out-active"
    >
      <div
        v-for="index in slides"
        v-if="index == active"
        :key="index"
      >
        Slide {{ index }}
      </div>
    </transition-group>
  </div>
  <span
    class="prev"
    @click="move(-1)"
  >
    <i class="fa fa-chevron-left" aria-hidden="true"></i>
  </span>
  <span
    class="next"
    @click="move(1)"
  >
    <i class="fa fa-chevron-right" aria-hidden="true"></i>
  </span>
  <ul class="dots">
    <li 
      v-for="(dot, index) in slides"
      :class="{ active: ++index === active }"
      @click="jump(index)"
    ></li>
  </ul>
</div>


<style scoped>
.prev,
.next {
  position: absolute;
  top: 50%;
  width: 50px;
  height: 50px;
  border: 2px solid #221e21;
  color: #221e21;
  border-radius: 50%;
  margin-top: -25px;
  margin-left: 25px;
  cursor: pointer;
  line-height: 48px;
  text-align: center;
  text-indent: -2px;
  transition: all 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.prev:hover,
.next:hover {
  background: #221e21;
  color: #fff;
  transform: scale(1.2);
}
.prev:active,
.next:active {
  transform: translate(0, 3px) scale(1.2);
}

.next {
  right: 0;
  margin-left: auto;
  margin-right: 25px;
  text-indent: 2px;
}

.dots {
  position: fixed;
  display: block;
  width: 100%;
  text-align: center;
  bottom: 20px;
}
.dots li {
  width: 6px;
  height: 6px;
  border-radius: 3px;
  background: #221e21;
  opacity: 0.2;
  display: inline-block;
  margin: 0 3px;
  cursor: pointer;
  transition: opacity 0.4s ease-in-out, width 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
.dots li.active {
  width: 22px;
  opacity: 1;
}

.slides {
  font-size: 40px;
  display: flex;
  height: 100%;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}
@media (min-width: 600px) {
  .slides {
    font-size: 80px;
  }
}
@media (min-width: 900px) {
  .slides {
    font-size: 140px;
  }
}
.slides .animated {
  transition: all 400ms;
  position: absolute;
  transform: translate(-50%, -50%);
}
.slides .slide-in {
  opacity: 0;
  transform: translate(-40%, -50%);
}
.slides .slide-in-active {
  transition-delay: 150ms;
}
.slides .slide-out {
  opacity: 1;
}
.slides .slide-out-active {
  opacity: 0;
  transform: translate(-60%, -50%);
}

.buttons {
  position: absolute;
  top: 10px;
  left: 10px;
}

button {
  padding: 10px;
  outline: none;
  border: none;
  -webkit-appearance: none;
  background: #221e21;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  cursor: pointer;
}
button:disabled {
  opacity: 0.2;
  cursor: no-drop;
}
</style>

<script>
export default {
  el: '#app',
  data: {
    slides: 5,
    active: 1
  },
  methods: {
    move(amount) {
      let newActive
      const newIndex = this.active + amount
      if (newIndex > this.slides) newActive = 1
      if (newIndex === 0) newActive = this.slides
      this.active = newActive || newIndex
    },
    jump(index) {
      this.active = index
    },
    addSlide() {
      this.slides = this.slides + 1
    },
    removeSlide() {
      this.slides = this.slides - 1 
    }
  }
}
</script>
