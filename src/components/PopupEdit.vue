<template>
  <div class="q-pa-md">
   <q-table
      :data="data"
      :columns="columns"
      :title="title"
      :rows-per-page-options="[]"
      row-key="name"
    >
      <template v-slot:body="props">
        <q-tr :props="props">
          <q-td key="desc" :props="props">
            {{ props.row.name }}
            <q-popup-edit v-model="props.row.name" title="Edit the Name">
              <q-input v-model="props.row.name" dense autofocus counter />
            </q-popup-edit>
          </q-td>
          <q-td key="calories" :props="props">
            {{ props.row.calories }}
            <q-popup-edit v-model="props.row.calories">
              <q-input v-model="props.row.calories" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="fat" :props="props">
            {{ props.row.fat }}
            <q-popup-edit v-model="props.row.fat">
              <q-input v-model="props.row.fat" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="carbs" :props="props">
            {{ props.row.carbs }}
            <q-popup-edit v-model="props.row.carbs" disable>
              <q-input v-model="props.row.carbs" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="protein" :props="props">
            {{ props.row.protein }}
            <q-popup-edit v-model="props.row.protein">
              <q-input v-model="props.row.protein" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="sodium" :props="props">
            {{ props.row.sodium }}
            <q-popup-edit v-model="props.row.sodium">
              <q-input v-model="props.row.sodium" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="calcium" :props="props">
            {{ props.row.calcium }}
            <q-popup-edit v-model="props.row.calcium">
              <template v-slot:title>
                <div class="text-italic text-primary">
                  My Custom Title
                </div>
              </template>
              <q-input v-model="props.row.calcium" dense autofocus />
            </q-popup-edit>
          </q-td>
          <q-td key="iron" :props="props">
            {{ props.row.iron }}
            <q-popup-edit v-model="props.row.iron">
              <q-input v-model="props.row.iron" dense autofocus />
            </q-popup-edit>
          </q-td>
        </q-tr>
      </template>
    </q-table>
  </div>
</template>

<script>
export default {
  name: 'PopupEdit',
  props: {
    title: String,
    data: Array,
    columns: Array,
  },
  data() {
    return {
    };
  },
};
</script>
