<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({

  setup() {
    const content = ref(
      'NutUI4.0上线后我们研发团队也在不断的优化、测试、使用、迭代 Vue3 的相关组件，但是在跨端小程序的开发过程中，发现没有合适的组件库可以支持多端开发。为了填补这一空白，同时为了优化开发者体验，让 NutUI 能够为更多的开发者带来便利，我们决定在 NutUI 中增加小程序多端适配的能力。',
    )
    return { content }
  },
})
</script>

<template>
  <div class="demo h-100vh!">
    <h2 class="title">
      头部省略
    </h2>
    <nut-cell>
      <nut-ellipsis :content="content" direction="start" class="elli" />
    </nut-cell>

    <h2 class="title">
      尾部省略
    </h2>
    <nut-cell>
      <nut-ellipsis :content="content" direction="end" class="elli" />
    </nut-cell>

    <h2 class="title">
      中间省略
    </h2>
    <nut-cell>
      <nut-ellipsis :content="content" direction="middle" class="elli" />
    </nut-cell>

    <h2 class="title">
      多行省略
    </h2>
    <nut-cell>
      <nut-ellipsis :content="content" direction="start" rows="3" />
    </nut-cell>

    <h2 class="title">
      展开收起
    </h2>
    <nut-cell>
      <nut-ellipsis :content="content" direction="start" expand-text="展开" collapse-text="收起" />
    </nut-cell>
    <nut-cell>
      <nut-ellipsis :content="content" direction="middle" expand-text="展开" collapse-text="收起" />
    </nut-cell>
    <nut-cell>
      <nut-ellipsis :content="content" direction="end" rows="3" expand-text="展开" collapse-text="收起" />
    </nut-cell>
  </div>
</template>

<route lang="json">
{
  "style": {
    "navigationBarTitleText": "Ellipsis"
  }
}
</route>
