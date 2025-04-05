<template>
  <q-page class="q-gutter-md">

    <div class="q-gutter-md text-container">


      <div class="image-container q-mb-md">
        <div class="flex-container">
          <img alt="Photo" src="https://avatars.githubusercontent.com/u/42941626" class="responsive-image">

          <div class="text">
            <p class="responsive-text">{{ me }}</p>
            <p class="responsive-text2">{{ degree }}</p>
            <p class="responsive-text2">{{ field }}</p>

          </div>
        </div>

        <div class="random-text"><br>

          <b>
            <p>About me</p>
          </b>
          <hr>
          Passionate PhD student, doing research in the areas of critical systems and mobile networks.
          With a background in electronics and telecommunications, I hold a bachelor's degree in Electrical Engineering
          from the Federal University of Espirito Santo (UFES, ES - Brazil), a double diploma in Computer Engineering
          from Telecom Paris (Palaiseau, France), and a master's degree in embedded systems and information processing
          from the Institut Polytechnique de Paris (Palaiseau, France).
          <br>
          I completed the first year of his master’s degree focusing on Embedded Systems, Mobile Networks, and the
          Internet of Things (IoT).
          Over a summer internship in 2023, I was part of the control and acquisition engineering team at SOLEIL, a
          synchrotron facility near Paris, working on a project dedicated to the centralized supervision of industrial
          programmable logic controllers (PLCs).
          Afterward, I pursued a Master 2 in Embedded Systems and Information Processing (M2 SETI), completing my degree
          with an end-of-studies project at Orange SA, focusing on remote access to Matter IoT devices.
          <br>
          As an Electrical Engineering student in Brazil at the Federal University of Espírito Santo (UFES), I was in
          the Telecommunications Laboratory (LabTel) research team, where I developed my bachelor’s final project titled
          ‘Multiplatform System for Data Reception via Visible Light Communication Technology’.
          At LabTel, I engaged in several research projects in Visible Light Communications.
          <br>
          Additionally, I worked as an Automation Intern at the Cassiano Antonio Moraes University Hospital (HUCAM) and
          as an Embedded Systems and IoT R&D intern at 2Solve Engineering and Technology.
          During my undergraduate studies, I participated in various projects and organizations, including the Museum of
          Life Sciences, the Academic Center of Electrical Engineering, and the Tutorial Education Program.



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

          <div>
            <b>
              <p>Experience</p>
            </b>
            <hr>
            <div v-for="(exp, index) in experience" :key="index">
              <p>{{ exp.duration }} - {{ exp.position }}</p>
              <p>{{ exp.company }}, {{ exp.location }}</p>
              <ul>
                <li v-for="(detail, index) in exp.details" :key="index">{{ detail }}</li>
              </ul>
              <br>
            </div>
          </div>

          <div>
            <b>
              <p>Education</p>
            </b>
            <hr>
            <div v-for="(edu, index) in education" :key="index">
              <p>{{ edu.duration }} - {{ edu.degree }}</p>
              <p>{{ edu.institution }}</p>
              <ul>
                <li v-for="(detail, index) in edu.details" :key="index">{{ detail }}</li>
              </ul>
            </div>
          </div>

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
          2018 – 2019 - Activity Manager.<br>
          Academic Center of UFES Electrical Engineering, Vitória, Brazil.<br>
          Organization of welcome events for freshmen, organization of lectures on subjects of interest to graduation,
          promotion of sports events, electrical engineering custom t-shirts selling, maintenance of the study room.
          <br><br>
          2018 - Museum Mediator.<br>
          UFES Museum of Life Sciences, Vitória, Brazil.<br>
          Introduce the museum to visitors, control the flow of people, and pass safety guidelines.


          <br><br>
          <b>
            <p>Honours and Awards</p>
          </b>
          <hr>

          2025 - Honorable Mention, Find Me on the Moon: NASA Lunar Navigation Challenge.
          National Aeronautics and Space Administration (NASA), USA.
          Selene Squad: rover designed for navigating, mapping, and characterizing the Shackleton Crater.<a
            href="https://www.freelancer.com/community/articles/find-me-on-the-moon-nasa-lunar-navigation-challenge-winners-announced">Winners
            Announcement</a>.


          <br><br>
          2022 – 2024 - BRAFITEC scholarship.<br>
          CAPES Foundation, Brazil.<br>
          Master's degree funding granted based on criteria of academic and technical excellence.

          <br><br>
          2016 - Honorable Mention Brazilian Public School Mathematics Olympiad.<br>
          Institute of Pure and Applied Mathematics (IMPA), Rio de Janeiro, Brazil.<br>
          Stood out in mathematics at this Olympiad, being the only high school student out of around 500 in the school
          to
          receive this award.

          <br><br>
          2015 – 2016 - Outstanding certificate at the São João Batista School Science Fair.<br>
          EEEFM São João Batista (High School), Cariacica, Brazil.<br>
          2016 (1st place) - Physics project involving basic concepts of electromagnetism to wirelessly turn on
          lamps.<br>
          2015 (2nd place) - Tesla coil capable of creating electric arcs of a few centimeters.


          <br><br>
          <b>
            <p>Language Skills</p>
          </b>
          <hr>
          Portuguese - Native Language.<br>
          English - Advanced (C1, 2024). Cambridge Linguaskill B2 (178 out of 180), 2022.<br>
          French - Advanced (C1, 2024). Test de Connaissance du Français B2 (488 out of 699), 2021.<br>
          Spanish - Intermediate (B1, 2024).<br>
          Italian & Galician: Basic knowledge.

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
      me: "Alaf Nascimento",
      degree: "IPP PhD Student at Télécom Paris",
      field: "Computer Science and Telecommunications Engineering",
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
      ],
      education: [
        {
          duration: "2024 – 2027",
          degree: "Doctor of Philosophy (PhD) in Engineering",
          institution: "Institut Polytechnique de Paris, Palaiseau, France.",
          details: [
            "Research Subject: Real-time scheduling for 5G NR SCADA systems."
          ]
        },
        {
          duration: "2022 – 2024",
          degree: "Master of Science (MSc) in Engineering",
          institution: "Télécom Paris, Institut Polytechnique de Paris, Palaiseau, France. Double degree programme.",
          details: [
            "M1: Embedded systems, mobile networks, and the internet of things.",
            "M2: Embedded systems and information processing.",
            "Master project: Modelling the critical real-time execution of a 5G base station."
          ]
        },
        {
          duration: "2017 – 2024",
          degree: "Bachelor of Science (BSc) in Electrical Engineering",
          institution: "Federal University of Espírito Santo, Vitória, Brazil. Double degree programme.",
          details: [
            "Control and automation systems, telecommunications, and computer science.",
            "Final Project: Multiplatform System For Data Reception Via Visible Light Communication Technology."
          ]
        }
      ],
      experience: [
        {
          duration: "2024",
          position: "NAI Project (PEPR 5G) Researcher",
          company: "LTCI, Telecom Paris",
          location: "Palaiseau, France",
          details: [
            "Research on the real-time aspects of URLLC in 5G, mainly the application of critical systems task scheduling algorithms.",
            "Teaching activities on Embedded Systems and Mobile Networks."
          ]
        },
        {
          duration: "2024",
          position: "Embedded Systems and IoT Intern.",
          company: "Orange S.A.",
          location: "Meylan, France",
          details: [
            "Development of an application for remote access to Matter devices.",
            "Embedded software for an IoT gateway based on ARM Cortex-A processor."
          ]
        },
        {
          duration: "2023",
          position: "Network and Automation Intern",
          company: "Synchrotron SOLEIL",
          location: "Saint-Aubin, France",
          details: [
            "Software tool parameterization dedicated to centralized supervision of Siemens PLCs (S7-3xx and S7-15xx).",
            "Coverage of over 98% of the targeted devices, through a solution based on the S7 and SNMP protocols.",
            "Real-time monitoring tool: Zabbix;",
            "Programming languages: Python, C/C++, and CMake."
          ]
        },
        {
          duration: "2021 – 2022",
          position: "Embedded Systems and IoT R&D intern",
          company: "2Solve Engineering and Technology",
          location: "Vitória - ES, Brazil",
          details: [
            "Development of software for embedded systems, IoT Web Applications, and technical documentation.",
            "Embedded systems based on Raspberry Pi and SAMD21.",
            "Programming languages: Javascript, Python, C/C++, and CMake.",
            "Dev tools: NodeJS, AngularJS, InfluxDB, and MongoDB.",
            "IoT tools: Node-RED and Grafana.",
            "Research project: Design of an OOK transmitter for short-link visible light data communication."
          ]
        },
        {
          duration: "2019 – 2021",
          position: "Scientific and Technological Undergraduate Researcher",
          company: "UFES Telecommunications Laboratory (LabTel)",
          location: "Vitória, Brazil",
          details: [
            "Software and hardware design for visible light communication systems (VLC systems).",
            "Dev tools: Android Studio, NodeJS, VueJS.",
            "Programming languages: MatLab, Java, Python, and C++.",
            "Research projects:",
            "1. Application of Visible Light Communication Technology in Monitoring High-Risk Newborns;",
            "2. SmaL: Smartphone Receiver for Coded Data via Light.",
            "Publications: [1], and [2]."
          ]
        },
        {
          duration: "2019 – 2020",
          position: "Automation Intern",
          company: "Cassiano Antonio Moraes University Hospital (HUCAM)",
          location: "Vitória, Brazil",
          details: [
            "Establishment of electronics for a supervisory system, data monitoring app, and creating technical documentation.",
            "Embedded systems based on Raspberry Pi, Arduino, and ESP8266.",
            "Real-time monitoring tool: Zabbix.",
            "Programming languages: Python, Javascript, and C++.",
            "Publications: [4]"
          ]
        },
        {
          duration: "2019",
          position: "Scholar in educational programme",
          company: "Tutorial Teaching Program (PET)",
          location: "Vitória, Brazil",
          details: [
            "Software training, such as LaTex.",
            "Research about embedded systems.",
            "Production of scientific articles.",
            "Embedded systems based on Raspberry Pi and Arduino;",
            "Programming languages: MatLab, Python and C/C++.",
            "Publications: [3]"
          ]
        },
      ]
    };
  }
})
</script>
