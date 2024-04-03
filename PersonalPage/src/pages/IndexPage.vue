<template>
  <q-page class="q-gutter-md">

    <div class="q-gutter-md text-container">

      
      <div class="image-container q-mb-md">
        <div class="flex-container">
          <img alt="Photo" src="https://avatars.githubusercontent.com/u/42941626" class="responsive-image">
  
          <div class="text">
            <p class="responsive-text">{{ me }}</p>
            <p class="responsive-text2">{{ field }}</p>
            <p class="responsive-text2">{{ degree }}</p>
            
          </div>
        </div>

        <div class="random-text"><br>

          <b>
            <p>About me</p>
          </b>
          <hr>
          Passionate master's student in electrical engineering with a background in telecommunications and automation, holding a history of presenting at conferences and writting research papers, principally in the area of the
          Internet of Things (IoT). Throughout my career I have received awards in maths, physics and recently a
          scholarship based on academic and technical excellence. I am currently seeking a Ph.D. programme in Engineering
          aiming to delve further into the IoT world and Digital Twins.

          <br><br>
          <b>
            <p>Research Interests</p>
          </b>
          <hr>
          <ul>
            <li v-for="(item, index) in research" :key="index">
              {{ item }}
            </li>
          </ul>

          <b>
            <p>Experience</p>
          </b>
          <hr>
          2024 - Embedded Systems and IoT Intern.
          Orange S.A., Meylan, France.
          Development of an application for remote access to Matter devices.
          Embedded software for an IoT gateway based on ARM Cortex-A processor.

          <br>
          2023 - Network and Automation Intern.
          Synchrotron SOLEIL, Saint-Aubin, France.
          Software tool parameterisation dedicated to centralised supervision of Siemens PLCs (S7-3xx and S7-15xx).
          Coverage of over 98 % of the targeted devices, through a solution based on the S7 and SNMP protocols.
          Real-time monitoring tool: Zabbix;
          Programming languages: Python, C/C++, and CMake.

          <br>
          2021 – 2022 - Embedded Systems and IoT R&D intern.
          2Solve Engineering and Technology, Vitória, Brazil.
          Development of software for embedded systems, IoT Web Applications, and technical documentation.
          Embedded systems based on Raspberry Pi and SAMD21.
          Programming languages: Javascript, Python, C/C++, and CMake.
          Dev tools: NodeJS, AngularJS, InfluxDB, and MongoDB.
          IoT tools: Node-RED and Grafana.
          Research project:
          Design of an OOK transmitter for short-link visible light data communication.

          <br>
          2019 – 2021 - Scientific and Technological Undergraduate Researcher.
          UFES Telecommunications Laboratory (LabTel), Vitória, Brazil.
          Software and hardware design for visible light communication systems (VLC systems).
          Dev tools: Android Studio, NodeJS, VueJS.
          Programming languages: MatLab, Java, Python, and C++.
          Research projects:
          Application of Visible Light Communication Technology in Monitoring High-Risk Newborns;
          SmaL: Smartphone Receiver for Coded Data via Light.
          Publications: [1], and [2].

          <br>
          2019 – 2020 - Automation Intern.
          Cassiano Antonio Moraes University Hospital (HUCAM), Vitória, Brazil.
          Establishment of electronics for a supervisory system, data monitoring app, and creating technical
          documentation.
          Embedded systems based on Raspberry Pi, Arduino, and ESP8266.
          Real-time monitoring tool: Zabbix.
          Programming languages: Python, Javascript, and C++.
          Publications: [4]

          <br>
          2019 - Scholar in educational programme.
          Tutorial Teaching Program (PET), Vitória, Brazil.
          Software training, such as LaTex. Research about embedded systems. Production of scientific articles.
          Embedded systems based on Raspberry Pi and Arduino;
          Programming languages: MatLab, Python and C/C++.
          Publications: [3]


          <br><br>
          <b>
            <p>Education</p>
          </b>
          <hr>
          2022 – 2024 - Master of Science in Engineering.<br>
          Télécom Paris, Polytechnic Institute of Paris, Palaiseau, France. Double degree programme.<br>
          &nbsp;&nbsp;&nbsp;&nbsp;M1: Embedded systems, mobile networks, and the internet of things.<br>
          &nbsp;&nbsp;&nbsp;&nbsp;M2: Embedded systems and information processing.<br>
          &nbsp;&nbsp;&nbsp;&nbsp;Master project: Modelling the critical real-time execution of a 5G base station.

          <br><br>
          2017 – 2024 - Bachelor of Science in Electrical Engineering.<br>
          Federal University of Espírito Santo, Vitória, Brazil. Double degree programme.<br>
          &nbsp;&nbsp;&nbsp;&nbsp;Control and automation systems, telecommunications, and computer science.<br>
          &nbsp;&nbsp;&nbsp;&nbsp;Final Project: Multiplatform System For Data Reception Via Visible Light Communication Technology.

          <br><br>
          <b>
            <p>Publications, Theses, and Appearances</p>
          </b>
          <hr>
          <ul>
            <li v-for="(item, index) in pubs" :key="index">
             [{{ index + 1 }}] {{ item }}
            </li>
          </ul>

          <b>
            <p>Volunteering</p>
          </b>
          <hr>
          2018 – 2019 - Activity Manager.
          Academic Center of UFES Electrical Engineering, Vitória, Brazil.
          Organization of welcome events for freshmen, organization of lectures on subjects of interest to graduation,
          promotion of sports events, electrical engineering custom t-shirts selling, maintenance of the study room.
          <br>
          2018 - Museum Mediator.
          UFES Museum of Life Sciences, Vitória, Brazil.
          Introduce the museum to visitors, control the flow of people, and pass safety guidelines.


          <br><br>
          <b>
            <p>Honours and Awards</p>
          </b>
          <hr>
          2022 – 2024 - BRAFITEC scholarship.
          CAPES Foundation, Brazil.
          Master's degree funding granted based on criteria of academic and technical excellence.

          <br>
          2016 - Honorable Mention Brazilian Public School Mathematics Olympiad.
          Institute of Pure and Applied Mathematics (IMPA), Rio de Janeiro, Brazil.
          Stood out in mathematics at this Olympiad, being the only high school student out of around 500 in the school to
          receive this award.

          <br>
          2015 – 2016 - Outstanding certificate at the São João Batista School Science Fair.
          EEEFM São João Batista (High School), Cariacica, Brazil.
          2016 (1st place) - Physics project involving basic concepts of electromagnetism to wirelessly turn on lamps.
          2015 (2nd place) - Tesla coil capable of creating electric arcs of a few centimeters.


          <br><br>
          <b>
            <p>Language Skills</p>
          </b>
          <hr>
          Portuguese - Native Language.<br>
          English - C1, 2024. Cambridge Linguaskill B2 (178 out of 180), 2022.<br>
          French - C1, 2024. Test de Connaissance du Français B2 (488 out of 699), 2021.<br>
          Spanish - A2, 2024.

        </div>

      </div>

    </div>

  </q-page>
