<template>
  <q-tabs
    align="center"
    indicator-color="transparent"
    switch-indicator
    no-caps
    active-color="primary"
    class="text-secondary"
  >
    <q-route-tab
      :ripple="false"
      v-for="(menuTab, index ) in mobileMenu"
      :key="index"
      :label="menuTab.label"
      :icon="menuTab.icon"
      :to="{nameL:menuTab.to}"
      exact
    />
  </q-tabs>
</template>

<script>
export default {
  name: 'mainMenu',
  data() {
    return {
      mobileMenu: [
        {
          label: 'Estadisticas',
          icon: 'mdi-chart-bar',
          to: 'home'
        },
       /*  {
          label: 'Sintomas',
          icon: 'mdi-heart-pulse',
          to: '#'
        },
        {
          label: 'Ayuda',
          icon: 'mdi-help-box',
          to: '#'
        } */
      ]
    }
  }
}
</script>
