<template>
  <div class="content-inner">
    <div class="container">
      <div class="row">
        <div class="col-lg-3">
          <ProjectList :project-list="projectList" :category-list="categoryList" :selected-category="selectedCategory"
            :selected-project="selectedProject" />
        </div>
        <div class="col-lg-9">
          <TaskList :task-list="taskList" :category="selectedCategory" :project="selectedProject" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
// import { socialvue } from '../../../config/pluginInit'
import ProjectList from "../Todo/ProjectList";
import TaskList from "../Todo/TaskList";
const taskList = [
  {
    id: 1,
    task_title: 'Landing Page For Secret Project ',
    project_id: 1,
    category_id: 1,
    user_id: 1,
    status: 'Expiring',
    task_status: false,
    dinlineblock: 'd-inline-block'
  },
  {
    id: 1,
    task_title: 'Fix Critical Crashes',
    project_id: 1,
    category_id: 1,
    user_id: 2,
    status: '',
    task_status: true,
    dinlineblock: ''
  },
  {
    id: 2,
    task_title: 'IOS App - Redesign The Contact',
    project_id: 1,
    category_id: 2,
    user_id: 3,
    status: 'Ending',
    task_status: false,
    dinlineblock: 'd-inline-block'
  },
  {
    id: 3,
    task_title: 'Final Meetup For The Secrat Project Client',
    project_id: 1,
    category_id: 1,
    user_id: 4,
    status: '',
    task_status: false,
    dinlineblock: ''
  },
  {
    id: 4,
    task_title: 'Code The Parsing Element',
    project_id: 1,
    category_id: 4,
    user_id: 5,
    status: 'Complete',
    task_status: false,
    dinlineblock: ''
  },
  {
    id: 5,
    task_title: 'Test The Bug, That Causes Design',
    project_id: 1,
    category_id: 3,
    user_id: 6,
    status: 'Urgent',
    task_status: false,
    dinlineblock: 'd-inline-block'
  },
  {
    id: 6,
    task_title: 'Android App Design',
    project_id: 1,
    category_id: 2,
    user_id: 7,
    status: 'Complete',
    task_status: false,
    dinlineblock: ''
  },
  {
    id: 7,
    task_title: 'Skype Meetup With Clients',
    project_id: 1,
    category_id: 2,
    user_id: 8,
    status: 'Complete',
    task_status: false,
    dinlineblock: '' 
  }
]

const projectList = [
  {
    id: 1,
    project_name: 'Secret Project',
    count: {
      id: 1,
      people: "",
      files: "44",
      statics: "",
    },
  },
  {
    id: 2,
    project_name: 'Bnie Mobile App',
    count: {
      id: 2,
      people: "",
      files: "20",
      statics: "",
    },
  },
  {
    id: 3,
    project_name: 'New Portfolio Site',
    count: {
      id: 3,
      people: "",
      files: "20",
      statics: "",
    },
  },
  // {
  //   id: 4,
  //   project_name: 'CRM'
  // }
]
const categoryList = [
  {
    id: 1,
    name: 'All Task',
    color: 'success',
    isHidden: true,
    count: ""
  },
  {
    id: 2,
    name: 'People',
    color: 'warning',
    isHidden: false,
  },
  {
    id: 3,
    name: 'Files',
    color: 'danger',
    isHidden: false,
  },
  {
    id: 4,
    name: 'Statistics',
    color: 'primary',
    isHidden: false,
  }
]

const selectedProject = {
  id: 1,
  project_name: 'Wednesday, 08th January, 2020'
}
const selectedCategory = {
  id: 1,
  name: 'All Task',
  color: 'success',
  isHidden: true
}

</script>