</template>

<style>
.flex-container {
  display: flex;
  align-items: center;
}

.text {
  margin-left: 20px;
  /* Adjust the margin as needed */
}


.responsive-image {
  max-width: 100%;
  height: auto;
}

.text-container {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 60vh;
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
      title: "IoT and Embedded Systems Engineer",
      me: "Alaf DO NASCIMENTO SANTOS",
      field: "Electronics and Telecommunications Engineering",
      degree: "Master in Embedded Systems and Information Processing",
      pubs: [
        "ZWAAG, K., ROCHA, H., SEGATTO, M., BASTOS, T., SILVA, J., SANTOS, F., SANTOS, A. et al., 2021. Performance Evaluation of an OOK - Based Visible Light Communication System for Transmission of Patient Monitoring Data.IFMBE Proceedings.",
        "SANTOS, A., ROCHA, H., SEGATTO, M., BASTOS, T., SILVA, J., ZWAAG, K.et al., 2020. Application of Visible Light Communication Technology for Monitoring in Hospitals.Brazilian Congress on Biomedical Engineering.",
        "SANTOS, A., JURESWKI, A., MENDONÇA, M., ULHOA, P., 2020. History of PET Electrical Engineering UFES.Brazilian Congress of Engineering Education.",
        "SANTOS, A., JUNIOR, L., JARDIM, I., 2020. Low - Cost Module for Supervisory System of Hospital Substations.In: Congresso Internacional Online das Engenharias."
      ],
      research: [
        "Real-time systems",
        "Embedded Software",
        "Embedded Artificial Intelligence",
        "Mobile Networks",
        "Internet of Things",
        "Visible Light Communication",
        "Digital Twins",
      ]
    };
  }
})
</script>
