<template>
  <form>
    <BaseSelect
      :options="categories"
      v-model="event.category"
      label="Select a category"
    />
    <BaseCheckbox v-model="event.extras.catering" label="Catering" />

    <BaseInput v-model="event.title" label="Title" type="text" />
    <div>
      <BaseRadio
        v-model="event.pets"
        :value="1"
        label="Yes"
        name="pets"
        buttons
      />
    </div>
    <div>
      <BaseRadio
        v-model="event.pets"
        :value="0"
        label="No"
        name="pets"
        buttons
      />
    </div>
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
        extras: {
          catering: false,
          music: false,
        },
      },
    }
  },
  props: {},
  methods: {},
}
</script>

<style scoped></style>
