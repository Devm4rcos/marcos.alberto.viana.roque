# marcos.alberto.viana.roque


<>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio - Marcos Alberto Viana Roque</title>
    <!-- Início do bloco de estilos CSS puro, sem frameworks -->
    <style>
        /* Estilos de reset e base */
        :root {
            --cor-primaria: #007BFF; /* Azul para destaque */
            --cor-secundaria: #333; /* Cinza escuro para texto */
            --cor-fundo: #f4f4f9; /* Cinza claro para o fundo */
            --cor-clara: #ffffff; /* Branco */
            --sombra-caixa: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: var(--cor-fundo);
            color: var(--cor-secundaria);
            padding-top: 60px; /* Espaço para o menu fixo */
        }

        /* Estilos do cabeçalho e menu de navegação (Fixo) */
        .cabecalho {
            background-color: var(--cor-secundaria);
            color: var(--cor-clara);
            padding: 15px 0;
            position: fixed; /* Torna o menu fixo no topo */
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: var(--sombra-caixa);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo a {
            color: var(--cor-clara);
            text-decoration: none;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-menu ul {
            list-style: none;
            display: flex;
        }

        .nav-menu ul li {
            margin-left: 20px;
        }

        .nav-menu ul li a {
            color: var(--cor-clara);
            text-decoration: none;
            font-weight: 500;
            padding: 5px 10px;
            border-radius: 4px;
            transition: background-color 0.3s, color 0.3s;
        }

        .nav-menu ul li a:hover, .nav-menu ul li a.ativo {
            background-color: var(--cor-primaria);
            color: var(--cor-clara);
        }

        /* Estilos das seções principais */
        .secao {
            padding: 60px 0;
            min-height: 80vh; /* Garante que a seção ocupe a maior parte da tela */
        }

        .secao:nth-child(even) {
            background-color: var(--cor-clara); /* Fundo branco para seções pares */
        }

        .secao h2 {
            font-size: 2.5rem;
            color: var(--cor-primaria);
            margin-bottom: 30px;
            text-align: center;
            border-bottom: 2px solid var(--cor-primaria);
            display: inline-block;
            padding-bottom: 5px;
            margin-left: 50%;
            transform: translateX(-50%);
        }

        /* Estilos específicos da seção Sobre Mim */
        #sobre .perfil {
            display: flex;
            gap: 40px;
            align-items: center;
            padding: 20px;
        }

        .perfil-foto {
            flex-shrink: 0; /* Impede a imagem de encolher */
        }

        .perfil-foto img {
            width: 250px;
            height: 250px;
            object-fit: cover;
            border-radius: 50%; /* Foto redonda */
            border: 5px solid var(--cor-primaria);
            box-shadow: var(--sombra-caixa);
        }

        .perfil-info h3 {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--cor-secundaria);
        }

        /* Estilos específicos da seção Formação */
        .timeline {
            position: relative;
            max-width: 1000px;
            margin: 0 auto;
            padding-left: 30px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            top: 0;
            left: 10px;
            bottom: 0;
            width: 4px;
            background-color: var(--cor-primaria);
        }

        .timeline-item {
            margin-bottom: 40px;
            position: relative;
            padding-left: 40px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background-color: var(--cor-primaria);
            border: 3px solid var(--cor-fundo);
            left: 3px;
            top: 5px;
        }

        .timeline-item h4 {
            font-size: 1.2rem;
            color: var(--cor-primaria);
        }
        
        .timeline-item p.periodo {
            font-style: italic;
            color: #666;
            margin-bottom: 5px;
        }

        .idiomas-lista {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            text-align: center;
        }
        
        /* Estilos específicos da seção Portfólio */
        .grid-portfolio {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .projeto-card {
            background-color: var(--cor-clara);
            border-radius: 8px;
            box-shadow: var(--sombra-caixa);
            overflow: hidden;
            transition: transform 0.3s;
            text-align: center;
            padding: 20px;
        }

        .projeto-card:hover {
            transform: translateY(-5px);
        }

        .projeto-card h3 {
            color: var(--cor-primaria);
            margin-bottom: 10px;
        }

        .projeto-card a {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 15px;
            background-color: var(--cor-primaria);
            color: var(--cor-clara);
            text-decoration: none;
            border-radius: 4px;
            font-weight: bold;
        }

        /* Estilos específicos da seção Contato (Formulário) */
        .form-container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: var(--cor-clara);
            border-radius: 8px;
            box-shadow: var(--sombra-caixa);
        }

        .form-grupo {
            margin-bottom: 20px;
        }

        .form-grupo label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        .form-grupo input[type="text"],
        .form-grupo input[type="email"],
        .form-grupo textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1rem;
        }

        .form-grupo textarea {
            resize: vertical;
            min-height: 150px;
        }

        .botao-enviar {
            background-color: var(--cor-primaria);
            color: var(--cor-clara);
            border: none;
            padding: 12px 25px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1.1rem;
            transition: background-color 0.3s;
            width: 100%;
        }

        .botao-enviar:hover {
            background-color: #0056b3; /* Um azul mais escuro no hover */
        }
        
        /* Estilos para mensagens de validação */
        .mensagem-erro {
            color: red;
            font-size: 0.9rem;
            margin-top: 5px;
            display: none; /* Escondido por padrão */
        }

        .mensagem-alerta {
            padding: 15px;
            margin-top: 20px;
            border-radius: 4px;
            font-weight: bold;
            text-align: center;
        }

        .alerta-sucesso {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }

        /* Estilos responsivos (Mobile-first) */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
                padding: 0 10px;
            }

            .cabecalho {
                padding: 10px 0;
            }

            .logo {
                margin-bottom: 10px;
            }

            .nav-menu ul {
                flex-direction: column;
                align-items: center;
            }

            .nav-menu ul li {
                margin: 5px 0;
            }

            .secao {
                padding: 40px 0;
            }

            #sobre .perfil {
                flex-direction: column;
                text-align: center;
            }

            .perfil-foto img {
                width: 150px;
                height: 150px;
            }

            .timeline {
                padding-left: 20px;
            }

            .timeline::before, .timeline-item::before {
                left: 0px; /* Ajuste para centralizar no mobile */
            }
        }
    </style>
    <!-- Fim do bloco de estilos CSS puro -->
