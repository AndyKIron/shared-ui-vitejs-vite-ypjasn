<script setup lang="ts">
import { ref } from 'vue';
import Button from '@ironsource/shared-ui/button';
import Tabs from '@ironsource/shared-ui/tabs';

defineProps<{ msg: string }>();

const count = ref(0);
const selectedTab = ref('1');

const tabs = [
  {
    id: '1',
    name: 'Rewarded Video',
    iconName: 'generic',
  },
  {
    id: '2',
    name: '',
    iconName: 'generic',
  },
  {
    id: '3',
    name: 'Banner',
    iconName: '',
  },
  {
    id: '4',
    name: 'Disabled Tab',
    iconName: 'generic',
    disabled: true,
  },
];
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <Button variant="solid" @click="count++">count is {{ count }}</Button>

    <Tabs :tabs-list="tabs" v-model:selected-tab="selectedTab"></Tabs>

    <br />

    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>
</template>
