<template>
  <div>
    <h1>Анимации</h1>
    <nav>
      <a href="#" @click="currentAnimation = 0">Радар</a>
      <a href="#" @click="currentAnimation = 1">Счетчик увеличивается</a>
      <a href="#" @click="currentAnimation = 2">Счетчик уменьшается</a>
    </nav>
    <Radar v-if="currentAnimation === 0"></Radar>
    <CounterPlus v-if="currentAnimation === 1"></CounterPlus>
    <CounterMinus v-if="currentAnimation === 2"></CounterMinus>
  </div>
</template>

<script>
import CounterMinus from './counter-minus.vue';
import CounterPlus from './counter-plus.vue'
import Radar from './radar.vue'

export default {
	components: {
		Radar,
    CounterPlus,
    CounterMinus,
  },
  data() {
    return {
      currentAnimation: 0
    };
  }
}
</script>