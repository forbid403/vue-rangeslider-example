<template>
<div>
  <h1>
    @domak/vue-rangeslider
  </h1>
  <h2>Default</h2>
  <RangeSlider
  ></RangeSlider>

  <br><br>

  <h2>Example</h2>
  <RangeSlider
  :keyboardMove="true"
  @getMinValue="getMinValue"
  @getMaxValue="getMaxValue"
  :min="0"
  :max="20"
  :gap="1"
  :defaultMin="minValue"
  :defaultMax="maxValue"
  :sliceNum="1"
  :bar="{
    color: '#593B02',
    sliceColor: '#F2B705',
  }"
  :tooltip="{
    visibility: true,
    color: '#F29F05'
  }"
  :handle="{
    color: '#D98E04',
    borderRadius: 'none'
  }"
  ></RangeSlider>
  <h3>min: {{this.minValue}}, max: {{this.maxValue}}</h3>
</div>
    
</template>

<script>
import RangeSlider from "@domak/vue-rangeslider";
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    RangeSlider
  },
  data() {
    return {
      minValue: 7,
      maxValue: 15,
    }
  },
  methods: {
    getMinValue: function(value) {
      this.minValue = value;
    },
    getMaxValue: function(value) {
      this.maxValue = value;
    },
  },
}
</script>

<style scoped>
body {
  background-color: cornflowerblue;
  background-color: darksalmon;
}
</style>
