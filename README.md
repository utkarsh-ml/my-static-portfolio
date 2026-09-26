<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>
   
</head>
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');

:root {
  color-scheme: dark;
  --background: #0b1120;
  --surface: #111a2d;
  --surface-light: #17233a;
  --text: #e8eef8;
  --muted: #a4b1c7;
  --accent: #5eead4;
  --accent-dark: #0f766e;
  --border: rgba(164, 177, 199, 0.16);
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 6rem;
}

body {
  min-height: 100vh;
  background: radial-gradient(ellipse at 50% -20%, #1c3150 0, var(--background) 55%);
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.7;
}

header {
  position: sticky;
  top: 0;
  z-index: 10;
  padding: 1rem max(5vw, calc((100vw - 1100px) / 2));
  background: rgba(11, 17, 32, 0.88);
  border-bottom: 1px solid var(--border);
  backdrop-filter: blur(14px);
}

header h1 {
  color: var(--text);
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.25rem;
  letter-spacing: -0.03em;
}

nav#nav {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.3rem 1.25rem;
  margin-top: 0.55rem;
  color: var(--muted);
  font-size: 0.9rem;
}

nav#nav a,
a {
  color: var(--accent);
  text-decoration: none;
  transition: color 160ms ease, background 160ms ease;
}

nav#nav a:hover,
a:hover {
  color: #99f6e4;
}

main {
  width: min(100% - 2.5rem, 900px);
  margin: 0 auto;
}

section {
  padding: 5rem 0;
  scroll-margin-top: 5rem;
}

#home {
  padding: 7rem 0 6rem;
}

#home h2 {
  max-width: 700px;
  font-size: clamp(2.7rem, 8vw, 5rem);
  line-height: 1.05;
  letter-spacing: -0.06em;
}

#home h2::after {
  display: block;
  width: 4rem;
  height: 4px;
  margin-top: 1.4rem;
  border-radius: 99px;
  background: var(--accent);
  content: '';
}

#home p:first-of-type {
  max-width: 620px;
  margin-top: 1.5rem;
  color: var(--muted);
  font-size: 1.15rem;
}

#home p:last-of-type {
  display: flex;
  flex-wrap: wrap;
  gap: 0.85rem;
  margin-top: 2rem;
}

#home p:last-of-type a {
  display: inline-block;
  padding: 0.7rem 1.15rem;
  border: 1px solid var(--accent);
  border-radius: 0.65rem;
  font-weight: 700;
}

#home p:last-of-type a:first-child {
  background: var(--accent);
  color: #08211f;
}

#home p:last-of-type a:first-child:hover {
  background: #99f6e4;
}

#home p:last-of-type a:last-child:hover {
  background: rgba(94, 234, 212, 0.1);
}

hr {
  height: 1px;
  border: 0;
  background: var(--border);
}

section h2 {
  margin-bottom: 1.5rem;
  font-family: 'Space Grotesk', sans-serif;
  font-size: clamp(1.8rem, 5vw, 2.5rem);
  letter-spacing: -0.04em;
}

section p {
  margin: 0 0 1rem;
  color: var(--muted);
}

strong {
  color: var(--text);
}

#projects article {
  margin-top: 1rem;
  padding: 1.4rem 1.5rem;
  border: 1px solid var(--border);
  border-radius: 0.9rem;
  background: linear-gradient(135deg, var(--surface-light), var(--surface));
  transition: transform 180ms ease, border-color 180ms ease;
}

#projects article:hover {
  transform: translateY(-3px);
  border-color: rgba(94, 234, 212, 0.5);
}

#projects h3 {
  margin-bottom: 0.35rem;
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.2rem;
}

#projects article p {
  margin-bottom: 0;
}

#experience ul {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.8rem;
  list-style: none;
}

#experience li {
  padding: 1rem 1.1rem;
  border: 1px solid var(--border);
  border-radius: 0.75rem;
  background: var(--surface);
  color: var(--muted);
}

#contact > p {
  margin-bottom: 0.45rem;
}

form {
  display: grid;
  gap: 0.35rem;
  max-width: 600px;
  margin-top: 2rem;
  padding: 1.5rem;
  border: 1px solid var(--border);
  border-radius: 1rem;
  background: var(--surface);
}

form p {
  margin: 0;
}

label {
  display: inline-block;
  margin-bottom: 0.35rem;
  color: var(--text);
  font-size: 0.92rem;
  font-weight: 600;
}

input[type='text'],
input[type='email'],
textarea {
  width: 100%;
  padding: 0.75rem 0.85rem;
  border: 1px solid var(--border);
  border-radius: 0.55rem;
  outline: none;
  background: #0b1120;
  color: var(--text);
  font: inherit;
}

input:focus,
textarea:focus {
  border-color: var(--accent);
  box-shadow: 0 0 0 3px rgba(94, 234, 212, 0.12);
}

textarea {
  min-height: 130px;
  resize: vertical;
}

input[type='submit'] {
  margin-top: 0.75rem;
  padding: 0.75rem 1.1rem;
  border: 0;
  border-radius: 0.6rem;
  background: var(--accent);
  color: #08211f;
  cursor: pointer;
  font: inherit;
  font-weight: 700;
}

input[type='submit']:hover {
  background: #99f6e4;
}

footer {
  padding: 1.5rem 1rem;
  border-top: 1px solid var(--border);
  color: var(--muted);
  text-align: center;
  font-size: 0.9rem;
}

