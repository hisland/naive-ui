# v-show debug

```html
<n-space vertical item-style="line-height: 0;">
  <n-space>
    <button @click="toggle">toggle</button>
    <n-avatar v-show="isShow">{{ value }}</n-avatar>
    <n-avatar v-if="isShow" round>{{ value }}</n-avatar>
  </n-space>
  <n-input v-model:value="value" />
</n-space>
```

```js
import { defineComponent, onMounted, onUpdated, ref } from 'vue'

export default defineComponent({
  setup () {
    const isShow = ref(false)
    const toggle = () => {
      isShow.value = !isShow.value
    }
    onMounted(() => {
      console.log('world')
    })

    onUpdated(() => {
      console.log('hello')
    })
    return {
      value: ref('Oasis111'),
      toggle,
      isShow
    }
  }
})
```
