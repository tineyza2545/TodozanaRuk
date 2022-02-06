<template>
  <v-container>
    <v-simple-table fixed-header height="300px">
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">ROW</th>
            <th class="text-left">Name</th>
            <th class="text-left">Delete</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(item, index) in desserts" :key="index">
            <td>{{ index + 1 }}</td>
            <td>{{ item.name }}</td>
            <td>
              <v-btn
                color="red darken-3 white--text"
                depressed
                @click="deleteTodo(index)"
              >
                <v-icon left>
                  {{ icons.mdiDelete }}
                </v-icon>
                Delete
              </v-btn>
            </td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
    <div
      class="d-flex align-start flex-column"
      style="position: fixed; bottom: 0"
    >
      <h1 class="red--text">
        **หมายเหตุ : กรุณากรอกข้อมูลให้ครบถ้วน (ระบบขัดข้องแจ้ง)
        <img
          class="mx-2"
          style="max-width: 10rem; max-height: 5rem"
          src="../assets/asd.png"
          alt=""
        />
      </h1>
    </div>
    <div class="d-flex align-end flex-column">
      <img
        style="position: fixed; bottom: 0; max-width: 20rem; max-height: 10rem"
        src="../assets/enzyme-gif-revised_orig.gif"
        alt=""
      />
    </div>
  </v-container>
</template>

<script>
import { mdiAccount, mdiPencil, mdiShareVariant, mdiDelete } from "@mdi/js";
export default {
  data() {
    return {
      icons: {
        mdiAccount,
        mdiPencil,
        mdiShareVariant,
        mdiDelete,
      },
    };
  },
  props: ["desserts"],
  methods: {
    deleteTodo(index) {
      this.desserts.splice(index, 1);
    },
  },
};
</script>

<style></style>
