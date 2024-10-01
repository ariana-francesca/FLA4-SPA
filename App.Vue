<template>
  <div id="resume">
    <img src="./assets/pic.jpg">
    <h1>{{ profile.name }}</h1>
    <p><strong>Objective:</strong> {{ profile.objective }}</p>
    <p><strong>Course:</strong> {{ profile.course }}</p>
    <p><strong>Specialization:</strong> {{ profile.specialization }}</p>

    <h2 id="comp">Education</h2>
    <ul>
      <li>
        <strong>Elementary:</strong> {{ education.elementary.name }} ({{ education.elementary.years }})
      </li>
      <li>
        <strong>JHS/SHS:</strong> {{ education.jhs.name }} ({{ education.jhs.years }})
      </li>
      <li>
        <strong>College:</strong> {{ education.college.degree }} from {{ education.college.institution }} ({{ education.college.years }})
      </li>
    </ul>

    <h2 id="comp">Skills</h2>
    <h3 id="skills">Training</h3>
    <ul>
      <li v-for="item in skills.training" :key="item">{{ item }}</li>
    </ul>

    <h3 id="skills">Seminars</h3>
    <ul>
      <li v-for="item in skills.seminars" :key="item">{{ item }}</li>
    </ul>

    <h3 id="skills">Technologies</h3>
    <ul>
      <li v-for="item in skills.technologies" :key="item">{{ item }}</li>
    </ul>

    <h3 id="skills">Programming Languages</h3>
    <ul>
      <li v-for="item in skills.languages" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      profile: {
        name: "Ariana Francesca N. Punsalang",
        objective: "Aspiring web developer seeking an internship position to leverage my skills in HTML, CSS, and JavaScript to create dynamic web applications and contribute to innovative projects.",
        course: "Bachelor of Science in Information Technology",
        specialization: "Web Development"
      },
      education: {
        elementary: {
          name: "Sto.Rosario Elementary School",
          years: "-"
        },
        jhs: {
          name: "Holy Angel University",
          years: "-"
        },
        college: {
          degree: "Bachelor of Science in Information Technology",
          institution: "Holy Angel University",
          years: "-"
        }
      },
      skills: {
        training: ["Full-Stack Web Development Bootcamp", "Introduction to Data Science"],
        seminars: ["Future of Web Development", "Cybersecurity Awareness"],
        technologies: ["HTML", "CSS", "JavaScript", "Vue.js"],
        languages: ["JavaScript", "Python", "Java"]
      }
    };
  }
};
</script>

<style>
#resume {
  margin: 0 auto;
  font-family: Arial, sans-serif;
  background-color: #0B192C ;
  color: antiquewhite;
  text-align: center;
}

h2 {
  border-bottom: 2px solid #ccc;
}

h1 {
  padding: 5px;
  font-size: .8cm;
}

strong {
  color: burlywood;
}

#skills {
  font-weight:bold ;
  color: burlywood;
}

#comp {
  font-size: 25px;
  color: aquamarine;
}

img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 25%; 
  height: 25%;
  padding-top: 25px;
}


</style>
