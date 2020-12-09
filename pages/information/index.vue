<template>
  <layout-wrapper>
    <layout-visual
      title="Information"
      :height="53"
      visual="visual-information"
    />
    <div class="w-full md:max-w-3xl mx-auto pt-10 mb-10">
      <layout-information-list
        v-for="(item, index) in items"
        :id="item.id"
        :key="index"
        :date="item.date"
        :title="item.title"
      />
    </div>
    <base-button name="トップに戻る" link="/" />
  </layout-wrapper>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({ $config }) {
    const { data } = await axios.get(`${$config.apiUrl}/information`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })
    return {
      items: data.contents,
    }
  },
  head() {
    return {
      title: 'お知らせ',
    }
  },
}
</script>
