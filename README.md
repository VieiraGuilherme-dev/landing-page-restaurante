# 🚖 VeloCity

VeloCity é um site moderno e intuitivo desenvolvido para conectar passageiros a motoristas de táxi, carro e moto com rapidez e segurança. Com um design responsivo e funcionalidades avançadas, o VeloCity oferece uma experiência de agendamento online personalizada e eficiente.

## 📌 Funcionalidades

- 🚕 **Reserva de Táxis Online:** Agende sua corrida de maneira rápida e segura.
- 🎯 **Personalização de Viagem:** Ajuste o trajeto, música, temperatura e escolha o tipo de veículo.
- ⏰ **Suporte 24/7:** Atendimento ao cliente disponível em tempo integral.
- 📊 **Interface Responsiva:** Design adaptável para dispositivos móveis, tablets e desktops.
- 🔎 **Busca Rápida:** Acesse facilmente as principais informações e funcionalidades.

## 📂 Estrutura do Projeto e Detalhes de Implementação

## 1. Estrutura HTML (index.html)

O arquivo `index.html` contém a estrutura básica da página, com a parte visual do jogo, como a área de resultados e a seleção de opções do usuário.

~~~html
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" type="text/css" href="style.css">
    <link rel="stylesheet" href="https://unpkg.com/boxicons@latest/css/boxicons.min.css">
    <link href="https://cdn.jsdelivr.net/npm/remixicon@4.5.0/fonts/remixicon.css" rel="stylesheet" />
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lexend:wght@100..900&family=Roboto:wght@700&display=swap"
        rel="stylesheet">
    <title>VeloCity</title>
</head>

<body>

    <header>
        <a href="#" class="logo">
            <img src="img/logo.png" alt="VeloCity Logo">
        </a>

        <ul class="navlinks">
            <a href="#home">Home</a>
            <a href="#about">About Us</a>
            <a href="#services">Services</a>
            <a href="#feature">Latest Features</a>
            <a href="#contact">Contact</a>
        </ul>

        <div class="h-right">
            <a href="#"><img width="30" height="30" src="https://img.icons8.com/ios/30/ffffff/search--v1.png"
                    alt="search" /></a>
            <a href="#" class="h-btn">Book a taxi</a>
            <div class="bx bx-menu" id="menu-icon"></div>
        </div>
    </header>

~~~

---

## 2. Estilização CSS

Abaixo está o código CSS que define a aparência do site, incluindo as animações para os resultados e interações.

~~~css
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
    scroll-behavior: smooth;
    font-family: "Lexend", sans-serif;
}

:root {
    --h1-font: 4rem;
    --h2-font: 3.5rem;
    --p-font: 1.1rem;

    --bg-color: #ffffff;
    --text-color: #000000;
    --main-color: #ffee02;
    --other-color: #727272;
}

body {
    background: var(--bg-color);
    color: var(--text-color);
}

header {
    position: fixed;
    width: 100%;
    top: 0;
    right: 0;
    z-index: 1000;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: var(--text-color);
    padding: 25px 17%;
    transition: all .7s ease;
}
~~~

---

## 3. Lógica JavaScript

Aqui está o código JavaScript que controla a interação do usuário, o resultado do jogo e as animações.

~~~javascript
const header = document.querySelector("header");

window.addEventListener("scroll", function () {
    header.classList.toggle("sticky", window.scrollY > 160);
});

let menu = document.querySelector('#menu-icon');
let navlinks = document.querySelector('.navlinks');

menu.onclick = () => {
    menu.classList.toggle('bx-x');
    navlinks.classList.toggle('open');
};

window.onscroll = () => {
    menu.classList.remove('bx-x');
    navlinks.classList.remove('open');
};

const animate = ScrollReveal({
    origin: 'top',
    distance: '65px',
    duration: 2600, // Corrigido de 'durarion' para 'duration'
    delay: 400
});

animate.reveal(".home-text, .about-img, .feature-left, .social-icons", { origin: "left" });

animate.reveal(".arrow, .about-text, .feature-right", { origin: "right" });

animate.reveal(".home-img, .text-center, .services-content, .feature-middle, .end-text1, end-text2, .contact-box", { interval: 150});

~~~

---
## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura do site
- **CSS3**: Estilização e layout responsivo
- **JavaScript**: Interatividade e funcionalidades dinâmicas
- **Boxicons** e **Remixicon**: Ícones modernos
- **Google Fonts**: Tipografia personalizada (Lexend e Roboto)

## 🚀 Como Executar o Projeto

1. Clone este repositório:

```bash
   git clone https://github.com/seu-usuario/velocity.git
```

2. Navegue até o diretório do projeto:

```bash
   cd velocity
```

3. Abra o arquivo `index.html` em seu navegador preferido.

## 📞 Contato

Desenvolvido por **Guilherme Vieira**. Entre em contato:

- Email: [gv524003@gmail.com](mailto:gv524003@gmail.com)
- LinkedIn: [linkedin.com/in/seu-perfil](https://linkedin.com/in/seu-perfil)

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para utilizá-lo e modificá-lo conforme necessário.

