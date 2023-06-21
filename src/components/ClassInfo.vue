<!-- TODO: デザイン修正、フロアガイドに戻るボタンとフロア選択に戻るボタン追加-->
<template>
  <div >
    <h1>授業情報</h1>
    <h2>{{ classData.subject }}</h2>
    <h2>教員：{{ classData.teacher }}</h2>
    <h3>学期： {{ classData.semester }}</h3>
    <div>
      <h3>履修可能学年</h3>
      <p>1年: {{ classData.1st year }}</p>
      <p>2年: {{ classData.2nd year }}</p>
      <p>3年: {{ classData.3rd year }}</p>
      <p>4年: {{ classData.4th year  }}</p>
    </div>
    <div>
      <h3>授業実施日時</h3>
      <p>曜日: {{ classData.day }} 時限: {{ classData.period }}</p>
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

</style>