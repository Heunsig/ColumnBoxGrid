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
      description: '미야자키 하야오 감독의 애니메이션 걸작. 신비로운 온천에서 일어나는 모험을 통해 성장과 용기, 그리고 자연과의 조화를 다룬 환상적인 이야기입니다.',
    },
    {
      id: 9,
      name: '라라랜드',
      description: 'Ryan Gosling과 Emma Stone 주연의 뮤지컬 로맨스. 할리우드의 꿈을 향해 달려가는 두 젊은이의 사랑과 예술에 대한 열정을 담은 현대적인 뮤지컬입니다.',
    },
    {
      id: 10,
      name: '기생충',
      description: '봉준호 감독의 블랙 코미디 스릴러. 계급 갈등과 사회적 불평등을 예리하게 조명하며, 예상치 못한 반전으로 관객을 사로잡는 혁신적인 작품입니다.',
    },
    {
      id: 11,
      name: '듄',
      description: 'Denis Villeneuve 감독의 SF 대작. 사막 행성 아라키스의 정치적 갈등과 Paul Atreides의 운명을 다룬 웅장한 스페이스 오페라입니다.',
    },
    {
      id: 12,
      name: '스파이더맨: 노 웨이 홈',
      description: 'Tom Holland 주연의 마블 슈퍼히어로 영화. 멀티버스의 개념을 도입하여 과거의 스파이더맨들과의 만남을 통해 흥미진진한 액션을 선보입니다.',
    },
    {
      id: 13,
      name: '오펜하이머',
      description: 'Christopher Nolan 감독의 전기 드라마. 원자폭탄 개발의 아버지 J. Robert Oppenheimer의 생애를 통해 과학과 도덕의 경계를 탐구합니다.',
    },
    {
      id: 14,
      name: '토이스토리 4',
      description: '픽사 애니메이션의 대표작. 장난감들의 우정과 성장을 다룬 감동적인 이야기로, 어린이와 어른 모두에게 깊은 감동을 선사합니다.',
    },
    {
      id: 15,
      name: '조커',
      description: '',
    },
    {
      id: 16,
      name: '블랙 팬서',
      description: 'Chadwick Boseman 주연의 마블 슈퍼히어로 영화. 와칸다의 왕이자 블랙 팬서로서의 T\'Challa의 이야기를 통해 문화적 정체성과 리더십을 조명합니다.',
    },
    {
      id: 17,
      name: '어벤져스: 엔드게임',
      description: '마블 시네마틱 유니버스의 대단원. 11년간의 스토리를 마무리하며 슈퍼히어로들의 최후의 결전을 그린 웅장한 액션 블록버스터입니다.',
    },
    {
      id: 18,
      name: '위대한 개츠비',
      description: 'Leonardo DiCaprio 주연의 로맨틱 드라마. 1920년대 재즈 시대의 화려함과 허영을 배경으로 한 사랑과 꿈, 그리고 미국의 꿈에 대한 이야기입니다.',
    },
    {
      id: 19,
      name: '인터스텔라',
      description: 'Christopher Nolan 감독의 SF 드라마. 우주 탐사를 통해 인류의 생존과 사랑의 본질을 탐구하는 웅장한 스페이스 오디세이입니다.',
    },
    {
      id: 20,
      name: '겨울왕국',
      description: '디즈니 애니메이션의 현대적 걸작. 자매애와 용기를 다룬 뮤지컬 애니메이션으로, Let It Go의 히트와 함께 전 세계적인 인기를 얻었습니다.',
    },
  ]
})

</script>

<template>
  <div class="container">
    <h1>Movies</h1>
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
  width: 35rem;
  margin: 0 auto;
}
</style>