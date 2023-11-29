<template>
  <div class="page">
    <IndexBar :index-list="categories" :sticky-offset-top="60">
      <div class="container">
        <section v-for="category in categories" :key="category" class="section">
          <IndexAnchor :index="category">Title {{ category }}</IndexAnchor>
          <Cell :title="text" />
        </section>
      </div>
    </IndexBar>
  </div>
</template>

<script setup>
import { IndexBar, IndexAnchor, Cell } from 'vant';

const categories = [
  "Populair ❤️",
  "Menus & Chicken Mix",
  "The BOX",
  "Voorgerechten",
  "Pan pizza medium",
  "Classic pizza medium",
  "Classic pizza large",
  "Pan pizza large",
  "Cheesy crust pizza large",
  "Desserten",
  "Dranken"
];
const text = "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis corrupti culpa minus libero eligendi fugit nam, nostrum sapiente fuga consectetur aliquid quo voluptatem, necessitatibus quas! Animi iusto nihil tempore vitae sint neque quasi qui ullam quae. Assumenda rem quisquam dicta sunt! Provident quam enim, excepturi eum sequi saepe rerum repellendus!";
</script>

<style>
.page {
  padding-top: 60px;
}

.container {
  width: 1200px;
  margin: 0 auto;
}

.section {
  margin-bottom: 50px;
  font-size: 40px;
}

div.van-index-bar__sidebar {
  padding: 20px 0;
  top: 0;
  flex-direction: row;
  transform: translateY(0);
  background: #fff;
  box-shadow: 0 0 3px 2px rgba(0, 0, 0, 0.2);
  width: 100%;
  justify-content: center;
}
</style>
