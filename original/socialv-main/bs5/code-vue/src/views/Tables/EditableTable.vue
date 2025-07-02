<template>
  <div class="content-inner">
    <b-container>
      <b-row>
        <b-col sm="12">
          <div
            class="card position-relative inner-page-bg bg-primary"
            style="height: 150px"
          >
            <div class="inner-page-title">
              <h3 class="text-white">Editable Table Page</h3>
              <p class="text-white">lorem ipsum</p>
            </div>
          </div>
        </b-col>
        <b-col sm="12">
          <b-card no-body>
            <h3
              class="card-header text-center font-weight-bold text-uppercase py-4"
            >
              Editable table
            </h3>
            <b-card-body class="pt-0">
              <div id="table" class="table-editable">
                <span class="table-add float-end mb-3 me-2">
                  <button
                    class="btn btn-sm btn-success d-flex align-items-center"
                    @click="addRow"
                  >
                    <i class="material-symbols-outlined me-1 md-18">add</i>Add
                    New
                  </button>
                </span>
                <table
                  class="table table-bordered table-responsive-md table-striped text-center"
                >
                  <thead>
                    <tr>
                      <th>Name</th>
                      <th>Age</th>
                      <th>Company Name</th>
                      <th>Country</th>
                      <th>City</th>
                      <th>Sort</th>
                      <th>Remove</th>
                    </tr>
                  </thead>
                  <tbody>
                    <b-tr v-for="(row, index) in rows" :key="index">
                      <b-td contenteditable="true" v-model="row.name">{{
                        row.name
                      }}</b-td>
                      <b-td contenteditable="true" v-model="row.age">{{
                        row.age
                      }}</b-td>
                      <b-td contenteditable="true" v-model="row.company">
                        {{ row.company }}
                      </b-td>
                      <b-td contenteditable="true" v-model="row.country">
                        {{ row.country }}
                      </b-td>
                      <b-td contenteditable="true" v-model="row.city">{{
                        row.city
                      }}</b-td>
                      <td>
                        <span class="table-up">
                          <a
                            href="#!"
                            class="indigo-text"
                            @click="moveRowUp(index)"
                          >
                            <i class="material-symbols-outlined md-16">north</i>
                          </a>
                        </span>
                        {{ "" }}
                        <span class="table-down">
                          <a
                            href="#!"
                            class="indigo-text"
                            @click="moveRowDown(index)"
                          >
                            <i class="material-symbols-outlined md-16">south</i>
                          </a>
                        </span>
                      </td>
                      <td>
                        <span class="table-remove">
                          <button
                            type="button"
                            class="btn btn-danger btn-rounded btn-sm my-0"
                            @click="removeRow(index)"
                          >
                            Remove
                          </button>
                        </span>
                      </td>
                    </b-tr>
                  </tbody>
                </table>
              </div>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      rows: [
        {
          name: "Anna Mull",
          age: "35",
          company: "Portica",
          country: "USA",
          city: "Oregon",
        },
        {
          name: "Jon Mull",
          age: "55",
          company: "dow jones",
          country: "US",
          city: "London",
        },
      ],
    };
  },
  methods: {
    addRow() {
      this.rows.push({
        name: "Jon Mull",
        age: "55",
        company: "dow jones",
        country: "US",
        city: "London",
      });
    },
    removeRow(index) {
      this.rows.splice(index, 1);
    },
    moveRowUp(index) {
      if (index > 0) {
        const temp = this.rows[index];
        this.rows.splice(index, 1);
        this.rows.splice(index - 1, 0, temp);
      }
    },
    moveRowDown(index) {
      if (index < this.rows.length - 1) {
        const temp = this.rows[index];
        this.rows.splice(index, 1);
        this.rows.splice(index + 1, 0, temp);
      }
    },
  },
};
</script>
