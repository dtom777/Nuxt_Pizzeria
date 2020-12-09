<template>
  <layout-wrapper>
    <layout-visual title="Concept" :height="53" visual="visual-concept" />
    <div class="w-full md:max-w-3xl mx-auto mt-10 mb-5 px-6 md:px-0">
      <h2 class="text-xl font-bold text-center mb-5">
        こだわりの有機野菜・本場イタリアの石窯を使用
      </h2>
      <p>
        当店では、無農薬・無化学肥料栽培による有機JAS認定を受けた安心・安全な野菜を使用しています。<br />
        ピッツアは、本場イタリアの炉床の石が分厚い窯を使っているため、高温でピッツァを素早く焼き上げることができます。<br />
        そのため、表面は香ばしく、中は水分を保ったまま焼き上げ、フワフワモチモチとした食感を生みます。<br />
        Napoli自慢のピッツァ、ぜひ一度！
      </p>
    </div>
    <base-button name="トップに戻る" link="/" />
  </layout-wrapper>
</template>

<script>
export default {
  head() {
    return {
      title: 'コンセプト',
    }
  },
}
</script>
