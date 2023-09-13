<script>
  import Header from './Header.svelte';
  import Experience from './Experience.svelte';
  import Education from './Education.svelte';
  import Skills from './Skills.svelte';
  import Certifications from './Certifications.svelte';

  let headerData = {
    name: "MANAS PRATIM SARMA",
    title: "Full Stack Developer || Software Developer",
    phone: "+(91)93653 32364",
    email: "manas_sarma121@protonmail.com",
    linkedin: "linkedin.com/in/manassarma13",
    github: "github.com/manassarma13",
    location: "Guwahati, Assam",
  };

  let experienceData = [
    {
      position: "Front End Developer",
      company: "VENTUNO TECHNOLOGIES, Chennai",
      date: "Sep 2021 - present",
      description: `
        - Developed EPG (Electronic Program Guide) Widget for an OTT platform using React.js (Typescript) + SCSS [as an intern].
        - As an employee, worked on different OTT platforms, created new components, added and updated legacy code to implement new features and fixed bugs using React.Js, Typescript/JavaScript + SCSS + Git.
        - Set up Sonar and ES Linting tools, Testing tools and Test servers to maintain code quality.
        - API documentation, development, debugging, and testing using Postman.
        - Wrote unit and integrated test cases using RTL and Jest. And also e2e testing with unit test cases using Cypress.
        - Source control with Git, used Git Tags for maintaining version and GitHub Actions to implement CI/CD.
        - Made multiple POCs of features using JavaScript with proper documentation
        - Implemented performance optimization strategies targeting Core Web Vitals including CLS, LCP, FID, FCP, etc to optimize the SEO score of the corporate website written in php.
      `,
      skills: "React Js JavaScript Typescript Scss React Testing Library Jest Cypress GIT Sonar Linting",
    },
    {
      position: "Freelancer",
      company: "LOCAL BUSINESSES AND CLIENTS, Guwahati & Remote",
      date: "Aug 2019 - May 2021",
      description: `
        - Helped a few local clients grow their businesses:
        - Proficiently utilized Node.js to build server-side logic, optimizing application performance and scalability.
        - Leveraged Node.js and Express.js to create robust and efficient API endpoints, enhancing data communication and user experience.
        - Implemented real-time features using technologies like Socket.IO in Node.js, enabling instant communication and dynamic updates within applications.
        - Implemented best security practices, including validation, parameterized queries, and security headers.
        - Documented codebase thoroughly in Notion.
        - Continuously refactored and improved codebase to reduce technical debt and enhance maintainability.
        - Android app development using React Native and Android Studio and Firebase to authenticate and use as a database. Created the UI design in Figma.
      `,
      skills: "NodeJs Firebase React Native Android Studio Figma WordPress",
    },
    {
      position: "Robotics, Game Development and Web Development Trainer",
      company: "BeBright",
      date: "Sept 2018 - Aug 2019",
      description: `
        - Taught basics of front end web development HTML, CSS and JavaScript and helped them create some good looking interactive websites of their own.
        - Taught basics of Game Development and Design as well as basic graphics designing in order to design their own assets and producing simple music [sfx] for their games. Used free and open source software for the training.
        - Assisted in a robotics summer camp.
      `,
      skills: "HTML CSS JS GIMP Construct2 Arduino Robotics",
    }
  ];

  let educationData = "2020 Bachelor of Technology, in Electronics and Communication Department, Assam Science and Technology University(ASTU).";

  let skillsData = [
    "Programming Languages JavaScript ,Typescript, Java, Kotlin",
    "UI Frameworks ReactJs, NextJs Angular2 +, Svelte",
    "Backend Languages NodeJS with Express, Golang with Fiber",
    "Mobile Frameworks React Native, Android Studio",
    "Styling Frameworks Bootstrap, Material UI, Tailwind CSS",
    "Database MySQL, SQLite, Firebase, MongoDB",
    "Additional Software Experimented DaVinci Resolve, Cubase AI, GIMP, Audacity, Adobe Photoshop, Adobe Illustrator",
  ];

  let certificationsData = [
    "2012 Diploma in Hardware Engineering [ETGr]",
    "2020 Udemy MEAN Stack Guide https://ude.my/UC-8bcf3158-13ef-4fcb-8ac5-11353f570245",
    "2021 JavaScript Algorithms and Data Structures http://ude.my/UC-d98fa3d3-0f6f-4a3d-a1b6-4beba293475b",
  ];
</script>

<Header {...headerData} />
<h2>Experience</h2>
{#each experienceData as item (item)}
  <Experience {...item} />
{/each}

<Education {educationData} />

<Skills {skillsData} />

<Certifications {certificationsData} />
