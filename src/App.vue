<script setup>
  import FirstComponent from "./components/FirstComponent.vue";
  import Datas from "./components/Datas.vue";
  import PrimitiveReactiveData from "./components/PrimitiveReactiveData.vue";
  import NonPrimitiveReactiveData from "./components/NonPrimitiveReactiveData.vue";
  import DataBinding from "./components/DataBinding.vue";
  import WithProps from "./components/WithProps.vue";
  import ListenEvent from "./components/ListenEvent.vue";
  import ComputedProperties from "./components/ComputedProperties.vue";
  import AssistedProperties from "./components/AssistedProperties.vue";
  import ConditionalRendering from "./components/ConditionalRendering.vue";
  import ListRendering from "./components/ListRendering.vue";

  const personDogs = [
    {name: "Totó", age: 2},
    {name: "Luke", age: 8},
    {name: "Pity", age: 5}
  ]
</script>

<template>
  <header>Vuejs</header>

  <ListRendering name="Jihed" :dogs="personDogs"/>
  <ConditionalRendering name-person="Jihed" :num-dogs="2"/>
  <AssistedProperties />
  <ComputedProperties />
  <ListenEvent />
  <WithProps item="Eraser" :price="2.50"/>
  <DataBinding />
  <NonPrimitiveReactiveData />
  <PrimitiveReactiveData />
  <Datas/>
  <FirstComponent/>

</template>