</head>
<body>

    <!-- CABEÇALHO FIXO E MENU DE NAVEGAÇÃO -->
    <header class="cabecalho">
        <div class="container">
            <div class="logo">
                <a href="#sobre">Marcos Alberto Viana Roque</a>
            </div>
            <nav class="nav-menu">
                <ul>
                    <!-- Links que levam às seções (SPA) -->
                    <li><a href="#sobre" class="nav-link">Sobre mim</a></li>
                    <li><a href="#formacao" class="nav-link">Formação</a></li>
                    <li><a href="#portfolio" class="nav-link">Portfólio</a></li>
                    <li><a href="#contato" class="nav-link">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- CONTEÚDO PRINCIPAL (Todas as Seções/Páginas) -->
    <main>

        <!-- SEÇÃO 1: SOBRE MIM (index.html simulado) -->
        <section id="sobre" class="secao">
            <div class="container">
                <h2>Sobre Mim</h2>
                <div class="perfil">
                    <div class="perfil-foto">
                        <!-- Imagem placeholder, substitua por sua foto real -->
                        <img src="https://placehold.co/250x250/007BFF/ffffff?text=Marcos" alt="Foto de Marcos Alberto Viana Roque">
                    </div>
                    <div class="perfil-info">
                        <h3>Marcos Alberto Viana Roque</h3>
                        <p>Desenvolvedor Full Stack com foco em soluções eficientes e escaláveis. Minha jornada na tecnologia começou com uma paixão por resolver problemas complexos e transformá-los em aplicações simples e intuitivas. Tenho experiência em desenvolvimento web, desde a criação da interface do usuário (Front-end) até a lógica de negócios e persistência de dados (Back-end).</p>
                        <p>Atualmente, busco oportunidades para aplicar meus conhecimentos em projetos desafiadores e continuar o aprendizado contínuo, que é a essência desta área.</p>
                        
                        <h4>Hobbies & Interesses</h4>
                        <p>Nas horas vagas, sou um entusiasta de esportes ao ar livre, como trilhas e ciclismo. Também me dedico à leitura sobre inteligência artificial e a jogos de estratégia que aprimoram o raciocínio lógico.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- SEÇÃO 2: FORMAÇÃO (formacao.html simulado) -->
        <section id="formacao" class="secao">
            <div class="container">
                <h2>Formação e Qualificações</h2>

                <div class="timeline">
                    <!-- Item 1: Formação Educacional Mais Recente -->
                    <div class="timeline-item">
                        <h4>Bacharelado em Ciência da Computação</h4>
                        <p>Universidade Federal de Tecnologia (UFT)</p>
                        <p class="periodo">2018 - 2022</p>
                        <p>Conclusão do curso com ênfase em desenvolvimento de software e algoritmos de alto desempenho.</p>
                    </div>
                    
                    <!-- Item 2: Curso de Especialização (Exemplo) -->
                    <div class="timeline-item">
                        <h4>Bootcamp Desenvolvedor Full Stack Moderno</h4>
                        <p>TechSkills Academy Online</p>
                        <p class="periodo">Julho 2023 - Outubro 2023</p>
                        <p>Curso intensivo cobrindo tecnologias como Node.js, Banco de Dados NoSQL e Arquitetura de Microserviços.</p>
                    </div>
                    
                    <!-- Item 3: Certificação (Exemplo) -->
                    <div class="timeline-item">
                        <h4>Certificação em Cloud Computing (AWS Certified Practitioner)</h4>
                        <p>Amazon Web Services</p>
                        <p class="periodo">Abril 2024</p>
                        <p>Conhecimento fundamental e compreensão geral dos serviços da AWS.</p>
                    </div>
                </div>

                <h3>Idiomas</h3>
                <ul class="idiomas-lista">
                    <li><strong>Português:</strong> Nativo</li>
                    <li><strong>Inglês:</strong> Avançado (Certificado TOEFL)</li>
                    <li><strong>Espanhol:</strong> Básico</li>
                </ul>
            </div>
        </section>

        <!-- SEÇÃO 3: PORTFÓLIO (portfolio.html simulado) -->
        <section id="portfolio" class="secao">
            <div class="container">
                <h2>Projetos Realizados</h2>
                <div class="grid-portfolio">
                    
                    <!-- Projeto 1 -->
                    <div class="projeto-card">
                        <h3>Sistema de Gestão de Biblioteca</h3>
                        <p>Sistema Web para controle de empréstimos, devoluções e catálogo de livros.</p>
                        <p><small>Tecnologias: HTML, CSS Puro, JavaScript Vanilla, PHP.</small></p>
                        <a href="https://github.com/MarcosAlbertoVianaRoque/projeto-biblioteca" target="_blank">Ver Projeto</a>
                    </div>
                    
                    <!-- Projeto 2 -->
                    <div class="projeto-card">
                        <h3>Calculadora de Investimentos Interativa</h3>
                        <p>Ferramenta para simular diferentes cenários de investimento com gráficos dinâmicos.</p>
                        <p><small>Tecnologias: HTML, CSS Puro, JavaScript (manipulação de DOM e lógica).</small></p>
                        <a href="https://github.com/MarcosAlbertoVianaRoque/calculadora-investimentos" target="_blank">Ver Projeto</a>
                    </div>
                    
                    <!-- Projeto 3 -->
                    <div class="projeto-card">
                        <h3>Landing Page Responsiva</h3>
                        <p>Design moderno e totalmente responsivo para um produto SaaS fictício.</p>
                        <p><small>Tecnologias: HTML5 Semântico e CSS3 (Flexbox/Grid).</small></p>
                        <a href="https://github.com/MarcosAlbertoVianaRoque/landing-page-responsiva" target="_blank">Ver Projeto</a>
                    </div>

                </div>
            </div>
        </section>

        <!-- SEÇÃO 4: CONTATO (contato.html simulado) -->
        <section id="contato" class="secao">
            <div class="container">
                <h2>Entre em Contato</h2>
                <div class="form-container">
                    <p style="margin-bottom: 20px;">Use o formulário abaixo para enviar uma mensagem. Todos os campos são obrigatórios.</p>

                    <form id="formulario-contato">
                        <!-- Campo Nome (Obrigatório) -->
                        <div class="form-grupo">
                            <label for="nome">Nome Completo:</label>
                            <input type="text" id="nome" name="nome" required>
                            <span id="erro-nome" class="mensagem-erro">O nome é obrigatório.</span>
                        </div>

                        <!-- Campo E-mail (Obrigatório e Validação de Formato) -->
                        <div class="form-grupo">
                            <label for="email">E-mail:</label>
                            <input type="email" id="email" name="email" required>
                            <span id="erro-email" class="mensagem-erro">Por favor, insira um e-mail válido.</span>
                        </div>

                        <!-- Campo Mensagem (Obrigatório) -->
                        <div class="form-grupo">
                            <label for="mensagem">Mensagem:</label>
                            <textarea id="mensagem" name="mensagem" required></textarea>
                            <span id="erro-mensagem" class="mensagem-erro">A mensagem é obrigatória.</span>
                        </div>

                        <button type="submit" class="botao-enviar">Enviar Mensagem</button>

                        <!-- Área para exibir mensagens de status após a simulação de envio -->
                        <div id="status-mensagem" class="mensagem-alerta" style="display: none;"></div>
                    </form>
                </div>
            </div>
        </section>

    </main>

    <!-- SCRIPTS JAVASCRIPT VANILLA -->
    <script>
        // Variáveis de referência para o formulário e elementos de feedback
        const form = document.getElementById('formulario-contato');
        const statusMensagem = document.getElementById('status-mensagem');
        const navLinks = document.querySelectorAll('.nav-link');
        
        /**
         * Função para validar um endereço de e-mail.
         * @param {string} email - O endereço de e-mail a ser validado.
         * @returns {boolean} Retorna true se o e-mail for válido, false caso contrário.
         */
        function validarEmail(email) {
            // Regex simples para verificar o formato básico de e-mail
            const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return regex.test(email);
        }

        /**
         * Função principal de validação do formulário.
         * Garante que todos os campos obrigatórios sejam preenchidos e que o e-mail seja válido.
         * @param {Event} event - O objeto de evento do formulário.
         */
        function validarFormulario(event) {
            // Previne o envio padrão do formulário, permitindo a validação e simulação
            event.preventDefault(); 
            
            let valido = true;
            
            // Pega os valores dos campos
            const nome = document.getElementById('nome').value.trim();
            const email = document.getElementById('email').value.trim();
            const mensagem = document.getElementById('mensagem').value.trim();

            // Reseta todas as mensagens de erro
            document.querySelectorAll('.mensagem-erro').forEach(el => el.style.display = 'none');
            statusMensagem.style.display = 'none';

            // 1. Validação do Nome
            if (nome === "") {
                document.getElementById('erro-nome').style.display = 'block';
                valido = false;
            }

            // 2. Validação do E-mail
            if (email === "") {
                document.getElementById('erro-email').textContent = 'O e-mail é obrigatório.';
                document.getElementById('erro-email').style.display = 'block';
                valido = false;
            } else if (!validarEmail(email)) {
                document.getElementById('erro-email').textContent = 'Por favor, insira um e-mail válido (ex: seuemail@dominio.com).';
                document.getElementById('erro-email').style.display = 'block';
                valido = false;
            }
            
            // 3. Validação da Mensagem
            if (mensagem === "") {
                document.getElementById('erro-mensagem').style.display = 'block';
                valido = false;
            }

            // Se o formulário for válido, simula o envio
            if (valido) {
                simularEnvio();
            }
        }

        /**
         * Simula o processo de envio após a validação bem-sucedida.
         * Limpa o formulário e exibe uma mensagem de sucesso.
         */
        function simularEnvio() {
            // Simulação de envio de dados (poderia ser uma chamada fetch() real)
            console.log('Dados simulados enviados:', {
                nome: document.getElementById('nome').value.trim(),
                email: document.getElementById('email').value.trim(),
                mensagem: document.getElementById('mensagem').value.trim()
            });

            // Exibe mensagem de sucesso
            statusMensagem.className = 'mensagem-alerta alerta-sucesso';
            statusMensagem.textContent = 'Mensagem enviada com sucesso! Em breve, Marcos Alberto Viana Roque entrará em contato.';
            statusMensagem.style.display = 'block';
            
            // Limpa o formulário após o envio simulado
            form.reset();
        }

        // Adiciona o listener de evento para o formulário
        form.addEventListener('submit', validarFormulario);

        /**
         * Função para atualizar o destaque do link ativo no menu de navegação
         * com base na seção visível.
         */
        function atualizarLinkAtivo() {
            const sections = document.querySelectorAll('.secao');
            let scrollY = window.pageYOffset;

            sections.forEach(current => {
                const sectionHeight = current.offsetHeight;
                const sectionTop = current.offsetTop - 70; // 70px para compensar o cabeçalho fixo
                const sectionId = current.getAttribute('id');

                // Verifica qual seção está mais visível na viewport
                if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight) {
                    navLinks.forEach(link => {
                        link.classList.remove('ativo');
                        if (link.getAttribute('href') === `#${sectionId}`) {
                            link.classList.add('ativo'); // Adiciona a classe 'ativo'
                        }
                    });
                }
            });
        }

        // Adiciona listeners para rolagem e load da página
        window.addEventListener('scroll', atualizarLinkAtivo);
        window.addEventListener('load', atualizarLinkAtivo); // Define o link ativo ao carregar
        
        // Garante que a primeira seção ('Sobre Mim') esteja ativa ao carregar
        document.addEventListener('DOMContentLoaded', () => {
            const firstLink = document.querySelector('.nav-link[href="#sobre"]');
            if (firstLink) {
                firstLink.classList.add('ativo');
            }
        });
    </script>
    <!-- Fim dos scripts JavaScript -->

</body>
</html>
