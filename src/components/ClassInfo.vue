<!-- TODO: デザイン修正、フロアガイドに戻るボタンとフロア選択に戻るボタン追加-->
<template>
  <div >
    <h1>授業情報</h1>
    <h2>{{ classData.subject }}</h2>
    <h2>教員：{{ classData.teacher }}</h2>
    <h3>学期： {{ classData.semester }}</h3>
    <div>
      <h3>履修可能学年</h3>
      <p>1年: {{ classData['1st year'] ? '可' : '不可' }}</p>
      <p>2年: {{ classData['2nd year'] ? '可' : '不可' }}</p>
      <p>3年: {{ classData['3rd year'] ? '可' : '不可' }}</p>
      <p>4年: {{ classData['4th year'] ? '可' : '不可' }}</p>
    </div>
    <div>
      <h3>授業実施日時</h3>
      <p> {{ classData.day }} {{ classData.period }}時限</p>
    </div>
        <router-link to="/floor-select" class="back">フロア選択へ戻る</router-link>
  </div>
</template>

<script>

export default {
  name: 'ClassInfo',
  props: ['id', 'classData']
}
</script>

<style scoped>
.button-container {
  position: fixed;
  bottom: 200px;
  right: 200px;
}

.back {
  position: absolute;
  right: 25px;
  bottom: 25px;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 40px;
  padding-right: 40px;
  border: 2px solid #747578;
  border-radius: 80px;
  color: #ff0000;
  font-weight: 700;
  font-size: 16px;
  background-color: #fff;
  text-decoration: none;
}
</style>