<template>
    <div class="projects" id="project-card" >         
        <div v-for="projects in projects" :key="projects.id">
            <div class="project-card">
                <div class="project-image">
                    <img src="{{projects.covers[202]}}" class="project-img">
                </div>
                <div class="project-general-info">
                    <p class="project-index">#{{projects.id}}</p>
                    <p class="project-name">{{projects.name}}</p>
                    <p class="project-fields">{{projects.fields}}</p>
                    <button class="project-open-btn1">Что-то сделать</button>
                    <button class="project-open-btn2">Посмотреть</button>
                </div>
                <div class="project-stats">
                    <ul class="project-stat">
                        <li class="project-li-stat"><i class="fas fa-eye"></i> {{projects.stats.views}}</li> 
                        <li class="project-li-stat"><i class="fas fa-thumbs-up"></i> {{projects.stats.appreciations}}</li>
                        <li class="project-li-stat"><i class="fas fa-comment"></i> {{projects.stats.comments}}</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios';
import {mapState, mapMutations, mapGetters} from "vuex";
export default {
    data() {
        return {
            projects: []
        }
    },
    created() {
        this.getProjects()
    },
    methods: {
    getProjects: function() {
        axios.get('https://api.behance.net/v2/projects?q=motorcycle&client_id=UQHakERSArHWQGtYuuN0vuWbWFcPdtcL')
        .then(response => this.projects = response.data.projects)
    }
    },
}
</script>

<style>
.projects {
    min-height: 600px;
    padding-right: 5px;
    padding-left: 5px;
    padding-top: 5px;
    display: grid;
    grid-template-columns: 530px 530px;
    grid-auto-rows: 220px;
}
.project-card {
    width: 97%;
    height: 93%;
    margin: 0 auto 10px auto;
    border-radius: 20px;
    display: grid;
    grid-template-columns: 202px 1fr;
    grid-template-rows: 158px;
    border: 1px solid #e7e7e7;
    box-shadow: 1px 1px 8px rgba(0,0,0,0.3);
}
.project-card:hover {
    background-color: #f5f5f5;
    box-shadow: 5px 5px 10px rgba(0,0,0,0.3);
}
.project-img {
    border-top-left-radius: 20px;
    padding-top: 0.5px;
}
.project-general-info {
    margin: 0px;
    padding-left: 5px;
    display: grid;
}
.project-li-stat {
    display: inline; 
    margin-right: 5px;
}
.project-stat {
    list-style: none;
    padding-left: 0px;
    text-align: center;
}
.project-index {
    text-align: right;
    margin-right: 5px;
    margin-top: 5px;
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 1;
    grid-row-end: 1;
}
.project-name {
    margin-bottom: 0px;
    font-size: 1.3em;
    text-align: center;
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 2;
    grid-row-end: 2;
}
.project-fields {
    text-align: center;
    color: #939292;
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 3;
    grid-row-end: 3;
}
.project-image {
   grid-column-start: 1;
   grid-column-end: 2;
   grid-row-start: 1;
   grid-row-end: 2;
}
.project-stats {
   grid-column-start: 1;
   grid-column-end: 3;
   grid-row-start: 2;
   grid-row-end: 2;
}
p {
    margin: 0px;
}
.project-open-btn1, .project-open-btn2 {
    margin-right: 5px;
    cursor: pointer;
    width: 140px;
    height: 28px;
}
</style>
