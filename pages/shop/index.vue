<template>
  <layout-wrapper>
    <layout-visual title="Shop" :height="53" visual="visual-shop" />
    <div class="w-full md:max-w-3xl mx-auto mt-10 mb-5 px-6 md:px-0">
      <table class="table-auto bg-white w-full mb-3">
        <tbody>
          <tr>
            <td class="border border-light-blue-500 px-2 py-2">店舗名</td>
            <td class="border border-light-blue-500 px-2 py-2">
              pizzeria Napoli
            </td>
          </tr>
          <tr>
            <td class="border border-light-blue-500 px-2 py-2">住所</td>
            <td class="border border-light-blue-500 px-2 py-2">
              〒xxx-xxxx<br />
              兵庫県神戸市中央区１丁目○<br />
              △△△△△△△△△△△△ビル１F
            </td>
          </tr>
          <tr>
            <td class="border border-light-blue-500 px-2 py-2">座席数</td>
            <td class="border border-light-blue-500 px-2 py-2">
              50席<br />
              （うちテーブル40席・カウンター10席）<br />
              ※全席禁煙です。
            </td>
          </tr>
          <tr>
            <td class="border border-light-blue-500 px-2 py-2">アクセス</td>
            <td class="border border-light-blue-500 px-2 py-2">
              JR三ノ宮駅から徒歩3分
            </td>
          </tr>
          <tr>
            <td class="border border-light-blue-500 px-2 py-2">ご予約</td>
            <td class="border border-light-blue-500 px-2 py-2">
              TEL:080-xxxx-xxxx
            </td>
          </tr>
        </tbody>
      </table>
      <div>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d547.0064038591075!2d135.19304221818456!3d34.69496368525482!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x60008ee4f97cbcdf%3A0xa98feea1f562d433!2z77yI5qCq77yJ44OW44Or44Ki44Oz44OJ44OZ44Ki!5e0!3m2!1sja!2sjp!4v1607242307107!5m2!1sja!2sjp"
          frameborder="0"
          allowfullscreen=""
          class="w-full"
          aria-hidden="false"
          tabindex="0"
        ></iframe>
      </div>
    </div>
    <base-button name="トップに戻る" link="/" />
  </layout-wrapper>
</template>

<script>
export default {
  head() {
    return {
      title: '店舗情報',
    }
  },
}
</script>

<style scoped>
* {
  border-color: rgb(99, 179, 237);
}
</style>