@media (max-width: 600px) {
  header {
    padding: 0.9rem 1.25rem;
  }

  nav#nav {
    gap: 0.25rem 0.85rem;
    font-size: 0.82rem;
  }

  main {
    width: min(100% - 2rem, 900px);
  }

  section {
    padding: 3.5rem 0;
  }

  #home {
    padding: 5rem 0 4.5rem;
  }

  #experience ul {
    grid-template-columns: 1fr;
  }

  form {
    padding: 1.1rem;
  }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    transition-duration: 0.01ms !important;
  }
}

</style>

<body>
  <header>
    <h1>Utkarsh Mani Singh</h1>
    <nav id="nav">
      <a href="#home">Home</a> |
      <a href="#about">About</a> |
      <a href="#projects">Projects</a> |
      <a href="#experience">What I’m Working On</a> |
      <a href="#contact">Contact</a> |
      <a href="https://github.com/utkarsh-ml" target="_blank" rel="noopener noreferrer">GitHub</a>
    </nav>
  </header>

  <main>
    <section id="home">
      <h2>Welcome</h2>
      <p>Hello! I'm a web developer passionate about creating simple, useful, and modern digital experiences.</p>
      <p><a href="#projects">View My Work</a> | <a href="#contact">Hire Me</a></p>
    </section>

    <hr>

    <section id="about">
      <h2>About Me</h2>
      <p>I’m a B.Tech Computer Science &amp; Engineering (AI &amp; ML) student focused on becoming an industry-ready AI Engineer. I’m building my foundation across Python, software engineering, data structures &amp; algorithms, databases, APIs, web development, AI/ML, automation, and AI agents.</p>
      <p>I learn by building rather than simply following tutorials. My approach is simple: <strong>Learn → Understand → Design → Build → Test → Debug → Deploy → Document → Improve.</strong></p>
      <p>Currently, I’m strengthening my software engineering fundamentals, developing real-world projects, and exploring how AI can be combined with backend systems, automation, and intelligent applications.</p>
      <p>My long-term goal is to build production-quality AI systems and products that solve practical problems—not just models that work in a notebook.</p>
    </section>

    <hr>

    <section id="projects">
      <h2>Projects</h2>
      <article>
        <h3>Portfolio Website</h3>
        <p>Designed and developed a personal portfolio to showcase work, skills, and experience.</p>
      </article>
      <article>
        <h3>Business Landing Page</h3>
        <p>Created a clean landing page for a startup with a strong focus on clarity and conversion.</p>
      </article>
      <article>
        <h3>Online Store UI</h3>
        <p>Built a simple and attractive e-commerce interface to improve product browsing experience.</p>
      </article>
    </section>

    <hr>

    <section id="experience">
      <h2>What I’m Working On</h2>
      <ul>
        <li>🤖 <strong>AI Engineering</strong> — Machine Learning, Computer Vision, AI Agents</li>
        <li>🐍 <strong>Python</strong> — Advanced Python, OOP, automation and backend development</li>
        <li>⚙️ <strong>Software Engineering</strong> — Git, databases, APIs, architecture and SOLID principles</li>
        <li>🧠 <strong>DSA</strong> — Building problem-solving and algorithmic thinking</li>
        <li>🌐 <strong>Web &amp; Backend</strong> — Developing APIs and production-oriented applications</li>
        <li>🌱 <strong>AGROGEN</strong> — AI-powered agricultural intelligence and automation platform</li>
        <li>🚀 <strong>Mission 2030</strong> — Long-term journey toward becoming an industry-ready AI Engineer</li>
      </ul>
    </section>

    <hr>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: utkarsh.studio08@gmail.com</p>
      <p>Phone: +91 6393206600</p>
      <p>Location: Delhi, INDIA</p>
      <p>GitHub: <a href="https://github.com/utkarsh-ml" target="_blank" rel="noopener noreferrer">github.com/utkarsh-ml</a></p>
      <p>CodeChef: <a href="https://www.codechef.com/users/utkarsh_mani" target="_blank" rel="noopener noreferrer">utkarsh_mani</a></p>
      <p>HackerRank: <a href="https://www.hackerrank.com/utkarsh_mani" target="_blank" rel="noopener noreferrer">utkarsh_mani</a></p>
      <p>LeetCode: <a href="https://leetcode.com/utkarsh_mani_" target="_blank" rel="noopener noreferrer">utkarsh_mani_</a></p>
      <form id="contact-form">
        <p>
          <label for="name">Name:</label><br>
          <input id="name" type="text" name="name" required>
        </p>
        <p>
          <label for="email">Email:</label><br>
          <input id="email" type="email" name="email" required>
        </p>
        <p>
          <label for="message">Message:</label><br>
          <textarea id="message" name="message" rows="4" cols="40" required></textarea>
        </p>
        <p>
          <input type="submit" value="Send Message">
        </p>
      </form>
      <p id="form-status" role="status" aria-live="polite"></p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Utkarsh Mani Singh</p>
  </footer>
  <script>
    const contactForm = document.getElementById('contact-form');
    const formStatus = document.getElementById('form-status');
    const storageKey = 'portfolioContactMessages';

    contactForm.addEventListener('submit', (event) => {
      event.preventDefault();

      const formData = new FormData(contactForm);
      const message = {
        name: formData.get('name').trim(),
        email: formData.get('email').trim(),
        message: formData.get('message').trim(),
        submittedAt: new Date().toISOString()
      };

      try {
        const savedMessages = JSON.parse(localStorage.getItem(storageKey) || '[]');
        savedMessages.push(message);
        localStorage.setItem(storageKey, JSON.stringify(savedMessages));

        formStatus.textContent = 'Your message was saved in this browser.';
        contactForm.reset();
      } catch (error) {
        formStatus.textContent = 'The message could not be saved. Please check that browser storage is available.';
        console.error('Could not save the contact message:', error);
      }
    });
  </script>
</body>
</html>
