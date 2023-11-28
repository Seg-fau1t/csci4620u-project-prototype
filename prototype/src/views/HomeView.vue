<script setup>
import { ref, computed } from 'vue'

const pose = ref('standing')
const angel = ref('front')

const shirt = ref(0)
const pant = ref(0)

const img_path = computed(() => {
  return "".concat(pose.value, ".", angel.value,"-", shirt.value, pant.value)
})

</script>

<template>
  <main>
  <div class="box">
  <div class="columns">
  <div class="column">
  <figure class="image is-128x128">
  <img src="https://bulma.io/images/placeholders/128x128.png">
</figure>
  </div>
  <div class="column">
  <div class="columns">
  <div class="column">

  <div class="field">
  <label class="label">Pose</label>
  <div class="select">
  <select v-model="pose">
    <option>standing</option>
    <option>sitting</option>
  </select>
</div>
</div>
  </div>
  <div class="column">

  <div class="field">
  <label class="label">Angle</label>
  <div class="select">
  <select v-model="angel">
    <option>front</option>
    <option>side</option>
  </select>
</div>
</div>
  </div>
  <div class="column">
  <div class="field">
  <label class="label">Location</label>
  <div class="select">
  <select>
    <option>room</option>
  </select>
</div>
</div>
  </div>
</div>

<div class="field">
  <label class="label">Outfit</label>
  <div class="control">


<div class="columns">
  <div class="column">

    <div class="field">
  <div class="control">
    <input @click="shirt=0" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>

  </div>
</div>
    <div class="field">
  <div class="control">
    <input @click="pant=0" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>
  </div>
</div>
  </div>

  <div class="column">

    <div class="field">
  <div class="control">
    <input @click="shirt=1" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>
  </div>
</div>
    <div class="field">
  <div class="control">
    <input @click="pant=1" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>
  </div>
</div>
  </div>

  <div class="column">

    <div class="field">
  <div class="control">
    <input @click="shirt=2" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>
  </div>
</div>
    <div class="field">
  <div class="control">
    <input @click="pant=2" type="image" src="https://bulma.io/images/placeholders/128x128.png" height=128 width=128>
  </div>
</div>
  </div>

</div>


  </div>
</div>


  </div>
</div>
  </div>
  </main>
</template>
