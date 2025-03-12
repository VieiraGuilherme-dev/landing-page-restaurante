<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Century+Gothic&weight=800&size=48&pause=1000&color=F7F7F7&center=true&vCenter=true&width=600&lines=Landing+Page+do+Restaurante" alt="Typing SVG" />
</p>

---

# 📖 Visão Geral

Este projeto foi desenvolvido para a landing page de um restaurante, com o objetivo de atrair clientes e apresentar os principais serviços e produtos oferecidos. A aplicação foi construída utilizando **HTML5**, **CSS3** e **JavaScript** para criar uma interface visualmente agradável, com foco na experiência do usuário e em uma navegação simples e rápida. 🍽️✨

---

# 🌟 Funcionalidades e Destaques

- **Design Atraente:** Layout moderno e responsivo com imagens de alta qualidade para apresentar os pratos e o ambiente do restaurante. 📸🍴

- **Animações com CSS:** Animações suaves ao passar o mouse sobre os itens do menu e imagens de destaque, proporcionando uma experiência interativa e visualmente envolvente.

- **Interatividade com JavaScript:** Formulário dinâmico para reservas online, onde os usuários podem selecionar data, hora e quantidade de pessoas. ⏳

- **Menu de Navegação Simples:** Barra de navegação com links para as principais seções do site, como Cardápio, Reservas e Contato. 📜

---

# 🛠️ Tecnologias Utilizadas

<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" height="35"  />

• Estruturação do conteúdo e organização da página.

##

<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" height="35"  />
  
• Estilização moderna e responsiva, incluindo transições e animações para melhorar a interação do usuário.

##

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" height="35"  />
  
• Adição de interatividade, como o formulário de reserva e a navegação dinâmica entre as seções do site.

---

# 📂 Estrutura do Projeto e Detalhes de Implementação

## 1. Composição da Landing Page (index.html)

O arquivo `index.html` contém a estrutura principal da página, com seções destacando o cardápio, informações sobre o restaurante, formulário de reservas e a área de contato.

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Restaurante Saboroso</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#menu">Cardápio</a></li>
        <li><a href="#reservations">Reservas</a></li>
        <li><a href="#contact">Contato</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="menu">
      <h2>Nosso Cardápio</h2>
      <p>Explore os deliciosos pratos que preparamos especialmente para você!</p>
      <div class="menu-items">
        <!-- Exemplos de itens do cardápio -->
        <div class="menu-item">
          <img src="img/prato1.jpg" alt="Prato 1">
          <h3>Prato 1</h3>
          <p>Descrição do prato 1</p>
        </div>
        <div class="menu-item">
          <img src="img/prato2.jpg" alt="Prato 2">
          <h3>Prato 2</h3>
          <p>Descrição do prato 2</p>
        </div>
      </div>
    </section>

    <section id="reservations">
      <h2>Faça Sua Reserva</h2>
      <form id="reservation-form">
        <label for="date">Data:</label>
        <input type="date" id="date" name="date" required>
        
        <label for="time">Hora:</label>
        <input type="time" id="time" name="time" required>
        
        <label for="people">Quantidade de Pessoas:</label>
        <input type="number" id="people" name="people" required>
        
        <button type="submit">Reservar Agora</button>
      </form>
    </section>

    <section id="contact">
      <h2>Contato</h2>
      <p>Entre em contato conosco para mais informações.</p>
      <p>Email: contato@restaurantesaboroso.com</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Restaurante Saboroso | Todos os direitos reservados.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
~~~

---

## 2. Estilização e Design Responsivo com CSS

**Exemplo: Estilo do Menu de Itens**

Utilizamos CSS para criar um layout limpo e responsivo para exibir os itens do cardápio de forma atraente, com imagens e descrições.

~~~css
/* Estilo do menu */
.menu-items {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.menu-item {
  width: 200px;
  text-align: center;
  margin: 15px;
}

.menu-item img {
  width: 100%;
  border-radius: 8px;
  transition: transform 0.3s ease;
}

.menu-item:hover img {
  transform: scale(1.1); /* Animação ao passar o mouse */
}
~~~

---

## 3. Interatividade com JavaScript

**Exemplo: Formulário de Reserva**

Usamos JavaScript para validar o formulário de reservas, garantindo que todos os campos sejam preenchidos corretamente antes de enviar os dados.

~~~javascript
document.getElementById('reservation-form').addEventListener('submit', function(event) {
  const date = document.getElementById('date').value;
  const time = document.getElementById('time').value;
  const people = document.getElementById('people').value;

  if (!date || !time || !people) {
    alert('Por favor, preencha todos os campos!');
    event.preventDefault();
  } else {
    alert('Reserva realizada com sucesso!');
  }
});
~~~

---

## 4. Responsividade

O design do site foi feito para ser completamente responsivo, adaptando-se a diferentes tamanhos de tela, com media queries para ajustar a estrutura e o layout conforme necessário.

~~~css
/* Layout para telas pequenas */
@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    align-items: center;
  }

  .menu-items {
    flex-direction: column;
  }

  section {
    padding: 20px;
  }
}
~~~

---

# 🚀 Como Rodar o Projeto Localmente

Para testar ou desenvolver localmente, siga estes passos:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seuusuario/landing-page-restaurante.git
   cd landing-page-restaurante

