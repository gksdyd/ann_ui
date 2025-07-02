<template>
  <iq-card>
    <template v-slot:body>
      <div class="iq-todo-page">
        <form class="position-relative">
          <div class="form-group mb-0">
            <input type="text" class="form-control todo-search" id="exampleInputEmail002" placeholder="Search" />
            <a class="search-link" href="#">
              <svg width="16" height="17" viewBox="0 0 16 17" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="7.82491" cy="7.82495" r="6.74142" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></circle>
                <path d="M12.5137 12.8638L15.1567 15.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
              </svg>
            </a>
          </div>
        </form>
        <div class="add-new-project mt-3 mb-3">
          <a href="#" class="d-flex align-items-center nrw-project"><i class="material-symbols-outlined me-2"> add
            </i>add Project</a>
        </div>
        <ul class="todo-task-list p-0 m-0">
          <li v-for="(item, index) in props.projectList" :key="index" ref="todoId"
            :class="`${item.id === selectedProject ? 'active' : ''}`">
            <a href="#" v-b-toggle="'todo-task' + index" class="d-flex align-items-center"><i
                class="material-symbols-outlined md-14 me-2"> filter_none
              </i>{{ item.project_name }}</a>
            <b-collapse tag="ul" :id="'todo-task' + index" class="sub-task mt-2 p-0"
              :visible="index === 0 ? true : false">
          <li v-for="(category, index1) in props.categoryList" :key="index1"
            :class="`${category.id === selectedCategory.id ? 'active' : ''}`">
            <a class="d-flex align-items-center justify-content-between" :href="category.href">
              <div class="d-flex align-items-center">
                <i :class="`material-symbols-outlined md-18 me-1 filled text-${category.color}`">
                  fiber_manual_record</i>{{ category.name }}
              </div>
              <span v-if="item.count !== '' && index1 === 2" class="badge bg-danger float-end">{{
            item.count.files }}</span>
            </a>
          </li>
          </b-collapse>
          </li>
        </ul>
      </div>
    </template>
  </iq-card>
</template>
<script setup>
import { defineProps, ref } from 'vue';

const props = defineProps({
  projectList: { type: Array, default: () => [] },
  categoryList: { type: Array, default: () => [] },
  selectedCategory: { type: Object, default: () => { } },
  selectedProject: { type: Object, default: () => { } },
})
</script>
