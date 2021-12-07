<template>
  <div>
    <h1>ユーザー一覧</h1>
    <ul>
      <li v-for="i of 3" :key="i">
        <nuxt-link :to="`/users/${i}`">ユーザー{{ i }}</nuxt-link>
      </li>
    </ul>
    <h1>カテゴリー一覧</h1>
    <ul>
      <li v-for="category of categories" :key="category.name">
        <nuxt-link :to="`/category/${category.name}`">{{
          category.name
        }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      categories: [{ name: "apple" }, { name: "banana" }, { name: "orange" }],
    };
  },
};
</script>
