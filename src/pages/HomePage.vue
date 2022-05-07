<template>
<div>
    <AppHeader/>
    <ContentTable/>
</div>
</template>

<script>
import ContentTable from '../components/ContentTable.vue'
import AppHeader from '../components/AppHeader.vue'

export default {
  name: 'HomePage',

  components: {
    ContentTable,
    AppHeader
  },

  data: () => ({  
    //
  }),
};
</script>
