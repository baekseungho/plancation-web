<template>
  <div class="introWrapper">
    <div class="intro">
      <p>계획 짜기 어려우시죠?</p>
      <p><span>Plancation</span>은 사용자에게 맞춘 맞춤 스케줄링 서비스를 제공합니다.</p>
      <div class="introImg"></div>
      <p>날짜 또는 기간, 활동가능 시간, 주제에 대해 작성만 해주세요!</p>
      <p>
        결과로 나온 계획이 보충이 필요하다면 수정할 수 있으며, 수정 후 회원님의 할 일에 등록이
        가능합니다.
      </p>
    </div>
    <button class="nextBtn" @click="emit('changePage', 'AiDetail')">다음</button>
  </div>
</template>
<script setup>
import { defineProps, defineEmits } from 'vue'

const emits = defineEmits(['changePage'])
</script>
<style scoped>
.introWrapper {
  position: relative;
  width: 100%;
  height: 100%;
}

.intro {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #fff;
  border-radius: 0.4rem;
}

.intro p {
  color: #494b7c;
  font-size: 1rem;
  margin: 0.5rem 0;
}

.intro span {
  color: #8f91c7;
  font-size: 2rem;
  font-weight: 800;
  margin-right: 0.5rem;
}

.introImg {
  width: 25rem;
  height: 25rem;
  background-image: url(../assets/images/main/ai_image.svg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.nextBtn {
  position: absolute;
  width: 15rem;
  height: 3rem;
  right: 3rem;
  bottom: 1rem;
  border-radius: 0.4rem;
  border: 0.1rem solid #735bf2;
  font-size: 1rem;
  color: #735bf2;
  background-color: #fff;
  cursor: pointer;
}

.nextBtn:hover {
  background-color: #f1f1f1;
}
</style>
