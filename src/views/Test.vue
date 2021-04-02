<template>
  <div>
    <form action="" method="post">
      <RadioButton :label="label" :items="items"></RadioButton>
    </form>
  </div>
</template>

<script>
import RadioButton from '../components/RadioButton'

export default {
  name: 'Test',
  components: {
    RadioButton
  },
  data () {
    return {
      label: 'Name',
      items: [
        {
          value: 1,
          name: 'radio 1'
        },
        {
          value: 2,
          name: 'radio 2'
        },
        {
          name: 'radio 3',
          type: 'date'
        }
      ]
    }
  }
}
</script>

<style></style>
