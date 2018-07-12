<template>
  <div>
    <div>
      <div v-for="tab in tabs">
        {{tab.label}}
      </div>
    </div>
    <div>
      <component :is="selectedTab.component"/>
    </div>
  </div>
</template>