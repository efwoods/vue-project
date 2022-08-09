<template>
  <form>
    <div>
      <BaseSelect
        :options="categories"
        v-model="event.category"
        label="Select a category"
      />
    </div>
    <div>
      <BaseCheckbox v-model="event.extras.catering" label="Catering" />
    </div>
    <div>
      <BaseInput v-model="event.title" label="Title" type="text" />
    </div>

    <BaseRadioGroup
      v-model="event.pets"
      :vertical="true"
      name="pets"
      :options="petOptions"
    />

    <BaseRadio
      v-model="event.radio"
      :value="0"
      label="Radio Toggle Button"
      name="unique"
      buttons
    />
  </form>
</template>

<script>
import BaseInput from './BaseInput.vue'
import BaseCheckbox from './BaseCheckbox.vue'
import BaseRadio from './BaseRadio.vue'

export default {
  name: 'DefaultVue',
  components: {
    BaseCheckbox,
    BaseInput,
    BaseRadio,
  },
  created() {},
  data() {
    return {
      categories: [
        'sustainability',
        'nature',
        'animal welfare',
        'housing',
        'education',
        'food',
        'community',
      ],
      event: {
        category: '',
        title: '',
        description: '',
        location: '',
        pets: 1,
        radio: 1,
        extras: {
          catering: false,
          music: false,
        },
      },
      petOptions: [
        { label: 'Yes', value: 1 },
        { label: 'No', value: 0 },
      ],
    }
  },
  props: {},
  methods: {},
}
</script>

<style scoped></style>
