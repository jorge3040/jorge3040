<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jorge Rosell | Desarrollador de Software</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2b2d42;
            --secondary: #8d99ae;
            --accent: #ef233c;
            --light: #edf2f4;
            --dark: #1a1a2e;
            --gradient: linear-gradient(135deg, #2b2d42 0%, #1a1a2e 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--primary);
            line-height: 1.6;
        }
        
        .profile-container {
            max-width: 800px;
            margin: 2rem auto;
            padding: 2rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .profile-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 10px;
            background: var(--gradient);
        }
        
        .header {
            text-align: center;
            margin-bottom: 2rem;
            position: relative;
        }
        
        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 1rem;
            transition: transform 0.3s ease;
        }
        
        .profile-pic:hover {
            transform: scale(1.05);
        }
        
        h1 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-size: 2.2rem;
        }
        
        .title {
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .divider {
            width: 100px;
            height: 3px;
            background: var(--gradient);
            margin: 1rem auto;
            border-radius: 3px;
        }
        
        .about {
            margin-bottom: 2rem;
            text-align: center;
        }
        
        .about p {
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        .skills {
            margin-bottom: 2rem;
        }
        
        .section-title {
            color: var(--primary);
            margin-bottom: 1rem;
            text-align: center;
            font-size: 1.5rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 3px;
            background: var(--accent);
            border-radius: 3px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .skill-item {
            background: white;
            padding: 1rem;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .skill-icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--gradient);
            color: white;
            font-size: 1.5rem;
            transition: transform 0.3s ease, background 0.3s ease;
            text-decoration: none;
        }
        
        .social-link:hover {
            transform: scale(1.1) translateY(-3px);
            background: var(--accent);
        }
        
        .projects-btn {
            display: block;
            width: 200px;
            margin: 2rem auto;
            padding: 0.8rem 1.5rem;
            background: var(--gradient);
            color: white;
            text-align: center;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 5px 15px rgba(43, 45, 66, 0.3);
        }
        
        .projects-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(43, 45, 66, 0.4);
            background: var(--accent);
        }
        
        footer {
            text-align: center;
            margin-top: 2rem;
            color: var(--secondary);
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .profile-container {
                margin: 1rem;
                padding: 1.5rem;
            }
            
            .skills-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
        }
        
        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animated {
            animation: fadeIn 0.8s ease forwards;
        }
        
        .delay-1 { animation-delay: 0.2s; }
        .delay-2 { animation-delay: 0.4s; }
        .delay-3 { animation-delay: 0.6s; }
    </style>
</head>
<body>
    <div class="profile-container">
        <header class="header animated">
            <!-- Reemplaza con tu imagen de perfil -->
            <img src="https://via.placeholder.com/150" alt="Jorge Rosell" class="profile-pic">
            <h1>Jorge Rosell</h1>
            <div class="title">Desarrollador de Software | Diseñador Web</div>
            <div class="divider"></div>
        </header>
        
        <section class="about animated delay-1">
            <p>
                Soy <strong>Técnico Superior en Informática</strong> graduado en el Instituto Universitario de Tecnología 
                "Juan Pablo Pérez Alfonso" (IUTEPAL) en Maracay, estado Aragua, Venezuela. 
                Apasionado por la creación de soluciones tecnológicas innovadoras y el desarrollo de software de calidad.
            </p>
            <p>
                En esta plataforma busco <strong>nuevas oportunidades profesionales</strong> donde pueda aplicar mis 
                conocimientos y seguir creciendo como desarrollador. Ofrezco servicios de <strong>programación, 
                diseño de software y desarrollo web</strong>, con un enfoque en crear productos funcionales, 
                escalables y centrados en el usuario.
            </p>
            <p>
                Si deseas conocer más sobre mis proyectos y trabajos, te invito a seguirme en mis redes sociales 
                donde comparto mis últimos desarrollos y aprendizajes en el mundo de la tecnología.
            </p>
        </section>
        
        <section class="skills animated delay-2">
            <h2 class="section-title">Habilidades Técnicas</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-html5"></i></div>
                    <div>HTML5</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-css3-alt"></i></div>
                    <div>CSS3</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-js"></i></div>
                    <div>JavaScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-react"></i></div>
                    <div>React</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-node-js"></i></div>
                    <div>Node.js</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <div>Bases de Datos</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-git-alt"></i></div>
                    <div>Git</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-mobile-alt"></i></div>
                    <div>Responsive Design</div>
                </div>
            </div>
        </section>
        
        <div class="social-links animated delay-3">
            <!-- Reemplaza con tus enlaces reales -->
            <a href="https://github.com/tuusuario" class="social-link" target="_blank" title="GitHub">
                <i class="fab fa-github"></i>
            </a>
            <a href="https://linkedin.com/in/tuperfil" class="social-link" target="_blank" title="LinkedIn">
                <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="https://twitter.com/tuusuario" class="social-link" target="_blank" title="Twitter">
                <i class="fab fa-twitter"></i>
            </a>
            <a href="https://facebook.com/tuperfil" class="social-link" target="_blank" title="Facebook">
                <i class="fab fa-facebook-f"></i>
            </a>
            <a href="https://instagram.com/tuusuario" class="social-link" target="_blank" title="Instagram">
                <i class="fab fa-instagram"></i>
            </a>
        </div>
        
        <a href="#projects" class="projects-btn animated delay-3">
            Ver Mis Proyectos <i class="fas fa-arrow-right"></i>
        </a>
        
        <footer class="animated delay-3">
            © 2023 Jorge Rosell. Todos los derechos reservados.
        </footer>
    </div>
</body>
</html>