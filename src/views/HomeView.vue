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
  <div class="content"><p>This is where the generated image would go</p>
  <img src="https://bulma.io/images/placeholders/128x128.png">
  </div>

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
    <option>leaning</option>
    <option>lying down</option>
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
    <option>left side</option>
    <option>left side</option>
    <option>back</option>
  </select>
</div>
</div>
  </div>
  <div class="column">
  <div class="field">
  <label class="label">Location</label>
  <div class="select">
  <select>
    <option>garden</option>
    <option>city</option>
    <option>park</option>
    <option>living room</option>
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
    <img src="@/assets/red-shirt.png" height=128 width=128>

  </div>
</div>
    <div class="field">
  <div class="control">
    <img src="@/assets/b.png" height=128 width=128>
  </div>
</div>
  </div>

  <div class="column">

    <div class="field">
  <div class="control">
    <img src="@/assets/green-shirt.png" height=128 width=128>
  </div>
</div>
    <div class="field">
  <div class="control">
    <img src="@/assets/bb.png" height=128 width=128>
  </div>
</div>
  </div>

  <div class="column">

    <div class="field">
  <div class="control">
    <img src="@/assets/blue-shirt.png" height=128 width=128>
  </div>
</div>
    <div class="field">
  <div class="control">
    <img src="@/assets/bbb.png" height=128 width=128>
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
