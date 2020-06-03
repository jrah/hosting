<template>
  <div class="container mx-auto">
    <Menu />
    <div class="content mt-6 flex font-sans flex-col items-center">
      <span class="text-primaryColor text-sm">{{ title }}</span>
      <h1 class="text-4xl">{{ bigTitle }}</h1>
      <p class="mt-3 text-gray text-center lg:w-3/5">{{ description }}</p>
      <table class="mt-5 text-center border border-borderColor lg:w-full">
        <tr class="text-white bg-primaryColor">
          <td
            v-for="type in types"
            :key="type"
            class="p-4 w-2/6  border border-borderColor"
          >
            {{ type }}
          </td>
        </tr>
        <tr>
          <td
            v-for="plan in plans"
            :key="plan"
            class="p-6  border border-borderColor"
          >
            {{ plan }}
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import Menu from '~/components/Menu.vue'

export default {
  components: {
    Menu
  },
  data() {
    return {
      title: 'Hosting Price',
      bigTitle: '호스팅 비용 안내',
      description:
        'Vue119는 컨텐츠 관리 시스템(CMS)기반으로 Netlify를 사용하여 보다 편하고 저렴하게 홈페이지를 관리 할 수 있도록 도와드립니다.',
      types: ['Prismic(CMS)', 'Netlify(Hosting)', 'JavaScript(Main Code)'],
      plans: [
        '무료',
        '무료(게시글 등록, 팝업 수정시 배포함에 따라 작은 금액의 추가 요금 발생)',
        '빠르고 안정적인 반응속도'
      ]
    }
  }
}
</script>

<style scoped>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
