<template>
  <div>
    <Child ref="childRef">
      <p>askjdbaskjd</p>

      <!-- <template v-slot:test>
        <p>asfaf</p>
      </template> -->

      <template #test>
        <p>asfaf</p>
      </template>
    </Child>

    <button
      ref="btnRef"
      @click="onClick"
      class="rounded-lg border bg-blue-600 px-4 py-2 text-2xl text-white"
    >
      Chamar função do filho
    </button>
  </div>
</template>

<script setup lang="ts">
import { useTemplateRef } from 'vue'
import Child from './Child.vue'

defineOptions({ name: 'FatherComponent' })

const childRef = useTemplateRef('childRef')
const btnRef = useTemplateRef('btnRef')

const onClick = () => {
  if (!childRef.value || !childRef.value.onClick) {
    return
  }

  childRef.value.onClick()
  console.log(childRef.value.$el)

  if (btnRef.value) {
    console.log(btnRef.value)
  }
}
</script>
