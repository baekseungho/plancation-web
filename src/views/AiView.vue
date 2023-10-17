<template>
  <div class="ai">
    <div class="fixMenu">
      <!-- 사이드바 컴포넌트 (NAV메뉴,프로필)-->
      <SideBar class="fixSideBar" />
      <div class="fixHeaderBar">
        <!-- 헤더바 컴포넌트 (상단 헤더, 로고& 설정)-->
        <HeaderBar class="rightHeader" />
        <!-- 메인 화면 -->
        <div class="mainScreen">
          <AiIntro v-if="currentPage === 'AiIntro'" @changePage="handleChangePage"></AiIntro>
          <AiDetail></AiDetail>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import SideBar from '../components/SideBar.vue'
import HeaderBar from '../components/HeaderBar.vue'
import AiIntro from '../components/AiIntro.vue'
import AiDetail from '../components/AiDetail.vue'
import { ref } from 'vue'

const currentPage = ref('AiIntro')

const handleChangePage = (newPage) => {
  currentPage.value = newPage
}
</script>
<style lang="scss">
@import '../assets/scss/pages/ai.css'; // .ai {
//   display: flex;
// }
</style>
