<template>
  <layout-wrapper>
    <layout-visual
      title="Information"
      :height="53"
      visual="visual-information"
    />
    <div class="w-full md:max-w-3xl mx-auto pt-20 px-4">
      <h2 class="text-xl pb-2 border-b border-blue-500 border-solid font-bold">
        {{ item.title }}
      </h2>
      <div class="pt-4 mb-4">
        <time class="block text-gray-600 mb-1">
          {{ item.date | formatDate }}
        </time>
      </div>
      <!-- eslint-disable-next-line vue/no-v-html-->
      <div class="mb-20" v-html="item.body"></div>
    </div>
    <base-button name="一覧に戻る" link="/information/" />
  </layout-wrapper>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({ $config, params, error }) {
    try {
      const { data } = await axios.get(
        `${$config.apiUrl}/information/${params.id}`,
        {
          headers: { 'X-API-KEY': $config.apiKey },
        }
      )
      return {
        item: data,
      }
    } catch (err) {
      error({
        errorCode: 404,
      })
    }
  },
  head() {
    return {
      title: this.item.title,
    }
  },
}
</script>
