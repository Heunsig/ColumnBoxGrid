<script setup lang="ts">
import { computed } from 'vue';
import BoxContainer from './components/BoxContainer.vue';
import Card from './components/Card.vue';

const items = computed(() => {
  return [
    {
      id: 1,
      name: '인셉션',
      description: '꿈 속의 꿈을 다루는 SF 스릴러. 레오나르도 디카프리오가 주연한 Christopher Nolan 감독의 작품으로, 현실과 꿈의 경계를 모호하게 만드는 혁신적인 스토리텔링을 선보입니다.',
    },
    {
      id: 2,
      name: '타이타닉',
      description: '1912년 타이타닉호의 처녀항해를 배경으로 한 로맨틱 드라마. Jack과 Rose의 사랑 이야기를 통해 계급, 운명, 그리고 영원한 사랑의 의미를 다룹니다.',
    },
    {
      id: 3,
      name: '아바타',
      description: '판도라 행성의 외계 생명체와 인간의 갈등을 다룬 SF 영화. 3D 기술의 혁신으로 제작되어 시각적 효과의 새로운 기준을 제시했습니다.',
    },
    {
      id: 4,
      name: '스타워즈: 새로운 희망',
      description: '1977년 개봉한 SF 영화의 걸작. Luke Skywalker의 영웅 여정을 통해 선과 악의 대립, 그리고 희망의 메시지를 전달합니다.',
    },
    {
      id: 5,
      name: '포레스트 검프',
      description: 'Tom Hanks 주연의 드라마. 지적 장애가 있는 Forrest Gump의 인생을 통해 미국 현대사의 중요한 순간들을 유머러스하게 조명합니다.',
    },
    {
      id: 6,
      name: '매트릭스',
      description: '가상현실과 인공지능을 다룬 SF 액션 영화. Keanu Reeves가 주연한 이 작품은 현실의 본질에 대한 철학적 질문을 던집니다.',
    },
    {
      id: 7,
      name: '쇼생크 탈출',
      description: 'Tim Robbins와 Morgan Freeman 주연의 드라마. 희망과 우정, 그리고 자유에 대한 강력한 메시지를 담은 감동적인 이야기입니다.',
    },
    {
      id: 8,
      name: '센과치히로의 행방불명',
      description: '',
    },
    
  ]
})

</script>

<template>
  <div class="container">
    <BoxContainer 
      :items="items"
    >
      <template #default="{ item }">
        <Card :name="item.name" :description="item.description" />
      </template>
    </BoxContainer>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  height: 100vh;
  width: 35rem;
  margin: 0 auto;
}
</style>