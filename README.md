<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vince Adrian A. Harayo | Interactive Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* 1. Global Reset & Variables */
        :root {
            --primary: #4361ee;
            --primary-dark: #3a56d4;
            --secondary: #7209b7;
            --accent: #f72585;
            --success: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
            --gray: #6c757d;
            --gray-light: #e9ecef;
            --shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 40px rgba(0, 0, 0, 0.15);
            --radius: 16px;
            --radius-sm: 8px;
            --transition: all 0.3s ease;
            --gradient-primary: linear-gradient(135deg, #4361ee, #3a0ca3);
            --gradient-secondary: linear-gradient(135deg, #7209b7, #f72585);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* 2. Layout */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .profile-layout {
            display: grid;
            grid-template-columns: 350px 1fr;
            gap: 30px;
            margin-top: 30px;
        }

        /* 3. Profile Header */
        .profile-header {
            background: white;
            border-radius: var(--radius);
            padding: 40px 30px;
            text-align: center;
            box-shadow: var(--shadow);
            position: sticky;
            top: 30px;
        }

        .profile-avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 25px;
            border: 5px solid white;
            box-shadow: var(--shadow);
            background: var(--gradient-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            overflow: hidden;
        }

        .profile-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .profile-name {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 5px;
            color: var(--dark);
        }

        .profile-title {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 20px;
            font-size: 18px;
        }

        .profile-bio {
            color: var(--gray);
            margin-bottom: 30px;
            line-height: 1.7;
        }

        /* 4. Stats */
        .profile-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }

        .stat-item {
            text-align: center;
            padding: 15px 10px;
            background: var(--gray-light);
            border-radius: var(--radius-sm);
        }

        .stat-number {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 12px;
            color: var(--gray);
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* 5. Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
        }

        .social-link {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: var(--gray-light);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--dark);
            text-decoration: none;
            font-size: 18px;
            transition: var(--transition);
        }

        .social-link:hover {
            transform: translateY(-5px);
            background: var(--primary);
            color: white;
        }

        /* 6. Action Buttons */
        .action-buttons {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .btn {
            padding: 15px 20px;
            border-radius: var(--radius-sm);
            border: none;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .btn-primary {
            background: var(--gradient-primary);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(67, 97, 238, 0.3);
        }

        .btn-secondary {
            background: white;
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-3px);
        }

        /* 7. Main Content */
        .profile-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .content-section {
            background: white;
            border-radius: var(--radius);
            padding: 35px;
            box-shadow: var(--shadow);
            animation: fadeIn 0.5s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--gray-light);
        }

        .section-title {
            font-size: 22px;
            font-weight: 700;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* 8. Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }

        .skill-item {
            background: var(--gray-light);
            padding: 20px;
            border-radius: var(--radius-sm);
            transition: var(--transition);
        }

        .skill-item:hover {
            transform: translateY(-5px);
            background: var(--primary);
            color: white;
        }

        .skill-item:hover .skill-name,
        .skill-item:hover .skill-level {
            color: white;
        }

        .skill-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }

        .skill-name {
            font-weight: 600;
            color: var(--dark);
        }

        .skill-level {
            color: var(--primary);
            font-size: 14px;
            font-weight: 500;
        }

        .skill-bar {
            height: 8px;
            background: rgba(67, 97, 238, 0.1);
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--gradient-primary);
            border-radius: 4px;
            width: 0;
            transition: width 1s ease;
        }

        /* 9. Experience Timeline */
        .timeline {
            position: relative;
            padding-left: 30px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 2px;
            background: var(--gray-light);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            padding-bottom: 30px;
            border-bottom: 1px solid var(--gray-light);
        }

        .timeline-item:last-child {
            border-bottom: none;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -36px;
            top: 5px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--primary);
            border: 3px solid white;
            box-shadow: 0 0 0 3px var(--gray-light);
        }

        .timeline-date {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 5px;
            font-size: 14px;
        }

        .timeline-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .timeline-company {
            color: var(--gray);
            margin-bottom: 10px;
            font-size: 14px;
        }

        /* 10. Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: white;
            border-radius: var(--radius-sm);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid var(--gray-light);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .project-image {
            height: 180px;
            background: var(--gradient-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 40px;
        }

        .project-content {
            padding: 25px;
        }

        .project-title {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--dark);
        }

        .project-description {
            color: var(--gray);
            font-size: 14px;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .project-tag {
            background: var(--gray-light);
            color: var(--gray);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 500;
        }

        /* 11. Contact Form */
        .contact-form {
            display: grid;
            gap: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .form-label {
            font-weight: 600;
            color: var(--dark);
        }

        .form-input, .form-textarea {
            padding: 15px;
            border: 2px solid var(--gray-light);
            border-radius: var(--radius-sm);
            font-family: inherit;
            font-size: 16px;
            transition: var(--transition);
        }

        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.1);
        }

        .form-textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* 12. Response Messages */
        .response-message {
            display: none;
            padding: 20px;
            border-radius: var(--radius-sm);
            margin-top: 20px;
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .response-success {
            background: rgba(76, 201, 240, 0.1);
            border: 2px solid var(--success);
            color: #0a8;
        }

        .response-error {
            background: rgba(247, 37, 133, 0.1);
            border: 2px solid var(--accent);
            color: #d00;
        }

        /* 13. Responsive Design */
        @media (max-width: 992px) {
            .profile-layout {
                grid-template-columns: 1fr;
            }
            
            .profile-header {
                position: static;
            }
            
            .skills-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            .profile-stats {
                grid-template-columns: 1fr;
                gap: 10px;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .content-section {
                padding: 25px;
            }
        }

        @media (max-width: 480px) {
            .profile-avatar {
                width: 120px;
                height: 120px;
                font-size: 40px;
            }
            
            .profile-name {
                font-size: 24px;
            }
            
            .section-header {
                flex-direction: column;
                align-items: flex-start;
                gap: 15px;
            }
        }

        /* 14. Interaction Styles */
        .interaction-buttons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .interaction-btn {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: var(--radius-sm);
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .like-btn {
            background: rgba(247, 37, 133, 0.1);
            color: var(--accent);
        }

        .like-btn:hover, .like-btn.active {
            background: var(--accent);
            color: white;
        }

        .share-btn {
            background: rgba(67, 97, 238, 0.1);
            color: var(--primary);
        }

        .share-btn:hover {
            background: var(--primary);
            color: white;
        }

        .save-btn {
            background: rgba(76, 201, 240, 0.1);
            color: var(--success);
        }

        .save-btn:hover, .save-btn.active {
            background: var(--success);
            color: white;
        }

        /* 15. Loading States */
        .loading {
            opacity: 0.7;
            pointer-events: none;
        }

        .loading::after {
            content: '';
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s ease infinite;
            margin-left: 10px;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Profile Layout -->
        <div class="profile-layout">
            <!-- Left Sidebar - Profile Info -->
            <div class="profile-header">
                <div class="profile-avatar">
                    <img src = "nana.png">
                </div>
                <h1 class="profile-name">Vince Adrian A. Harayo</h1>
                <p class="profile-title">Web Developer & System Designer</p>
                <p class="profile-bio">
                    Pag may tsaga may bisaya. 
                    Boarding House Kaba Pwede Pa Lakat.
                </p>
                
                <!-- Stats -->
                <div class="profile-stats">
                    <div class="stat-item">
                        <div class="754" id="754">425</div>
                        <div class="stat-label">Projects</div>
                    </div>
                    <div class="stat-item">
                        <div class="5" id="242">7</div>
                        <div class="stat-label">Years Exp</div>
                    </div>
                    <div class="stat-item">
                        <div class="34534" id="234">135367</div>
                        <div class="stat-label">Clients</div>
                    </div>
                </div>
                
                <!-- Social Links -->
                <div class="social-links">
                    <a href="#" class="social-link" title="LinkedIn">
                        <i class="fab fa-linkedin-in"></i>
                    </a>
                    <a href="#" class="social-link" title="GitHub">
                        <i class="fab fa-github"></i>
                    </a>
                    <a href="#" class="social-link" title="Twitter">
                        <i class="fab fa-twitter"></i>
                    </a>
                    <a href="#" class="social-link" title="Dribbble">
                        <i class="fab fa-dribbble"></i>
                    </a>
                </div>
                
                <!-- Action Buttons -->
                <div class="action-buttons">
                    <button class="btn btn-primary" onclick="showContactForm()">
                        <i class="fas fa-paper-plane"></i> Contact Me
                    </button>
                    <button class="btn btn-secondary" onclick="downloadResume()">
                        <i class="fas fa-download"></i> Download CV
                    </button>
                </div>
            </div>
            
            <!-- Right Side - Main Content -->
            <div class="profile-content">
                <!-- Skills Section -->
                <section class="content-section" id="skills">
                    <div class="section-header">
                        <h2 class="section-title">
                            <i class="fas fa-code"></i> Skills & Expertise
                        </h2>
                        <div class="interaction-buttons">
                            <button class="interaction-btn like-btn" onclick="toggleLike('skills')">
                                <i class="far fa-heart"></i> Like
                            </button>
                            <button class="interaction-btn share-btn" onclick="shareSection('skills')">
                                <i class="fas fa-share-alt"></i> Share
                            </button>
                        </div>
                    </div>
                    
                    <div class="skills-grid">
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">UI/UX Design</span>
                                <span class="skill-level">Expert</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="95" style="width: 95%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">Figma</span>
                                <span class="skill-level">Advanced</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="90" style="width: 90%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">HTML/CSS</span>
                                <span class="skill-level">Expert</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="98" style="width: 98%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">JavaScript</span>
                                <span class="skill-level">Advanced</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="88" style="width: 88%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">React</span>
                                <span class="skill-level">Advanced</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="85" style="width: 85%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-header">
                                <span class="skill-name">WordPress</span>
                                <span class="skill-level">Intermediate</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" data-width="75" style="width: 75%;"></div>
                            </div>
                        </div>
                    </div>
                </section>
                
                <!-- Experience Section -->
                <section class="content-section" id="experience">
                    <div class="section-header">
                        <h2 class="section-title">
                            <i class="fas fa-briefcase"></i> Work Experience
                        </h2>
                        <div class="interaction-buttons">
                            <button class="interaction-btn save-btn" onclick="toggleSave('experience')">
                                <i class="far fa-bookmark"></i> Save
                            </button>
                        </div>
                    </div>
                    
                    <div class="timeline">
                        <div class="timeline-item">
                            <div class="timeline-date">2026 - Present</div>
                            <h3 class="timeline-title">Senior UX Designer</h3>
                            <div class="timeline-company">TechVision Inc.</div>
                            <p>Leading design team for enterprise SaaS products. Improved user satisfaction by 40% through user research and iterative design.</p>
                        </div>
                        <div class="timeline-item">
                            <div class="timeline-date">2023- 2024</div>
                            <h3 class="timeline-title">UI/UX Designer</h3>
                            <div class="timeline-company">CreativeMinds Agency</div>
                            <p>Designed mobile and web applications for various clients including startups and established companies.</p>
                        </div>
                        <div class="timeline-item">
                            <div class="timeline-date">2021 - 2022</div>
                            <h3 class="timeline-title">Frontend Developer</h3>
                            <div class="timeline-company">WebSolutions LLC</div>
                            <p>Built responsive websites and web applications using modern frontend technologies.</p>
                        </div>
                    </div>
                </section>
                
                <!-- Projects Section -->
                <section class="content-section" id="projects">
                    <div class="section-header">
                        <h2 class="section-title">
                            <i class="fas fa-project-diagram"></i> Featured Projects
                        </h2>
                        <div class="interaction-buttons">
                            <button class="interaction-btn like-btn" onclick="toggleLike('projects')">
                                <i class="far fa-heart"></i> Like
                            </button>
                        </div>
                    </div>
                    
                    <div class="projects-grid">
                        <div class="project-card">
                            <div class="project-image">
                                <i class="fas fa-mobile-alt"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">Fintech Mobile App</h3>
                                <p class="project-description">
                                    A mobile banking app with intuitive UI and advanced security features.
                                </p>
                                <div class="project-tags">
                                    <span class="project-tag">Figma</span>
                                    <span class="project-tag">React Native</span>
                                    <span class="project-tag">UI Design</span>
                                </div>
                                <button class="btn btn-secondary" onclick="viewProject(1)">
                                    View Details
                                </button>
                            </div>
                        </div>
                        
                        <div class="project-card">
                            <div class="project-image">
                                <i class="fas fa-chart-line"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">Analytics Dashboard</h3>
                                <p class="project-description">
                                    Real-time data visualization dashboard for business intelligence.
                                </p>
                                <div class="project-tags">
                                    <span class="project-tag">React</span>
                                    <span class="project-tag">D3.js</span>
                                    <span class="project-tag">UI/UX</span>
                                </div>
                                <button class="btn btn-secondary" onclick="viewProject(2)">
                                    View Details
                                </button>
                            </div>
                        </div>
                        
                        <div class="project-card">
                            <div class="project-image">
                                <i class="fas fa-shopping-cart"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">E-commerce Platform</h3>
                                <p class="project-description">
                                    Full-featured online shopping platform with personalized recommendations.
                                </p>
                                <div class="project-tags">
                                    <span class="project-tag">Vue.js</span>
                                    <span class="project-tag">Node.js</span>
                                    <span class="project-tag">UX Research</span>
                                </div>
                                <button class="btn btn-secondary" onclick="viewProject(3)">
                                    View Details
                                </button>
                            </div>
                        </div>
                    </div>
                </section>
                
                <!-- Contact Form Section -->
                <section class="content-section" id="contact" style="display: none;">
                    <div class="section-header">
                        <h2 class="section-title">
                            <i class="fas fa-envelope"></i> Get In Touch
                        </h2>
                        <button class="btn btn-secondary" onclick="hideContactForm()">
                            <i class="fas fa-times"></i> Close
                        </button>
                    </div>
                    
                    <form class="contact-form" onsubmit="submitContactForm(event)">
                        <div class="form-group">
                            <label class="form-label">Your Name</label>
                            <input type="text" class="form-input" placeholder="Enter your name" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">Email Address</label>
                            <input type="email" class="form-input" placeholder="Enter your email" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">Subject</label>
                            <input type="text" class="form-input" placeholder="What is this regarding?" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">Message</label>
                            <textarea class="form-textarea" placeholder="Type your message here..." required></textarea>
                        </div>
                        
                        <button type="submit" class="btn btn-primary">
                            <i class="fas fa-paper-plane"></i> Send Message
                        </button>
                        
                        <div class="response-message" id="responseMessage"></div>
                    </form>
                </section>
            </div>
        </div>
    </div>

    <script>
        // Profile Interaction System
        let profileData = {
            likes: { skills: false, projects: false },
            saved: { experience: false },
            stats: { projects: 42, experience: 8, clients: 127 }
        };

        // Show/Hide Contact Form
        function showContactForm() {
            document.getElementById('contact').style.display = 'block';
            document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
        }

        function hideContactForm() {
            document.getElementById('contact').style.display = 'none';
        }

        // Toggle Like
        function toggleLike(section) {
            const btn = document.querySelector(`#${section} .like-btn`);
            const icon = btn.querySelector('i');
            
            profileData.likes[section] = !profileData.likes[section];
            
            if (profileData.likes[section]) {
                btn.classList.add('active');
                icon.classList.remove('far', 'fa-heart');
                icon.classList.add('fas', 'fa-heart');
                
                // Show notification
                showNotification('liked', section);
            } else {
                btn.classList.remove('active');
                icon.classList.remove('fas', 'fa-heart');
                icon.classList.add('far', 'fa-heart');
            }
        }

        // Toggle Save
        function toggleSave(section) {
            const btn = document.querySelector(`#${section} .save-btn`);
            const icon = btn.querySelector('i');
            
            profileData.saved[section] = !profileData.saved[section];
            
            if (profileData.saved[section]) {
                btn.classList.add('active');
                icon.classList.remove('far', 'fa-bookmark');
                icon.classList.add('fas', 'fa-bookmark');
                
                // Show notification
                showNotification('saved', section);
            } else {
                btn.classList.remove('active');
                icon.classList.remove('fas', 'fa-bookmark');
                icon.classList.add('far', 'fa-bookmark');
            }
        }

        // Share Section
        function shareSection(section) {
            const sectionTitle = document.querySelector(`#${section} .section-title`).textContent;
            const url = `${window.location.origin}#${section}`;
            
            if (navigator.share) {
                navigator.share({
                    title: `Check out my ${sectionTitle}`,
                    text: `View my ${sectionTitle} on my profile`,
                    url: url
                });
            } else {
                // Fallback for browsers that don't support Web Share API
                navigator.clipboard.writeText(url);
                showNotification('shared', section);
            }
        }

        // Download Resume
        function downloadResume() {
            const btn = document.querySelector('.btn-secondary');
            const originalText = btn.innerHTML;
            
            btn.innerHTML = '<i class="fas fa-spinner loading"></i> Preparing...';
            btn.classList.add('loading');
            
            setTimeout(() => {
                btn.innerHTML = originalText;
                btn.classList.remove('loading');
                
                // Show success message
                const message = document.createElement('div');
                message.className = 'response-message response-success';
                message.innerHTML = '<i class="fas fa-check-circle"></i> Your resume has been downloaded successfully!';
                btn.parentElement.appendChild(message);
                
                setTimeout(() => message.remove(), 3000);
            }, 1500);
        }

        // View Project Details
        function viewProject(projectId) {
            const projects = [
                { id: 1, title: 'Fintech Mobile App', description: 'Complete mobile banking solution with biometric authentication and real-time notifications.' },
                { id: 2, title: 'Analytics Dashboard', description: 'Interactive data visualization tool with custom reports and export functionality.' },
                { id: 3, title: 'E-commerce Platform', description: 'Scalable online shopping platform with AI-powered recommendations and secure payments.' }
            ];
            
            const project = projects.find(p => p.id === projectId);
            
            // Create modal-like notification
            const notification = document.createElement('div');
            notification.className = 'response-message response-success';
            notification.innerHTML = `
                <h3 style="margin-bottom: 10px;">${project.title}</h3>
                <p>${project.description}</p>
                <p style="margin-top: 10px; font-size: 14px; color: #666;">
                    <i class="fas fa-info-circle"></i> This is a demo project view.
                </p>
            `;
            
            document.querySelector('#projects').appendChild(notification);
            
            setTimeout(() => notification.remove(), 5000);
        }

        // Submit Contact Form
        function submitContactForm(event) {
            event.preventDefault();
            
            const form = event.target;
            const submitBtn = form.querySelector('button[type="submit"]');
            const originalText = submitBtn.innerHTML;
            
            // Show loading state
            submitBtn.innerHTML = '<i class="fas fa-spinner loading"></i> Sending...';
            submitBtn.disabled = true;
            
            // Simulate API call
            setTimeout(() => {
                // Reset button
                submitBtn.innerHTML = originalText;
                submitBtn.disabled = false;
                
                // Show success message
                const responseMessage = document.getElementById('responseMessage');
                responseMessage.className = 'response-message response-success';
                responseMessage.innerHTML = `
                    <i class="fas fa-check-circle"></i>
                    <strong>Message Sent Successfully!</strong><br>
                    Thank you for your message. I'll get back to you within 24 hours.
                `;
                responseMessage.style.display = 'block';
                
                // Reset form
                form.reset();
                
                // Hide message after 5 seconds
                setTimeout(() => {
                    responseMessage.style.display = 'none';
                }, 5000);
            }, 2000);
        }

        // Show Notification
        function showNotification(type, section) {
            const messages = {
                liked: `You liked the ${section} section!`,
                saved: `You saved the ${section} section!`,
                shared: `Link to ${section} copied to clipboard!`
            };
            
            const notification = document.createElement('div');
            notification.className = 'response-message response-success';
            notification.style.position = 'fixed';
            notification.style.top = '20px';
            notification.style.right = '20px';
            notification.style.zIndex = '1000';
            notification.style.maxWidth = '300px';
            notification.innerHTML = `<i class="fas fa-check"></i> ${messages[type]}`;
            
            document.body.appendChild(notification);
            
            setTimeout(() => {
                notification.style.animation = 'slideIn 0.5s ease reverse';
                setTimeout(() => notification.remove(), 500);
            }, 3000);
        }

        // Animate Stats Counters
        function animateStats() {
            const statElements = {
                projectCount: document.getElementById('projectCount'),
                experienceYears: document.getElementById('experienceYears'),
                clientCount: document.getElementById('clientCount')
            };
            
            Object.keys(statElements).forEach((key, index) => {
                const element = statElements[key];
                const target = profileData.stats[key];
                let current = 0;
                
                const timer = setInterval(() => {
                    current += Math.ceil(target / 50);
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    element.textContent = current;
                }, 30 * (index + 1));
            });
        }

        // Animate Skill Bars on Scroll
        function animateSkillBars() {
            const skillBars = document.querySelectorAll('.skill-progress');
            
            skillBars.forEach(bar => {
                const width = bar.getAttribute('data-width');
                bar.style.width = '0%';
                
                setTimeout(() => {
                    bar.style.width = width + '%';
                }, 100);
            });
        }

        // Initialize on page load
        document.addEventListener('DOMContentLoaded', function() {
            animateStats();
            animateSkillBars();
            
            // Add scroll animation for sections
            const sections = document.querySelectorAll('.content-section');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'fadeIn 0.5s ease-out';
                    }
                });
            }, { threshold: 0.1 });
            
            sections.forEach(section => observer.observe(section));
            
            // Add click effects to all buttons
            document.querySelectorAll('button').forEach(button => {
                button.addEventListener('click', function(e) {
                    // Add ripple effect
                    const ripple = document.createElement('span');
                    const rect = this.getBoundingClientRect();
                    const size = Math.max(rect.width, rect.height);
                    const x = e.clientX - rect.left - size / 2;
                    const y = e.clientY - rect.top - size / 2;
                    
                    ripple.style.cssText = `
                        position: absolute;
                        border-radius: 50%;
                        background: rgba(255, 255, 255, 0.6);
                        transform: scale(0);
                        animation: ripple 0.6s linear;
                        width: ${size}px;
                        height: ${size}px;
                        top: ${y}px;
                        left: ${x}px;
                    `;
                    
                    this.appendChild(ripple);
                    
                    setTimeout(() => ripple.remove(), 600);
                });
            });
            
            // Add ripple animation
            const style = document.createElement('style');
            style.textContent = `
                @keyframes ripple {
                    to {
                        transform: scale(4);
                        opacity: 0;
                    }
                }
            `;
            document.head.appendChild(style);
        });
    </script>
</body>
</html>
