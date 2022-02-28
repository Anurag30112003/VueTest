<script>
    export default {
        name: 'About',
        data() {
            return {
                name: 'Anurag',
                Description: '      Hello I am full stack web developer with a passion for building web applications I have experience in building web applications ',
                tech:['React','VueJS','Express'],
                LookingFor: 'I am looking for a job in the field of Web Development or in Developer Advocate.',
            }
        }
    }
</script>
<template lang="pug">
.about
    h1 About
    p Hi,My name is {{name}}.
    //- Add a link in the description
    p {{Description}}   
     a(href="https://reactjs.org") {{tech[0]}}  
      a(href="https://vuejs.org/") {{tech[1]}} 
       a(href="https://expressjs.com/") {{tech[2]}}
    p and many more.
    p {{LookingFor}}
    </template>
<style scoped>
h1 {
    text-align: center;
    font-size: 3.5em;
    color: #999;
    margin-bottom: 0;
}
p {
    margin: 1;
    font-size: 25px;
}
</style>