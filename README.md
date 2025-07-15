<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Basic HTML5 setup -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Personal Website</title> <!-- UPDATE: Change this to your actual name -->
    <style>
        /* CSS Reset - Remove default browser styling */
        /* CSS Reset - Remove default browser styling */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Main body styling */
        body {
            font-family: 'Georgia', serif; /* Professional serif font */
            line-height: 1.6;
            color: #333;
            background-color: #fafafa; /* Light gray background */
        }

        /* Container for all content - centers everything */
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Navigation bar styling */
        nav {
            background-color: #fff;
            padding: 1rem 0;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1); /* Subtle shadow */
            position: sticky; /* Stays at top when scrolling */
            top: 0;
            z-index: 100; /* Ensures nav stays above other content */
        }

        /* Navigation menu layout */
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap; /* Wraps on smaller screens */
            gap: 2rem;
        }

        /* Navigation link styling */
        nav a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: background-color 0.3s; /* Smooth hover effect */
        }

        /* Navigation link hover and active states */
        nav a:hover, nav a.active {
            background-color: #f0f0f0;
        }

        /* Main content sections - hidden by default */
        .section {
            display: none;
            padding: 2rem 0;
        }

        /* Active section is visible */
        .section.active {
            display: block;
        }

        /* Main heading (your name) */
        h1 {
            color: #2c3e50;
            margin-bottom: 1rem;
            font-size: 2.5rem;
            text-align: center;
        }

        /* Section headings */
        h2 {
            color: #34495e;
            margin-bottom: 1.5rem;
            font-size: 2rem;
            border-bottom: 2px solid #ecf0f1; /* Underline effect */
            padding-bottom: 0.5rem;
        }

        /* Sub-section headings */
        h3 {
            color: #2c3e50;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        /* Bio section styling */
        .bio {
            text-align: center;
            font-size: 1.1rem;
            margin-bottom: 2rem;
            color: #555;
        }

        /* Interest tags container */
        .interests {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }

        /* Individual interest tag styling */
        .interest-tag {
            background-color: #3498db; /* Blue background */
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 20px; /* Rounded pill shape */
            font-size: 0.9rem;
        }

        /* Experience section container */
        .experience-section {
            margin-bottom: 2rem;
        }

        /* Individual experience item styling */
        .experience-item {
            background-color: #fff;
            padding: 1.5rem;
            margin-bottom: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1); /* Subtle shadow */
        }

        /* Experience item headings */
        .experience-item h4 {
            color: #2c3e50;
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        /* Job role/title styling */
        .experience-item .role {
            color: #7f8c8d;
            font-style: italic;
            margin-bottom: 0.5rem;
        }

        /* Date range styling */
        .experience-item .date {
            color: #95a5a6;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        /* Skills grid layout */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Responsive grid */
            gap: 1.5rem;
            margin-top: 1rem;
        }

        /* Individual skill category styling */
        .skill-category {
            background-color: #fff;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        /* Skill category headings */
        .skill-category h4 {
            color: #2c3e50;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        /* Skill list styling */
        .skill-list {
            list-style: none;
        }

        /* Individual skill items */
        .skill-list li {
            padding: 0.3rem 0;
            color: #555;
        }

        /* Custom bullet points for skills */
        .skill-list li:before {
            content: "▸ ";
            color: #3498db;
            font-weight: bold;
        }

        /* Writing and project item styling */
        .writing-item, .project-item {
            background-color: #fff;
            padding: 1.5rem;
            margin-bottom: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        /* Writing and project headings */
        .writing-item h4, .project-item h4 {
            color: #2c3e50;
            margin-bottom: 0.5rem;
        }

        /* Link styling in writing and projects */
        .writing-item a, .project-item a {
            color: #3498db;
            text-decoration: none;
        }

        /* Link hover effects */
        .writing-item a:hover, .project-item a:hover {
            text-decoration: underline;
        }

        /* Favorites section highlighting */
        .favorites {
            border-left: 4px solid #f39c12; /* Orange left border */
            padding-left: 1rem;
            margin-bottom: 2rem;
        }

        /* Contact information container */
        .contact-info {
            background-color: #fff;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            text-align: center;
        }

        /* Contact section heading */
        .contact-info h3 {
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        /* Contact info paragraphs */
        .contact-info p {
            margin-bottom: 0.5rem;
            color: #555;
        }

        /* Contact links */
        .contact-info a {
            color: #3498db;
            text-decoration: none;
        }

        /* Contact link hover effects */
        .contact-info a:hover {
            text-decoration: underline;
        }

        /* Mobile responsive design */
        @media (max-width: 600px) {
            /* Stack navigation vertically on mobile */
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            /* Smaller main heading on mobile */
            h1 {
                font-size: 2rem;
            }
            
            /* Center interests on mobile */
            .interests {
                justify-content: center;
            }
            
            /* Single column skills grid on mobile */
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation bar - sticky at top -->
    <nav>
        <div class="container">
            <ul>
                <!-- Navigation links - each calls showSection() to switch content -->
                <li><a href="#" onclick="showSection('home')" class="nav-link active">Home</a></li>
                <li><a href="#" onclick="showSection('experience')" class="nav-link">Experience</a></li>
                <li><a href="#" onclick="showSection('skills')" class="nav-link">Skills</a></li>
                <li><a href="#" onclick="showSection('writing')" class="nav-link">Writing</a></li>
                <li><a href="#" onclick="showSection('projects')" class="nav-link">Projects</a></li>
                <li><a href="#" onclick="showSection('contact')" class="nav-link">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Main content container -->
    <div class="container">
        <!-- HOME SECTION - Active by default -->
        <section id="home" class="section active">
            <h1>Your Name</h1> <!-- UPDATE: Replace with your actual name -->
            <div class="bio">
                <!-- UPDATE: Replace with your personal bio -->
                <p>Brief bio goes here. Write a few sentences about who you are, what you do, and what drives you. Keep it engaging and personal while maintaining a professional tone.</p>
            </div>
            <h3>Interests</h3>
            <div class="interests">
                <!-- UPDATE: Customize these interest tags with your own interests -->
                <span class="interest-tag">Public Policy</span>
                <span class="interest-tag">Data Science</span>
                <span class="interest-tag">Writing</span>
                <span class="interest-tag">Technology</span>
                <span class="interest-tag">Research</span>
                <span class="interest-tag">Community Service</span>
            </div>
        </section>

        <!-- EXPERIENCE SECTION -->
        <section id="experience" class="section">
            <h2>Past Experiences</h2>
            
            <!-- Professional Work Experience -->
            <div class="experience-section">
                <h3>Professional Experience</h3>
                <!-- UPDATE: Replace with your actual work experience -->
                <div class="experience-item">
                    <h4>Organization Name</h4> <!-- Company/Organization -->
                    <div class="role">Job Title</div> <!-- Your position -->
                    <div class="date">Month Year - Month Year</div> <!-- Employment period -->
                    <p>Brief description of your role and key accomplishments. Focus on impact and relevant skills developed.</p>
                </div>
                <!-- Add more experience items as needed -->
                <div class="experience-item">
                    <h4>Organization Name</h4>
                    <div class="role">Job Title</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Brief description of your role and key accomplishments. Focus on impact and relevant skills developed.</p>
                </div>
            </div>

            <!-- Fellowship Experience -->
            <div class="experience-section">
                <h3>Fellowships</h3>
                <!-- UPDATE: Replace with your actual fellowships -->
                <div class="experience-item">
                    <h4>Fellowship Name</h4>
                    <div class="role">Fellow</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of the fellowship program and your contributions or projects completed.</p>
                </div>
                <div class="experience-item">
                    <h4>Fellowship Name</h4>
                    <div class="role">Fellow</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of the fellowship program and your contributions or projects completed.</p>
                </div>
            </div>

            <!-- Volunteer and Club Experience -->
            <div class="experience-section">
                <h3>Volunteering & Clubs</h3>
                <!-- UPDATE: Replace with your actual volunteer work and club involvement -->
                <div class="experience-item">
                    <h4>Organization Name</h4>
                    <div class="role">Volunteer Role</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of your volunteer work and the impact you made.</p>
                </div>
                <div class="experience-item">
                    <h4>Club/Organization Name</h4>
                    <div class="role">Leadership Role</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of your involvement and leadership contributions.</p>
                </div>
            </div>
        </section>

        <!-- SKILLS SECTION -->
        <section id="skills" class="section">
            <h2>Skills</h2>
            <div class="skills-grid">
                <!-- Programming Skills -->
                <div class="skill-category">
                    <h4>Programming Languages</h4>
                    <ul class="skill-list">
                        <!-- UPDATE: Replace with your actual programming languages -->
                        <li>Python</li>
                        <li>R</li>
                        <li>JavaScript</li>
                        <li>SQL</li>
                        <li>HTML/CSS</li>
                        <li>Java</li>
                    </ul>
                </div>
                
                <!-- Writing Skills -->
                <div class="skill-category">
                    <h4>Writing</h4>
                    <ul class="skill-list">
                        <!-- UPDATE: Replace with your actual writing skills -->
                        <li>Policy Analysis</li>
                        <li>Research Papers</li>
                        <li>Technical Documentation</li>
                        <li>Grant Writing</li>
                        <li>Blog Writing</li>
                        <li>Content Strategy</li>
                    </ul>
                </div>
                
                <!-- Data Science Skills -->
                <div class="skill-category">
                    <h4>Data Science</h4>
                    <ul class="skill-list">
                        <!-- UPDATE: Replace with your actual data science skills -->
                        <li>Statistical Analysis</li>
                        <li>Machine Learning</li>
                        <li>Data Visualization</li>
                        <li>Pandas & NumPy</li>
                        <li>Tableau</li>
                        <li>A/B Testing</li>
                    </ul>
                </div>
                
                <!-- Public Policy Skills -->
                <div class="skill-category">
                    <h4>Public Policy</h4>
                    <ul class="skill-list">
                        <!-- UPDATE: Replace with your actual policy skills -->
                        <li>Policy Research</li>
                        <li>Stakeholder Engagement</li>
                        <li>Legislative Analysis</li>
                        <li>Program Evaluation</li>
                        <li>Community Organizing</li>
                        <li>Advocacy</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- WRITING SECTION -->
        <section id="writing" class="section">
            <h2>Writing</h2>
            
            <!-- Personal Favorites - highlighted section -->
            <div class="favorites">
                <h3>Personal Favorites</h3>
                <!-- UPDATE: Replace with your actual favorite pieces -->
                <div class="writing-item">
                    <h4><a href="#" target="_blank">Title of Favorite Piece</a></h4> <!-- UPDATE: Add actual link -->
                    <p>Brief description of this piece and why it's meaningful to you. Published in [Publication/Platform].</p>
                </div>
                <div class="writing-item">
                    <h4><a href="#" target="_blank">Title of Favorite Piece</a></h4>
                    <p>Brief description of this piece and why it's meaningful to you. Published in [Publication/Platform].</p>
                </div>
            </div>

            <!-- All Writing Pieces -->
            <h3>All Writing</h3>
            <!-- UPDATE: Replace with your actual writing pieces -->
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4> <!-- UPDATE: Add actual link -->
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4>
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4>
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
        </section>

        <!-- PROJECTS SECTION -->
        <section id="projects" class="section">
            <h2>Projects</h2>
            
            <!-- Project 1: Pathways to Policy -->
            <div class="project-item">
                <h4><a href="#" target="_blank">Pathways to Policy</a></h4> <!-- UPDATE: Add actual link -->
                <!-- UPDATE: Replace with actual project description -->
                <p>Detailed description of your Pathways to Policy project. What it is, your role, the impact, and key outcomes. Include any relevant metrics or achievements.</p>
            </div>
            
            <!-- Project 2: Paragon Policy Fellowship Work -->
            <div class="project-item">
                <h4><a href="#" target="_blank">Paragon Policy Fellowship Work</a></h4> <!-- UPDATE: Add actual link -->
                <!-- UPDATE: Replace with actual project description -->
                <p>Description of your work during the Paragon Policy Fellowship. Highlight specific projects, research, or policy recommendations you developed.</p>
            </div>
            
            <!-- Project 3: GitHub Portfolio -->
            <div class="project-item">
                <h4><a href="#" target="_blank">GitHub Portfolio</a></h4> <!-- UPDATE: Add actual link -->
                <!-- UPDATE: Replace with actual project description -->
                <p>Overview of your coding projects and contributions. Link to your GitHub profile and highlight your most impressive repositories or contributions to open source projects.</p>
            </div>
        </section>

        <!-- CONTACT SECTION -->
        <section id="contact" class="section">
            <h2>Contact Me!</h2>
            <div class="contact-info">
                <h3>Get In Touch</h3>
                <p>I'd love to hear from you! Feel free to reach out for collaboration opportunities, questions, or just to say hello.</p>
                <!-- UPDATE: Replace with your actual contact information -->
                <p><strong>Email:</strong> <a href="mailto:your.email@example.com">your.email@example.com</a></p>
                <p><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/yourprofile" target="_blank">linkedin.com/in/yourprofile</a></p>
                <p><strong>GitHub:</strong> <a href="https://github.com/zev-vz" target="_blank">github.com/zev-vz</a></p>
                <p><strong>Twitter:</strong> <a href="https://twitter.com/yourusername" target="_blank">@yourusername</a></p>
            </div>
        </section>
    </div>

    <!-- JavaScript for navigation functionality -->
    <script>
        // Function to switch between different sections
        function showSection(sectionId) {
            // Hide all sections by removing 'active' class
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });
            
            // Show the selected section by adding 'active' class
            document.getElementById(sectionId).classList.add('active');
            
            // Update navigation styling - remove active from all links
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                link.classList.remove('active');
            });
            
            // Add active class to the clicked navigation link
            event.target.classList.add('active');
            
            // Scroll to top of page when switching sections
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html></div>
            </div>

            <div class="experience-section">
                <h3>Volunteering & Clubs</h3>
                <div class="experience-item">
                    <h4>Organization Name</h4>
                    <div class="role">Volunteer Role</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of your volunteer work and the impact you made.</p>
                </div>
                <div class="experience-item">
                    <h4>Club/Organization Name</h4>
                    <div class="role">Leadership Role</div>
                    <div class="date">Month Year - Month Year</div>
                    <p>Description of your involvement and leadership contributions.</p>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills" class="section">
            <h2>Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h4>Programming Languages</h4>
                    <ul class="skill-list">
                        <li>Python</li>
                        <li>R</li>
                        <li>JavaScript</li>
                        <li>SQL</li>
                        <li>HTML/CSS</li>
                        <li>Java</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h4>Writing</h4>
                    <ul class="skill-list">
                        <li>Policy Analysis</li>
                        <li>Research Papers</li>
                        <li>Technical Documentation</li>
                        <li>Grant Writing</li>
                        <li>Blog Writing</li>
                        <li>Content Strategy</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h4>Data Science</h4>
                    <ul class="skill-list">
                        <li>Statistical Analysis</li>
                        <li>Machine Learning</li>
                        <li>Data Visualization</li>
                        <li>Pandas & NumPy</li>
                        <li>Tableau</li>
                        <li>A/B Testing</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h4>Public Policy</h4>
                    <ul class="skill-list">
                        <li>Policy Research</li>
                        <li>Stakeholder Engagement</li>
                        <li>Legislative Analysis</li>
                        <li>Program Evaluation</li>
                        <li>Community Organizing</li>
                        <li>Advocacy</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Writing Section -->
        <section id="writing" class="section">
            <h2>Writing</h2>
            
            <div class="favorites">
                <h3>Personal Favorites</h3>
                <div class="writing-item">
                    <h4><a href="#" target="_blank">Title of Favorite Piece</a></h4>
                    <p>Brief description of this piece and why it's meaningful to you. Published in [Publication/Platform].</p>
                </div>
                <div class="writing-item">
                    <h4><a href="#" target="_blank">Title of Favorite Piece</a></h4>
                    <p>Brief description of this piece and why it's meaningful to you. Published in [Publication/Platform].</p>
                </div>
            </div>

            <h3>All Writing</h3>
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4>
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4>
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
            <div class="writing-item">
                <h4><a href="#" target="_blank">Article Title</a></h4>
                <p>Brief description of the article. Published in [Publication/Platform], [Date].</p>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="section">
            <h2>Projects</h2>
            
            <div class="project-item">
                <h4><a href="#" target="_blank">Pathways to Policy</a></h4>
                <p>Detailed description of your Pathways to Policy project. What it is, your role, the impact, and key outcomes. Include any relevant metrics or achievements.</p>
            </div>
            
            <div class="project-item">
                <h4><a href="#" target="_blank">Paragon Policy Fellowship Work</a></h4>
                <p>Description of your work during the Paragon Policy Fellowship. Highlight specific projects, research, or policy recommendations you developed.</p>
            </div>
            
            <div class="project-item">
                <h4><a href="#" target="_blank">GitHub Portfolio</a></h4>
                <p>Overview of your coding projects and contributions. Link to your GitHub profile and highlight your most impressive repositories or contributions to open source projects.</p>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="section">
            <h2>Contact Me!</h2>
            <div class="contact-info">
                <h3>Get In Touch</h3>
                <p>I'd love to hear from you! Feel free to reach out for collaboration opportunities, questions, or just to say hello.</p>
                <p><strong>Email:</strong> <a href="mailto:your.email@example.com">your.email@example.com</a></p>
                <p><strong>LinkedIn:</strong> <a href="https://linkedin.com/in/yourprofile" target="_blank">linkedin.com/in/yourprofile</a></p>
                <p><strong>GitHub:</strong> <a href="https://github.com/zev-vz" target="_blank">github.com/zev-vz</a></p>
                <p><strong>Twitter:</strong> <a href="https://twitter.com/yourusername" target="_blank">@yourusername</a></p>
            </div>
        </section>
    </div>

    <script>
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById(sectionId).classList.add('active');
            
            // Update navigation
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                link.classList.remove('active');
            });
            event.target.classList.add('active');
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
