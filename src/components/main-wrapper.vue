<template>
  <div class="main-wrapper">
    <p>{{ title }}</p>
	<e-catalog />
	<e-card />
  </div>
</template>
<script>
import eCatalog from './e-catalog.vue'
import eCard from './e-card.vue'

export default {
  name: "main-wrapper",
  components: {
	  eCatalog, eCard

  }, // дочерние компоненты
  props: {}, //то что прилетает с родительского компонента
  data() {
    //персональные данные компонента
    return {
      title: "main wrapper",
    };
  },
  computed: {}, //свойства которые вычисляются
  methods: {}, //отлавливаем действия пользователя,клики и прочее
  watch: {}, //следим за изменениями чего угодно в компоненте
  mounted() {
    //хуки
    //отрабатывает при полной загрузке
    console.log(1);
  },
};
</script>

<style>
.main-wrapper {
  max-width: 900px;
  margin: 0 auto;
}
</style>