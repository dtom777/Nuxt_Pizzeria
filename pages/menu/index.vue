<template>
  <layout-wrapper>
    <layout-visual title="Menu" :height="53" visual="visual-menu" />
    <div class="container w-full mt-5 mx-auto">
      <div class="mb-10">
        <layout-menu-list
          v-for="(item, index) in items"
          :key="index"
          :image="item.image"
          :image-url="item.image.url"
          :name="item.name"
          :body="item.body"
          :price="item.price"
        />
      </div>
    </div>
    <base-button name="トップに戻る" link="/" />
  </layout-wrapper>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({ $config }) {
    const { data } = await axios.get(`${$config.apiUrl}/menu`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })
    return {
      items: data.contents,
    }
  },
  head() {
    return {
      title: 'メニュー',
    }
  },
}
</script>
