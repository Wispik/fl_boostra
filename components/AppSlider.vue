<template>
  <div class="slider-block">
    <div class="slider-block__top">
      <span>{{ title }}</span>
      <div class="slider-block__top-value">
        {{ inputValue }} {{ val }}
      </div>
    </div>
    <input 
      type="range" 
      v-model="inputValue"
      :min="min"
      :max="max"  
      :step="step"
      @input="onInput"
    >
    <div class="slider-block__bottom">
      <span>{{ min }}</span>
      <span>{{ max }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    },
    min: {
      type: Number
    },
    max: {
      type: Number
    },
    default: {
      type: Number
    },
    step: {
      type: Number,
      default: 1
    },
    val: {
      type: String
    }
  },
  data() {
    return {
      inputValue: 0
    }
  },
  mounted() {
    this.inputValue = this.default
  },
  methods: {
    onInput(e) {
      const range = e.target
      const value = range.value
      const min = range.min
      const max = range.max
      const valuePercent = `${100 - ((max - value) / (max - min) * 100)}%`
      range.style.backgroundSize = `${valuePercent} 100%`
    }
  }
}
</script>

<style lang="scss" scoped>
.slider-block {
  width: 280px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  color: var(--text-gray-color);

  @media (max-width: 1000px) {
    width: 100%;
  }
}
.slider-block__top {
  display: flex;
  align-items: center;
  gap: 10px;
  justify-content: space-between;
  margin-bottom: 8px;
}
.slider-block__top-value {
  color: rgba(2, 17, 59, 1);
  font-weight: 600;
  font-size: 20px;
  line-height: 20px;
}
.slider-block__bottom {
  display: flex;
  align-items: center;
  gap: 10px;
  justify-content: space-between;
  font-size: 12px;
}
input[type="range"] {
  accent-color: var(--blue-color);
  appearance: none;
  border: none;
  cursor: pointer;
  background-color: rgba(223, 239, 255, 1);
  background-image: linear-gradient(var(--blue-color), var(--blue-color));
  background-repeat: no-repeat;
  background-size: 0 100%;
  border-radius: 200px;

  &::-webkit-slider-thumb {
    appearance: none;
    width: 38px;
    height: 38px;
    background-color: #fff;
    border: 7px solid var(--blue-color);
    border-radius: 100%;
    margin-top: -14px;
  }

  &::-moz-range-thumb {
    width: 31px;
    height: 31px;
    background-color: #fff;
    border: 7px solid var(--blue-color);
    border-radius: 100%;
    margin-top: -14px;
  }

  &::-webkit-slider-runnable-track {
    appearance: none;
    height: 7px;
    width: 100%;
    border-radius: 200px;
  }
}
</style>