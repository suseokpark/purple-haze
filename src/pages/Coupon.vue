<template>
  <q-page class="flex flex-center">
      <q-btn color="white" text-color="black" label="GET요청(console 참조)" @click="loadData" />
      <q-btn color="white" text-color="black" label="POST요청(console 참조)" @click="postData" />
      <q-btn color="white" text-color="black" label="PUT요청(console 참조)" @click="putData" />
      <q-btn color="white" text-color="black" label="DELETE요청(console 참조)" @click="deleteData" />

      <div class="todo">
          쿠폰 관련 컴포넌트 적용 예정
      </div>
      <PopupEdit title="테이블 제목을 여기다 입력하세요."
                 :columns="columns"
                 :data="data"/>
      <Calendar/>
      <Editor/>
  </q-page>
</template>

<style>
</style>

<script>
import PopupEdit from '../components/PopupEdit';
import Calendar from '../components/Calendar';
import Editor from '../components/Editor';

export default {
  name: 'Coupon',
  data() {
    return {
      columns: [
        {
          name: 'desc', align: 'left', label: 'Dessert (100g serving)', field: 'name',
        },
        {
          name: 'calories', align: 'center', label: 'Calories', field: 'calories',
        },
        {
          name: 'fat', label: 'Fat (g)', field: 'fat',
        },
        {
          name: 'carbs', label: 'Carbs (g)', field: 'carbs',
        },
        {
          name: 'protein', label: 'Protein (g)', field: 'protein',
        },
        {
          name: 'sodium', label: 'Sodium (mg)', field: 'sodium',
        },
        {
          name: 'calcium', label: 'Calcium (%)', field: 'calcium',
        },
        {
          name: 'iron', label: 'Iron (%)', field: 'iron',
        },
      ],
      data: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          sodium: 87,
          calcium: '14%',
          iron: '1%',
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          sodium: 129,
          calcium: '8%',
          iron: '1%',
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          sodium: 337,
          calcium: '6%',
          iron: '7%',
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          sodium: 413,
          calcium: '3%',
          iron: '8%',
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          sodium: 327,
          calcium: '7%',
          iron: '16%',
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          sodium: 50,
          calcium: '0%',
          iron: '0%',
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          sodium: 38,
          calcium: '0%',
          iron: '2%',
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          sodium: 562,
          calcium: '0%',
          iron: '45%',
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          sodium: 326,
          calcium: '2%',
          iron: '22%',
        },
        {
          name: 'KitKat',
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          sodium: 54,
          calcium: '12%',
          iron: '6%',
        },
      ],
    };
  },
  components: { PopupEdit, Calendar, Editor },
  methods: {
    loadData() {
      this.$axios.get('https://reqres.in/api/users')
        .then(resp => console.log(resp.data));
    },
    postData() {
      this.$axios.post('https://reqres.in/api/users', {
        name: 'neo',
        job: 'programmer',
        id: 2981,
      }).then(resp => console.log(resp.data));
    },
    putData() {
      this.$axios.put('https://reqres.in/api/users/2', {
        name: 'morpheus',
        job: 'zion resident',
      }).then(resp => console.log(resp.data));
    },
    deleteData() {
      this.$axios.put('https://reqres.in/api/users/2').then(resp => console.log(resp.data));
    },
  },
};
</script>
