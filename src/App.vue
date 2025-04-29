<script setup>
  import FirstComponent from "./components/FirstComponent.vue";
  import Datas from "./components/Datas.vue";
  import PrimitiveReactiveData from "./components/PrimitiveReactiveData.vue";
  import NonPrimitiveReactiveData from "./components/NonPrimitiveReactiveData.vue";
  import DataBinding from "./components/DataBinding.vue";
  import WithProps from "./components/WithProps.vue";
</script>

<template>
  <header>Vuejs</header>
  <WithProps item="Eraser" :price="2.50"/>
  <DataBinding />
  <NonPrimitiveReactiveData />
  <PrimitiveReactiveData />
  <Datas/>
  <FirstComponent/>

</template>
