<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dinesh Madhavan - Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    :root {
      --primary: #2dd4bf;
      --secondary: #0ea5e9;
      --dark: #0f172a;
      --light: #f8fafc;
      --gray: #64748b;
      --dark-bg: #020617;
      --card-bg: rgba(30, 41, 59, 0.7);
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    
    body {
      background: var(--dark-bg);
      color: var(--light);
      line-height: 1.6;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem;
    }
    
    /* Header Section */
    .header {
      text-align: center;
      padding: 4rem 0;
      position: relative;
      overflow: hidden;
      border-radius: 1rem;
      margin-bottom: 3rem;
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(6, 78, 59, 0.8));
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }
    
    .profile-banner {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      opacity: 0.1;
      z-index: -1;
    }
    
    .profile-image {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 4px solid var(--primary);
      margin-bottom: 1.5rem;
      transition: transform 0.3s ease;
      box-shadow: 0 0 30px rgba(45, 212, 191, 0.3);
    }
    
    .profile-image:hover {
      transform: scale(1.05);
    }
    
    .typing-text {
      font-size: 2.5rem;
      font-weight: 700;
      margin: 1rem 0;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      min-height: 3.5rem;
    }
    
    .tagline {
      font-size: 1.2rem;
      color: var(--gray);
      margin-bottom: 1.5rem;
    }
    
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 1.5rem;
    }
    
    .social-link {
      color: var(--light);
      font-size: 1.5rem;
      transition: all 0.3s ease;
    }
    
    .social-link:hover {
      color: var(--primary);
      transform: translateY(-3px);
    }
    
    /* Section Styling */
    .section {
      margin-bottom: 4rem;
    }
    
    .section-title {
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: var(--light);
      position: relative;
      display: inline-block;
    }
    
    .section-title::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -8px;
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      border-radius: 3px;
    }
    
    /* Skills Section */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1.5rem;
      margin-top: 1.5rem;
    }
    
    .skill-card {
      background: var(--card-bg);
      padding: 1.5rem;
      border-radius: 0.8rem;
      text-align: center;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.05);
    }
    
    .skill-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
      border-color: var(--primary);
    }
    
    .skill-icon {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: var(--primary);
    }
    
    .skill-card h3 {
      margin-bottom: 0.5rem;
      color: var(--light);
    }
    
    .skill-card p {
      color: var(--gray);
      font-size: 0.95rem;
    }
    
    /* Projects Section */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    
    .project-card {
      background: var(--card-bg);
      border-radius: 0.8rem;
      overflow: hidden;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.05);
    }
    
    .project-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
      border-color: var(--primary);
    }
    
    .project-image {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    
    .project-content {
      padding: 1.5rem;
    }
    
    .project-title {
      font-size: 1.3rem;
      margin-bottom: 0.5rem;
      color: var(--light);
    }
    
    .project-description {
      color: var(--gray);
      margin-bottom: 1rem;
      font-size: 0.95rem;
    }
    
    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 1rem;
    }
    
    .tag {
      background: rgba(45, 212, 191, 0.1);
      color: var(--primary);
      padding: 0.3rem 0.8rem;
      border-radius: 50px;
      font-size: 0.8rem;
    }
    
    .project-links {
      display: flex;
      gap: 1rem;
      margin-top: 1rem;
    }
    
    .project-link {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      color: var(--light);
      text-decoration: none;
      font-size: 0.9rem;
      transition: all 0.3s ease;
    }
    
    .project-link:hover {
      color: var(--primary);
    }
    
    /* Stats Section */
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 1.5rem;
      margin-top: 1.5rem;
    }
    
    .stat-card {
      background: var(--card-bg);
      padding: 1.5rem;
      border-radius: 0.8rem;
      text-align: center;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.05);
    }
    
    .stat-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
      border-color: var(--primary);
    }
    
    .stat-number {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    
    /* Experience Section */
    .experience-card {
      background: rgba(255, 255, 255, 0.03);
      border-radius: 0.8rem;
      padding: 1.5rem;
      margin-bottom: 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: all 0.3s ease;
    }

    .experience-card:hover {
      border-color: var(--primary);
      box-shadow: 0 5px 20px rgba(45, 212, 191, 0.1);
    }

    .experience-header {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1rem;
      margin-bottom: 1rem;
    }

    .experience-header h3 {
      font-size: 1.3rem;
      color: var(--light);
      margin: 0;
    }

    .experience-company {
      color: var(--primary);
      font-weight: 600;
    }

    .experience-date {
      margin-left: auto;
      color: var(--gray);
      font-size: 0.9rem;
    }

    .experience-details p {
      margin-bottom: 0.5rem;
      color: var(--gray);
    }

    .experience-list {
      margin: 1rem 0 0 1.5rem;
      list-style: none;
    }

    .experience-list li {
      margin-bottom: 0.5rem;
      color: var(--gray);
      position: relative;
      padding-left: 1.5rem;
    }

    .experience-list li::before {
      content: '▹';
      position: absolute;
      left: 0;
      color: var(--primary);
    }
    
    /* Footer */
    .footer {
      text-align: center;
      padding: 2rem 0;
      color: var(--gray);
      font-size: 0.9rem;
    }
    
    /* Animations */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    .fade-in {
      animation: fadeIn 0.6s ease-out forwards;
    }
    
    .delay-1 { animation-delay: 0.2s; }
    .delay-2 { animation-delay: 0.4s; }
    .delay-3 { animation-delay: 0.6s; }
    
    /* Responsive Design */
    @media (max-width: 768px) {
      .typing-text {
        font-size: 2rem;
      }
      
      .skills-grid {
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
      }
      
      .projects-grid {
        grid-template-columns: 1fr;
      }
      
      .stats-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Header Section -->
    <header class="header fade-in">
      <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Background" class="profile-banner">
      <img src="https://avatars.githubusercontent.com/u/128453260?v=4" alt="Dinesh Madhavan" class="profile-image">
      <h1 class="typing-text" id="typing-text"></h1>
      <p class="tagline">Data Analyst & UI/UX Designer</p>
      
      <div class="social-links">
        <a href="https://github.com/DineshMadhavanM" target="_blank" class="social-link">
          <i class="fab fa-github"></i>
        </a>
        <a href="https://www.linkedin.com/in/dinesh-madhavan-4746292a5/" target="_blank" class="social-link">
          <i class="fab fa-linkedin"></i>
        </a>
        <a href="https://twitter.com/yourusername" target="_blank" class="social-link">
          <i class="fab fa-twitter"></i>
        </a>
        <a href="mailto:your.email@example.com" class="social-link">
          <i class="fas fa-envelope"></i>
        </a>
      </div>
    </header>

    <!-- About Section -->
    <section class="section fade-in delay-1">
      <h2 class="section-title">About Me</h2>
      <p>I'm a passionate Data Analyst and UI/UX Designer with expertise in transforming complex data into actionable insights and creating intuitive, user-centered designs. Currently expanding my expertise in Agentic AI through hands-on projects at Hexgen AI. With a strong foundation in data analysis, visualization, and frontend development, I bridge the gap between data and design to create impactful digital experiences.</p>
    </section>

    <!-- Experience Section -->
    <section class="section fade-in delay-1">
      <h2 class="section-title">Experience</h2>
      <div class="experience-card">
        <div class="experience-header">
          <h3>AI Intern</h3>
          <span class="experience-company">Hexgen AI</span>
          <span class="experience-date">2023 - Present</span>
        </div>
        <div class="experience-details">
          <p>Working on cutting-edge Agentic AI projects, focusing on:</p>
          <ul class="experience-list">
            <li>Developing autonomous AI agents for complex problem-solving</li>
            <li>Implementing natural language processing and machine learning models</li>
            <li>Building scalable AI solutions with Python and modern AI frameworks</li>
            <li>Collaborating with cross-functional teams to deploy AI solutions</li>
            <li>Conducting research on the latest advancements in Agentic AI</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="section fade-in delay-1">
      <h2 class="section-title">Technical Skills</h2>
      <div class="skills-grid">
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-database"></i></div>
          <h3>Data Analysis</h3>
          <p>Python, SQL, Power BI</p>
        </div>
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-paint-brush"></i></div>
          <h3>UI/UX Design</h3>
          <p>html, css, Js</p>
        </div>
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-code"></i></div>
          <h3>Frontend</h3>
          <p>HTML, CSS, JavaScript, React</p>
        </div>
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-server"></i></div>
          <h3>Backend</h3>
          <p>Node.js, Express, MongoDB</p>
        </div>
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-robot"></i></div>
          <h3>AI/ML</h3>
          <p>PyTorch, TensorFlow, LLMs</p>
        </div>
        <div class="skill-card fade-in delay-2">
          <div class="skill-icon"><i class="fas fa-brain"></i></div>
          <h3>Agentic AI</h3>
          <p>Autonomous Agents, LangChain, RAG</p>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="section fade-in delay-1">
      <h2 class="section-title">My Stats</h2>
      <div class="stats-grid">
        <div class="stat-card fade-in delay-2">
          <div class="stat-number" id="github-repos">0</div>
          <p>GitHub Repositories</p>
        </div>
        <div class="stat-card fade-in delay-2">
          <div class="stat-number" id="github-stars">0</div>
          <p>GitHub Stars</p>
        </div>
        <div class="stat-card fade-in delay-2">
          <div class="stat-number" id="github-followers">0</div>
          <p>GitHub Followers</p>
        </div>
        <div class="stat-card fade-in delay-2">
          <div class="stat-number" id="projects-completed">5+</div>
          <p>Projects Completed</p>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section class="section fade-in delay-1">
      <h2 class="section-title">Featured Projects</h2>
      <div class="projects-grid" id="projects-container">
        <!-- Projects will be loaded here by JavaScript -->
      </div>
    </section>

    <footer class="footer fade-in delay-3">
      <p>© 2023 Dinesh Madhavan. All rights reserved.</p>
      <p>Built with ❤️ and ☕</p>
    </footer>
  </div>

  <script>
    // Typing Animation
    const texts = ["Data Analyst", "UI/UX Designer", "AI Enthusiast", "Problem Solver"];
    let count = 0;
    let index = 0;
    let currentText = '';
    let letter = '';
    
    function type() {
      if (count === texts.length) {
        count = 0;
      }
      currentText = texts[count];
      letter = currentText.slice(0, ++index);
      
      document.getElementById('typing-text').textContent = letter;
      if (letter.length === currentText.length) {
        count++;
        index = 0;
        setTimeout(type, 2000);
      } else {
        setTimeout(type, 100);
      }
    }
    
    // Start typing animation
    document.addEventListener('DOMContentLoaded', () => {
      setTimeout(type, 1000);
      
      // Animate elements on scroll
      const animateOnScroll = () => {
        const elements = document.querySelectorAll('.fade-in');
        elements.forEach(element => {
          const elementTop = element.getBoundingClientRect().top;
          const windowHeight = window.innerHeight;
          
          if (elementTop < windowHeight - 100) {
            element.style.opacity = '1';
            element.style.transform = 'translateY(0)';
          }
        });
      };
      
      // Set initial state
      document.querySelectorAll('.fade-in').forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(20px)';
        el.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
      });
      
      // Add scroll event listener
      window.addEventListener('scroll', animateOnScroll);
      animateOnScroll(); // Run once on load
      
      // Fetch GitHub stats
      fetch('https://api.github.com/users/DineshMadhavanM')
        .then(response => response.json())
        .then(data => {
          document.getElementById('github-repos').textContent = data.public_repos || '0';
          document.getElementById('github-followers').textContent = data.followers || '0';
          // Note: GitHub API doesn't provide stars directly, you might need to fetch them separately
        })
        .catch(error => console.error('Error fetching GitHub data:', error));
      
      // Load projects
      loadProjects();
    });
    
    // Sample projects data
    const projects = [
      {
        title: "CareCostPredictor",
        description: "A machine learning model that predicts healthcare costs based on various factors. Built with Python and scikit-learn, this project demonstrates data preprocessing, feature engineering, and model deployment.",
        tags: ["Python", "scikit-learn", "Machine Learning", "Flask", "Data Analysis"],
        image: "https://images.unsplash.com/photo-1505751172876-fa186e26646d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
        link: "https://github.com/DineshMadhavanM/CareCostPredictor"
      },
      {
        title: "Autonomous AI Agent Framework",
        description: "Developed a framework for creating autonomous AI agents capable of goal-oriented behavior and decision-making in dynamic environments.",
        tags: ["Python", "PyTorch", "Reinforcement Learning", "OpenAI API"],
        image: "https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1025&q=80",
        link: "#"
      },
      {
        title: "Data Analysis Dashboard",
        description: "Interactive dashboard for visualizing and analyzing complex datasets with real-time updates.",
        tags: ["Python", "Pandas", "Plotly", "Dash"],
        image: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
        link: "#"
      },
      {
        title: "E-commerce UI/UX Redesign",
        description: "Complete redesign of an e-commerce platform focusing on improving user experience and conversion rates.",
        tags: ["Figma", "UI/UX", "Prototyping"],
        image: "https://images.unsplash.com/photo-1556742049-3aac8520c024?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80",
        link: "#"
      }
    ];
    
    // Load projects into the grid
    function loadProjects() {
      const container = document.getElementById('projects-container');
      
      projects.forEach((project, index) => {
        const projectElement = document.createElement('div');
        projectElement.className = `project-card fade-in delay-${(index % 3) + 1}`;
        projectElement.style.opacity = '0';
        projectElement.style.transform = 'translateY(20px)';
        projectElement.style.transition = `opacity 0.6s ease-out ${0.2 * (index + 1)}s, transform 0.6s ease-out ${0.2 * (index + 1)}s`;
        
        projectElement.innerHTML = `
          <img src="${project.image}" alt="${project.title}" class="project-image">
          <div class="project-content">
            <h3 class="project-title">${project.title}</h3>
            <p class="project-description">${project.description}</p>
            <div class="project-tags">
              ${project.tags.map(tag => `<span class="tag">${tag}</span>`).join('')}
            </div>
            <div class="project-links">
              <a href="${project.link}" class="project-link" target="_blank">
                <i class="fas fa-external-link-alt"></i> View Project
              </a>
              <a href="${project.link}" class="project-link" target="_blank">
                <i class="fab fa-github"></i> Code
              </a>
            </div>
          </div>
        `;
        
        container.appendChild(projectElement);
        
        // Trigger reflow
        void projectElement.offsetWidth;
        
        // Set final state
        setTimeout(() => {
          projectElement.style.opacity = '1';
          projectElement.style.transform = 'translateY(0)';
        }, 100);
      });
    }
  </script>
</body>
</html>
