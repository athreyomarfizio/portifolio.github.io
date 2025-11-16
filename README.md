/* =========================================================
   PORTFÓLIO - ESTILO BASE OTIMIZADO (Versão Profissional)
   Autor: [Seu Nome]
   ========================================================= */

/* =========================
   RESET & VARIÁVEIS GLOBAIS
   ========================= */
:root {
    --font-base: 'Roboto', sans-serif;
    --font-heading: 'Poppins', sans-serif;

    --color-primary: #3498db;
    --color-primary-dark: #2980b9;
    --color-dark: #2c3e50;
    --color-light: #f5f5f5;
    --color-text: #333;
    --color-white: #fff;

    --radius-sm: 4px;
    --radius-md: 8px;

    --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1);
    --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 10px 20px rgba(0, 0, 0, 0.1);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: var(--font-base);
    line-height: 1.6;
    color: var(--color-text);
    background-color: var(--color-light);
}

/* =========================
   TIPOGRAFIA
   ========================= */
h1, h2, h3 {
    font-family: var(--font-heading);
    font-weight: 600;
    color: var(--color-dark);
}

a {
    text-decoration: none;
    color: inherit;
    transition: color 0.3s, background-color 0.3s;
}

/* =========================
   HEADER
   ========================= */
header {
    background: linear-gradient(135deg, var(--color-dark), var(--color-primary));
    color: var(--color-white);
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
    border: 4px solid var(--color-white);
    object-fit: cover;
}

.tagline {
    font-style: italic;
    font-weight: 300;
    margin-top: 0.5rem;
}

/* =========================
   NAVEGAÇÃO
   ========================= */
nav ul {
    display: flex;
    justify-content: center;
    list-style: none;
    gap: 1.5rem;
    flex-wrap: wrap;
}

nav a {
    padding: 0.5rem 1rem;
    border-radius: var(--radius-sm);
}

nav a:hover {
    background-color: rgba(255, 255, 255, 0.2);
}

/* =========================
   CONTEÚDO PRINCIPAL
   ========================= */
main {
    max-width: 1200px;
    margin: 2rem auto;
    padding: 0 1rem;
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
}

.section-card {
    background: var(--color-white);
    border-radius: var(--radius-md);
    padding: 2rem;
    box-shadow: var(--shadow-md);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.section-card:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-lg);
}

.section-card h2 {
    margin-bottom: 1.5rem;
    border-bottom: 2px solid var(--color-primary);
    padding-bottom: 0.5rem;
    display: inline-block;
}

/* =========================
   SEÇÃO SOBRE MIM
   ========================= */
#sobre p {
    text-align: justify;
}

/* =========================
   SEÇÃO HABILIDADES
   ========================= */
.skills-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
}

.skill-category h3 {
    margin-bottom: 0.5rem;
    color: var(--color-primary);
}

.skill-category ul {
    list-style-position: inside;
}

.skill-category li {
    margin-bottom: 0.3rem;
}

/* =========================
   SEÇÃO PROJETOS
   ========================= */
.projects-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
}

.project-card {
    border: 1px solid #e0e0e0;
    border-radius: var(--radius-md);
    padding: 1.5rem;
    box-shadow: var(--shadow-sm);
    transition: transform 0.3s, box-shadow 0.3s;
    background-color: var(--color-white);
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
}

.project-card h3 {
    margin-bottom: 0.5rem;
}

.project-card p {
    margin-bottom: 1rem;
}

.project-link {
    display: inline-block;
    background-color: var(--color-primary);
    color: var(--color-white);
    padding: 0.5rem 1rem;
    border-radius: var(--radius-sm);
}

.project-link:hover {
    background-color: var(--color-primary-dark);
}

/* =========================
   ASIDE / HOBBIES
   ========================= */
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
    background-color: var(--color-primary);
    color: var(--color-white);
    border-radius: var(--radius-sm);
}

.social-links a:hover {
    background-color: var(--color-primary-dark);
}

/* =========================
   FOOTER
   ========================= */
footer {
    background-color: var(--color-dark);
    color: var(--color-white);
    text-align: center;
    padding: 2rem 1rem;
}

.footer-content {
    max-width: 800px;
    margin: 0 auto;
}

footer a {
    color: var(--color-primary);
}

footer a:hover {
    color: var(--color-primary-dark);
}

/* =========================
   RESPONSIVIDADE
   ========================= */
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
