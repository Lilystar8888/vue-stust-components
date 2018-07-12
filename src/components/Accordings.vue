<template>
  <div>
    <div v-for="(item, i) in list" :key="i" @click="selectedIdx=i">
      <label>{{item.label}}</label>
      <div v-if="selectedIdx===i">
        <div v-for="(sub, j) in item.list" :key="j">
          {{sub.label}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      selectedIdx: -1,
      list: [
        {
          label: 'Main 1',
          list: [
            {
              label: 'Sub 1',
              link: 'some-link'
            },
            {
              label: 'Sub 2',
              link: 'some-link'
            },
            {
              label: 'Sub 3',
              link: 'some-link'
            },
          ]
        },
        {
          label: 'Main 2',
          list: [
            {
              label: 'Sub 1',
              link: 'some-link'
            },
            {
              label: 'Sub 2',
              link: 'some-link'
            },
            {
              label: 'Sub 3',
              link: 'some-link'
            },
          ]
        },
        {
          label: 'Main 2',
          list: [
            {
              label: 'Sub 1',
              link: 'some-link'
            },
            {
              label: 'Sub 2',
              link: 'some-link'
            },
            {
              label: 'Sub 3',
              link: 'some-link'
            },
          ]
        },
      ],
    };
  },
};
  
</script>