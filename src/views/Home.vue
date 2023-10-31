<template>
  <v-card @click="group" class="sisi">
    <v-toolbar color="#2C2B2A">
      <v-app-bar-nav-icon  @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title><div class="bt">鹤拍</div></v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs
          v-model="model"
          centered
          grow
        >
          <v-tab >
              <div class="bt" @click="dat = true;yjiedan = false;phb = false">大厅</div>
          </v-tab>
          <v-tab>
            <div class="bt"  @click="dat = false;yjiedan = true;phb = false">已接单</div>
          </v-tab>
          <v-tab>
            <div class="bt"  @click="dat = false;yjiedan = false;phb = true">排行榜</div>
          </v-tab>
        </v-tabs>
      </template>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer"  temporary  class="oopp" :width="330"> 
      <mine/>
      </v-navigation-drawer>
      
      
  </v-card>
      <div v-if="dat">
        <dat/>
      </div>
      <div v-if="yjiedan">
        <yjd/>
      </div>
      <div v-if="phb">
        <phb/>
      </div>
</template>
<script >

import dat from '../components/dat.vue';
import yjd from '../components/yjd.vue';
import phb from '../components/phb.vue';
import mine from '../components/mine.vue';
  export default {
    components: {
      dat,yjd,phb,mine
    },
    data () {
      return {
    worklist: [
      { 'id': 1, 'name': '大厅' },
      { 'id': 2, 'name': '已接单' },
      { 'id': 3, 'name': '排行榜' }
    ],
    dat:true,
    yjiedan:false,
    phb:false,
    model: 'tab-2',
    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
    drawer: false,
    group: null,
    items: [
      {
        title: 'Foo',
        value: 'foo'
      },
      {
        title: 'Bar',
        value: 'bar'
      },
      {
        title: 'Fizz',
        value: 'fizz'
      },
      {
        title: 'Buzz',
        value: 'buzz'
      }
    ]
  };
    },
    methods: {
      godat() {
        this.$router.push('/dat');
      }
    },
    watch: {
      group() {
        this.drawer = false
      },
    },
  }
</script>
<style scoped>
.bt{
    
    font-weight: 600;
    color: #F9E6D2;
}
.oopp{
  z-index: 8810;
  width: 80vw;
}
.sisi{
  z-index: 8811;
}
</style>