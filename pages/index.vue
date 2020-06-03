<template>
  <div class="container">
    <Menu />
    <div class="content">
      <span>{{ title }}</span>
      <h1>{{ bigTitle }}</h1>
      <p>{{ description }}</p>
      <table>
        <tr>
          <td v-for="type in types" :key="type">{{ type }}</td>
        </tr>
        <tr>
          <td v-for="plan in plans" :key="plan">{{ plan }}</td>
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
.content {
  margin-top: 30px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'Noto Sans KR', sans-serif;
}
span {
  font-family: 'Roboto', sans-serif;
  font-size: 14px;
  color: #22a266;
}
h1 {
  font-size: 35px;
}
table {
  border: 0.5px solid #d3e5dc;
  border-collapse: collapse;
  width: 1020px;
  margin-top: 20px;
  text-align: center;
}
tr:first-child {
  font-family: 'Roboto', sans-serif;
  background-color: #22a266;
  color: white;
}
tr:last-child td {
  padding: 30px;
}
td {
  width: 33%;
  border: 0.5px solid #d3e5dc;
  padding: 15px;
}
</style>
