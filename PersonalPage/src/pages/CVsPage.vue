<template>
    <q-page class="q-gutter-md">
  
  
      <div class="q-gutter-md text-container">
        <div class="image-container q-mb-md">
          <img alt="Photo" src="https://avatars.githubusercontent.com/u/42941626" class="responsive-image">
        </div>
        <div class="q-mb-md text">
          <p class="responsive-text">{{ me }}</p>
          <p class="responsive-text2">{{ title }}</p>
  
          <div class="random-text">
            <p>
              Here you can find my
              <a href="CVs/cv1.pdf">CV</a>, <a href="CVs/cv2.pdf">academic CV</a>
              and
              <a href="CVs/resume1.pdf">Resume</a>.
            </p>
            <p>
              Ici vous pouvez trouver mon
              <a href="CVs/resume2.pdf">CV</a>.
            </p>
            <p>
              Aqui você pode encontrar meu
              <a href="CVs/cv3.pdf">curriculo completo</a>
              e
              <a href="CVs/resume3.pdf">curriculo resumido</a>.
            </p>
          </div>
        </div>
      </div>
  
    </q-page>
  </template>
  
  <style>
  .responsive-image {
    max-width: 100%;
    height: auto;
  }
  
  .text-container {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
  
  .responsive-text {
    font-size: 40px;
  }
  
  .responsive-text2 {
    font-size: 30px;
  }
  
  .random-text {
    font-size: 24px;
  }
  
  @media (max-width: 768px) {
    .random-text {
      font-size: 18px;
    }
  
    .responsive-text2 {
      font-size: 25px;
    }
  
    .responsive-text {
      font-size: 30px;
    }
  
  }
  
  @media (max-width: 480px) {
    .random-text {
      font-size: 16px;
    }
  
    .responsive-text2 {
      font-size: 20px;
    }
  
    .responsive-text {
      font-size: 25px;
    }
  
  }
  </style>
  
  <script>
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'IndexPage',
    data() {
      return {
        me: "Alaf DO NASCIMENTO SANTOS",
        title: "Master of Science in Engineering - Institut Polytechnique de Paris"
      };
    }
  })
  </script>
  