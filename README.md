<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Athreyo Marfizio - Landing Page</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Reset e estilos básicos */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f5f5;
        }

        h1, h2, h3 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
        }

        .header-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid white;
            object-fit: cover;
        }

        .tagline {
            font-style: italic;
            font-weight: 300;
            margin-top: 0.5rem;
        }

        /* Navegação */
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        nav a {
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: background-color 0.3s;
        }

        nav a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        /* Main content */
        main {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .section-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .section-card h2 {
            margin-bottom: 1.5rem;
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 0.5rem;
            display: inline-block;
        }

        /* Seção Sobre Mim */
        #sobre p {
            text-align: justify;
        }

        /* Seção Habilidades */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .skill-category h3 {
            margin-bottom: 0.5rem;
            color: #3498db;
        }

        .skill-category ul {
            list-style-position: inside;
        }

        .skill-category li {
            margin-bottom: 0.3rem;
        }

        /* Seção Projetos */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .project-card {
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .project-card h3 {
            color: #2c3e50;
            margin-bottom: 0.5rem;
        }

        .project-card p {
            margin-bottom: 1rem;
        }

        .project-link {
            display: inline-block;
            background-color: #3498db;
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: background-color 0.3s;
        }

        .project-link:hover {
            background-color: #2980b9;
        }

        /* Aside */
        .hobbies-list {
            list-style: none;
        }

        .hobbies-list li {
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
            flex-wrap: wrap;
        }

        .social-links a {
            padding: 0.5rem 1rem;
            background-color: #3498db;
            color: white;
            border-radius: 4px;
            transition: background-color 0.3s;
        }

        .social-links a:hover {
            background-color: #2980b9;
        }

        /* Footer */
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 1rem;
        }

        .footer-content {
            max-width: 800px;
            margin: 0 auto;
        }

        footer a {
            color: #3498db;
            transition: color 0.3s;
        }

        footer a:hover {
            color: #2980b9;
        }

        /* Responsividade */
        @media (min-width: 768px) {
            .header-content {
                flex-direction: row;
                justify-content: center;
                text-align: left;
            }
            
            main {
                grid-template-columns: 2fr 1fr;
            }
            
            #sobre, #habilidades, #projetos {
                grid-column: 1;
            }
            
            aside {
                grid-column: 2;
                grid-row: 1 / span 2;
                align-self: start;
            }
        }

        @media (max-width: 480px) {
            nav ul {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            .skills-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <img src="https://imgur.com/moQKEya.jpg" alt="Foto de Athreyo" class="profile-img">
            <div class="header-text">
                <h1>Athreyo Adryann Barbosa Marfizio</h1>
                <p class="tagline">“Construindo soluções com código e criatividade.”
                                        "Nada Acontece Por A Caso."</p>
            </div>
        </div>
        <nav>
            <ul>
                <li><a href="#sobre">Sobre Mim</a></li>
                <li><a href="#habilidades">Habilidades</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="sobre" class="section-card">
            <h2>Sobre Mim</h2>
            <p>Sou apaixonado por tecnologia, estudo desenvolvimento web e estou em busca de desafios que me permitam crescer profissionalmente e sempre buscando aprender coisas novas. Acredito que o conhecimento compartilhado é a melhor forma de evoluir na carreira e na vida. Sou uma pessoa simples, engraçada, comunicativa, extrovertida e legal.</p>
        </section>

        <section id="habilidades" class="section-card">
            <h2>Habilidades</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>Front-end</h3>
                    <ul>
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>JavaScript</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Back-end</h3>
                    <ul>
                        <li>Python</li>
                        <li>Java</li>
                        <li>SQL</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Outros</h3>
                    <ul>
                        <li>Redes de Computadores</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="projetos" class="section-card">
            <h2>Projetos</h2>
            <div class="projects-container">
                <article class="project-card">
                    <h3>Sistema de Gerenciamento de Tarefas</h3>
                    <p>Um aplicativo web desenvolvido com HTML, CSS e JavaScript para organização pessoal e profissional, com recursos de priorização e categorização de tarefas.</p>
                    <a href="file:///C:/Users/Maria-Notebook/Documents/Faculdade%20ATHREYO/index.html?" class="project-link">Ver Projeto</a>
                </article>
                <article class="project-card">
                    <h3>Site de Portfólio Interativo</h3>
                    <p>Landing page responsiva criada com HTML, CSS e JavaScript para apresentação de projetos de desenvolvimento web.</p>
                    <a href="file:///C:/Users/Maria-Notebook/Documents/Faculdade%20ATHREYO/index1.html" class="project-link">Ver Projeto</a>
                </article>
                <article class="project-card">
                    <h3>Jogo da adivinhação</h3>
                    <p>Um pequeno jogo em JavaScript que desafia o usuário a adivinhar um número aleatório entre 1 e 100.</p>
                    <a href="file:///C:/Users/Maria-Notebook/Documents/Faculdade%20ATHREYO/Jogo%20de%20adivinha%C3%A7%C3%A3o.html" class="project-link">Ver Projeto</a>
                </article>
            </div>
        </section>

        <aside class="section-card">
            <h2>Curiosidades</h2>
            <ul class="hobbies-list">
                <li>🎮 Adoro jogos eletrônicos nos momentos livres</li>
                <li>🌱 Estou aprendendo Python por hobby.</li>
                <li>📚 Leio pelo menos um livro por mês</li>
                <li>⚽ Pratico esportes regularmente</li>
            </ul>
            <div class="social-links">
                <a href="https://github.com/athreyomarfizio" target="_blank">GitHub</a>
                <a href="https://linkedin.com/in/athreyo-marfizio" target="_blank">LinkedIn</a>
                <a href="https://www.instagram.com/athreyo/" target="_blank">Instagram</a>
            </div>
        </aside>
    </main>

    <footer id="contato">
        <div class="footer-content">
            <p>Entre em contato: <a href="mailto:athreyoadryan@gmail.com">athreyoadryan@gmail.com</a></p>
            <p>© 2025 Athreyo Marfizio. Todos os direitos reservados.</p>
        </div>
    </footer>
</body>
</html>
