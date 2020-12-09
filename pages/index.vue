<template>
  <layout-wrapper>
    <layout-visual
      title="Napoli"
      message="神戸にあるナポリピザのお店です"
    ></layout-visual>
    <!-- menu -->
    <div class="w-full md:max-w-3xl mx-auto mt-10 px-6 md:px-0">
      <base-heading>Recommend Menu</base-heading>
      <div class="flex md:flex-wrap justify-between mb-5 md:mb-0">
        <layout-menu-list
          v-for="(item, index) in menuItems"
          :key="index"
          :image="item.image"
          :image-url="item.image.url"
          :name="item.name"
          :body="item.body"
          :price="item.price"
          item-class="md:w-56 mb-10 shadow-xl bg-white mr-2"
          block-class="max-w"
          image-class="w-full"
          data-class="px-2 py-2"
          :flag-body="false"
        />
      </div>
    </div>
    <base-button name="Menu List" link="/menu/" />
    <!-- information -->
    <div class="mt-10">
      <base-heading>Information</base-heading>
      <div class="mb-5">
        <layout-information-list
          v-for="(item, index) in infoItems"
          :id="item.id"
          :key="index"
          :date="item.date"
          :title="item.title"
        />
      </div>
      <base-button
        name="Information List"
        link="/information/"
        class-margin="mt-10"
      />
    </div>
  </layout-wrapper>
</template>

<script>
import axios from 'axios'
import LayoutWrapper from '~/components/LayoutWrapper.vue'
export default {
  components: { LayoutWrapper },
  async asyncData({ $config }) {
    const menu = await axios.get(
      `${$config.apiUrl}/menu?limit=3&filters=flag[equals]true`,
      {
        headers: { 'X-API-KEY': $config.apiKey },
      }
    )
    const info = await axios.get(`${$config.apiUrl}/information?limit=3`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })
    return {
      menuItems: menu.data.contents,
      infoItems: info.data.contents,
    }
  },
}
</script>
