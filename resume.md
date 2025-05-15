<head>
  <meta charset="UTF-8">
  <title>Mohammad Massri - Backend Developer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 40px;
    }
    h1, h2, h3 {
      color: #333;
    }
    .button-container {
      margin-top: 10px;
    }
    .download-btn {
      padding: 10px 15px;
      font-size: 14px;
      color: white;
      background-color: #007BFF;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    ul {
      list-style-type: disc;
      margin-left: 20px;
    }
  </style>
  
<div id="resume">

<h1>Mohammad Massri</h1>
  <p><strong>Backend Developer</strong></p>
  <p>📍 Tripoli, Lebanon<br>
     📞 +961 81462533<br>
     📧 mouhamaddev04@gmail.com</p>

  <div class="button-container">
    <button class="download-btn" onclick="downloadPDF()">Download PDF</button>
  </div>

  <h2>Summary</h2>
  <p>Experienced backend developer proficient in Python, specializing in server-side applications, database management, and API development.</p>

  <h2>Skills</h2>
  <ul>
    <li>Python</li>
    <li>Django & Django REST Framework</li>
    <li>PHP</li>
    <li>MySQL</li>
    <li>REST API Design</li>
    <li>Linux</li>
    <li>Git & Version Control</li>
    <li>Docker & Containerization</li>
  </ul>

  <h2>Experience</h2>

  <h3>Backend Developer</h3>
  <p><strong>WZTechno</strong><br>
  <em>Sep 2024 – Present</em></p>
  <ul>
    <li>Built a Technician Management System for a laptop/electronics repair company.</li>
    <li>Developed features to manage technician tasks, repair orders, and reporting tools.</li>
    <li>Used Django to create a secure and performant backend.</li>
    <li>Collaborated with the team to enhance features based on technician feedback.</li>
  </ul>

  <h3>Backend Developer</h3>
  <p><strong>Waffershop</strong><br>
  <em>Apr 2023 – Sep 2024</em></p>
  <ul>
    <li>Led backend development for ERP systems and mobile app dashboards.</li>
    <li>Utilized Django, DRF, and Angular to streamline operational workflows.</li>
    <li>Deployed apps using Docker, EC2, and AWS services (S3, etc).</li>
    <li>Ensured backend stability through unit and integration testing.</li>
    <li>Mentored junior developers on best practices in Git and clean code.</li>
    <li>Participated in code reviews and team collaboration meetings to improve code quality.</li>
  </ul>

  <h3>Mobile App Developer (Freelance)</h3>
  <p><strong>freelancer.com</strong><br>
  <em>Aug 2021 – Jan 2023</em></p>
  <ul>
    <li>Delivered multiple React Native mobile apps across industries.</li>
    <li>Contributed to <em>iSeaTree</em>, a citizen science app for tree tracking using AR (DBH calculation).</li>
    <li>Developed an Uber clone app with complete booking and ride interface for users and drivers.</li>
  </ul>

</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
<script>
  function downloadPDF() {
    const resume = document.getElementById('resume');
    const button = document.querySelector('button');
    button.style.display = 'none';

    resume.style.fontSize = '11px';
    resume.style.margin = '0.5in';

    const opt = {
      margin:       0.3,
      filename:     'Mohammad Massri - Backend Engineer - Resume.pdf',
      image:        { type: 'jpeg', quality: 0.98 },
      html2canvas:  { scale: 5 },
      jsPDF:        { unit: 'in', format: 'a4', orientation: 'portrait' }
    };

    html2pdf().set(opt).from(resume).save().then(() => {
      button.style.display = 'inline-block';
      resume.style.fontSize = '';
      resume.style.margin = '';
    });
  }
</script>
