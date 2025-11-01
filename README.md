/* ================================
   🎨 SISTEMA DE DESIGN
==================================*/
:root {
  /* Paleta principal */
  --cor-primaria: #0077b6;
  --cor-secundaria: #00b4d8;
  --cor-escura: #023e8a;
  --cor-clara: #caf0f8;
  --cor-texto: #333;

  /* Espaçamentos (escala modular) */
  --espaco-xs: 4px;
  --espaco-s: 8px;
  --espaco-m: 16px;
  --espaco-l: 32px;
  --espaco-xl: 48px;

  /* Tipografia */
  --fonte-principal: "Segoe UI", Arial, sans-serif;
  --tamanho-texto: 1rem;
  --tamanho-titulo: 2rem;
}

/* ================================
   ✨ ESTILOS GERAIS
==================================*/
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: var(--fonte-principal);
  background-color: var(--cor-clara);
  color: var(--cor-texto);
  line-height: 1.6;
}

/* ================================
   🧭 NAVEGAÇÃO
==================================*/
header {
  background-color: var(--cor-primaria);
  color: white;
  text-align: center;
  padding: var(--espaco-m);
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  background-color: var(--cor-escura);
  margin-top: var(--espaco-s);
}

nav li {
  margin: 0 var(--espaco-s);
}

nav a {
  color: white;
  text-decoration: none;
  padding: var(--espaco-s) var(--espaco-m);
  display: block;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

nav a:hover,
nav a:focus {
  background-color: var(--cor-secundaria);
}

/* ================================
   📱 LAYOUTS RESPONSIVOS (Flexbox)
==================================*/
main {
  padding: var(--espaco-l);
  text-align: center;
}

section.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: var(--espaco-m);
  background: white;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  padding: var(--espaco-l);
}

.projetos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: var(--espaco-l);
}

.projeto {
  background: white;
  padding: var(--espaco-m);
  border-radius: 10px;
  width: 280px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.projeto:hover {
  transform: translateY(-5px);
}

/* ================================
   🧠 COMPONENTES DE INTERFACE
==================================*/
button {
  background-color: var(--cor-secundaria);
  color: white;
  border: none;
  padding: var(--espaco-s) var(--espaco-m);
  border-radius: 5px;
  cursor: pointer;
  font-size: var(--tamanho-texto);
  transition: background-color 0.3s;
}

button:hover,
button:focus {
  background-color: var(--cor-primaria);
}

/* Formulário */
form {
  background-color: white;
  max-width: 400px;
  margin: 0 auto;
  padding: var(--espaco-l);
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

label {
  display: block;
  margin-top: var(--espaco-m);
  text-align: left;
}

input, textarea {
  width: 100%;
  padding: var(--espaco-s);
  margin-top: var(--espaco-s);
  border: 1px solid #ccc;
  border-radius: 5px;
}

/* ================================
   👁️‍🗨️ ACESSIBILIDADE E RESPONSIVIDADE
==================================*/
a:focus,
button:focus,
input:focus,
textarea:focus {
  outline: 2px solid var(--cor-secundaria);
  outline-offset: 3px;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
  }

  .projetos {
    flex-direction: column;
    align-items: center;
  }

  main {
    padding: var(--espaco-m);
  }
}

/* ================================
   ⚙️ RODAPÉ
==================================*/
footer {
  background-color: var(--cor-escura);
  color: white;
  text-align: center;
  padding: var(--espaco-m);
  margin-top: var(--espaco-l);
}
