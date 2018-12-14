<template>
    <div class="projects" id="project-card">           
        
    </div>
</template>
<script>
import axios from 'axios';
export default {
    mounted() {
    axios
        .get('https://api.behance.net/v2/projects?q=motorcycle&client_id=UQHakERSArHWQGtYuuN0vuWbWFcPdtcL')
        .then(response => this.projects = response.data)
        .then(projects =>
        {
            let output = '';
            let project = projects.projects;
    
            for (let i = 0; i < 10; i++) {
                let random = Math.floor(Math.random() * project.length)
                output += `
                <div class="project-card">
                    <div class="box1 project-image">
                        <img src="${project[random].covers[202]}" class="project-img">
                    </div>
                    <div class="box2 project-general-info">
                        <p class="project-index">Индекс: ${project[random].id}</p>
                        <p class="project-name">Название: ${project[random].name}</p>
                        <p class="project-fields">Категория: <br>${project[random].fields}</p>
                    </div>
                    <div class="box3 project-fields">
                        
                        <ul class="project-stats">
                            <li class="project-li-stat">Просмотров: ${project[random].stats.views}</li> 
                            <li class="project-li-stat">Благодарностей: ${project[random].stats.appreciations}</li>
                            <li class="project-li-stat">Комментариев: ${project[random].stats.comments}</li>
                        </ul>
                    </div>
                    
                </div>`;
                }

                document.getElementById('project-card').innerHTML = output;
        })
        
    }
}
</script>

<style>
.projects {
    min-height: 600px;
    padding-right: 5px;
    padding-left: 5px;
    padding-top: 5px;
    display: grid;
    grid-template-columns: 475px 475px;
    grid-auto-rows: 250px;
}
.project-card {
    width: 97%;
    height: 97%;
    background-color: #f5f5f5;
    margin: 0 auto;
    border-radius: 20px;
    display: grid;
    grid-template-columns: 202px 258px;
    grid-template-rows: 158px;
    border: 1px solid #e7e7e7;
}
.project-img {
    border-top-left-radius: 20px;
}
.project-general-info {
    margin: 0px;
    padding-left: 5px;
}
.project-fields {
    
}
.project-li-stat {
    display: inline; 
    margin-right: 5px;
}
.project-stats {
    list-style: none;
    padding-left: 0px;
    text-align: center;
}
.project-index {
    float: right;
    margin-bottom: 0px;
    margin-top: 5px;
    padding-right: 10px;
}
.project-name {
    margin-top: 30px;
    margin-bottom: 0px;
}
.box1 {
   grid-column-start: 1;
   grid-column-end: 2;
   grid-row-start: 1;
   grid-row-end: 2;
}
.box3 {
   grid-column-start: 1;
   grid-column-end: 3;
   grid-row-start: 2;
   grid-row-end: 2;
}
p {
    margin: 0px;
}
</style>
