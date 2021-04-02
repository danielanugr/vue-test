<template>
  <div>
    <label for="" class="group-label">{{ label }}</label>
    <div v-for="(item, count) in items" :key="count">
      <input
        v-if="!item.type"
        type="radio"
        name=""
        :id="item.name"
        :value="item.value"
        v-model="radioValue"
      />
      <label v-if="!item.type" :for="item.name">
        {{ item.name }}
      </label>
      <input
        v-if="item.type"
        type="radio"
        name=""
        id=""
        :value="customRadioValue"
        v-model="radioValue"
      />
      <input v-if="item.type" :type="item.type" v-model="customRadioValue" />
    </div>
    <p>value = {{ radioValue }}</p>
  </div>
</template>

<script>
export default {
  name: 'RadioButton',
  props: ['items', 'label'],
  data () {
    return {
      radioValue: '',
      customRadioValue: ''
    }
  }
}
</script>

<style>
.group-label {
  font-weight: bold;
}

span {
  margin: 0.2rem;
}
</style>
