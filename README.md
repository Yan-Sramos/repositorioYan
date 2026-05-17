# repositorioYan
Este repositório foi criado com o objetivo de compartilhar minhas experiências, conhecimentos e projetos na área de programação e tecnologia. Aqui você encontrará estudos, testes, exercícios e projetos desenvolvidos durante minha jornada de aprendizado, mostrando minha evolução prática e minhas habilidades ao longo do tempo.
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yan de Souza Ramos - Portfólio</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            line-height: 1.6;
            background: #0a0a0a;
            color: #e0e0e0;
            min-height: 100vh;
            overflow-x: hidden;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.2) 0%, transparent 50%);
            z-index: -1;
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(1deg); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        header {
            text-align: center;
            background: rgba(15, 15, 25, 0.9);
            padding: 3rem 2rem;
            border-radius: 25px;
            margin-bottom: 3rem;
            box-shadow: 
                0 30px 60px rgba(0,0,0,0.5),
                0 0 30px rgba(138, 43, 226, 0.2);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(138, 43, 226, 0.3);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(transparent, rgba(138, 43, 226, 0.1), transparent);
            animation: rotate 10s linear infinite;
        }

        @keyframes rotate {
            100% { transform: rotate(360deg); }
        }

        h1 {
            font-family: 'Orbitron', monospace;
            font-size: 3.5rem;
            font-weight: 900;
            background: linear-gradient(135deg, #8a2be2, #ba55d3, #9370db, #8a2be2);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
            animation: gradientShift 4s ease infinite;
            text-shadow: 0 0 30px rgba(138, 43, 226, 0.5);
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .subtitle {
            font-size: 1.4rem;
            color: #b0b0b0;
            margin-bottom: 1.5rem;
            font-weight: 300;
        }

        .faculdade {
            background: linear-gradient(135deg, #8a2be2, #ba55d3);
            color: white;
            display: inline-block;
            padding: 1rem 2rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.2rem;
            box-shadow: 0 10px 30px rgba(138, 43, 226, 0.4);
            position: relative;
            overflow: hidden;
        }

        .faculdade::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .faculdade:hover::after {
            left: 100%;
        }

        .section {
            background: rgba(20, 20, 35, 0.8);
            padding: 3rem;
            margin-bottom: 3rem;
            border-radius: 25px;
            box-shadow: 
                0 25px 50px rgba(0,0,0,0.4),
                inset 0 1px 0 rgba(255,255,255,0.1);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(138, 43, 226, 0.2);
            transition: all 0.4s ease;
            position: relative;
        }

        .section:hover {
            transform: translateY(-10px);
            box-shadow: 
                0 40px 80px rgba(138, 43, 226, 0.3),
                inset 0 1px 0 rgba(255,255,255,0.2);
            border-color: rgba(138, 43, 226, 0.5);
        }

        h2 {
            font-family: 'Orbitron', monospace;
            color: #ffffff;
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-align: center;
            position: relative;
            text-shadow: 0 0 20px rgba(138, 43, 226, 0.5);
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 5px;
            background: linear-gradient(90deg, transparent, #8a2be2, #ba55d3, transparent);
            border-radius: 3px;
            box-shadow: 0 0 20px #8a2be2;
        }

        .sobre-mim {
            text-align: center;
            font-size: 1.2rem;
            line-height: 1.9;
            color: #c0c0c0;
        }

        .projetos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
            margin-top: 2.5rem;
        }

        .projeto {
            background: rgba(30, 30, 50, 0.7);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: center;
            border: 2px solid rgba(138, 43, 226, 0.3);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .projeto::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(138, 43, 226, 0.2), transparent);
            transition: left 0.6s;
        }

        .projeto:hover::before {
            left: 100%;
        }

        .projeto:hover {
            border-color: #8a2be2;
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 30px 60px rgba(138, 43, 226, 0.4);
        }

        .tech-icon {
            font-size: 4rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #8a2be2, #ba55d3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            filter: drop-shadow(0 0 20px rgba(138, 43, 226, 0.5));
        }

        .projeto h3 {
            color: #ffffff;
            margin-bottom: 1.2rem;
            font-size: 1.6rem;
            font-family: 'Orbitron', monospace;
        }

        .projeto p {
            color: #b0b0b0;
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #8a2be2, #ba55d3);
            color: white;
            padding: 1rem 2.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 700;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            box-shadow: 0 10px 30px rgba(138, 43, 226, 0.4);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 20px 40px rgba(138, 43, 226, 0.6);
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 2.5rem;
        }

        .stat {
            background: linear-gradient(135deg, rgba(138, 43, 226, 0.2), rgba(186, 85, 211, 0.1));
            color: white;
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(138, 43, 226, 0.3);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .stat:hover {
            transform: translateY(-10px);
            border-color: #8a2be2;
            box-shadow: 0 20px 40px rgba(138, 43, 226, 0.3);
        }

        .stat i {
            font-size: 3rem;
            display: block;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #8a2be2, #ba55d3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* ✅ CORREÇÃO: Tamanhos menores para textos longos */
        .stat h3 {
            font-size: 1.8rem; /* Era 2.5rem - agora menor */
            margin-bottom: 0.5rem;
            font-family: 'Orbitron', monospace;
            line-height: 1.2;
            word-break: break-word;
        }

        .stat p {
            font-size: 0.95rem; /* Texto menor e ajustado */
            opacity: 0.9;
            line-height: 1.3;
        }

        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .container { padding: 15px; }
            .section { padding: 2rem; }
            .projetos-grid { grid-template-columns: 1fr; }
            .stat h3 { font-size: 1.6rem; }
            .stat p { font-size: 0.9rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Yan de Souza Ramos</h1>
            <p class="subtitle">Desenvolvedor em Formação</p>
            <div class="faculdade">
                <i class="fas fa-graduation-cap"></i> Engenharia de Software<br>CEUB Asa Norte
            </div>
        </header>

        <div class="section">
            <h2><i class="fas fa-user"></i> Sobre Mim</h2>
            <div class="sobre-mim">
                <p>Sou estudante de <strong>Engenharia de Software</strong> no CEUB Asa Norte. Apaixonado por programação, domino <strong>Python (Intermediário)</strong> e tenho base sólida em <strong>Java</strong>.</p>
                <p>Foco em resolver problemas reais através de código limpo e eficiente. Sempre aprendendo novas tecnologias!</p>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-code"></i> Experiências Práticas</h2>
            <div class="projetos-grid">
                <div class="projeto">
                    <div class="tech-icon">
                        <i class="fab fa-python"></i>
                    </div>
                    <h3>Projetos Python</h3>
                    <p>• Projetar programas para resolver problemas reais<br>• Uso de condições e estruturas de repetição<br>• Manipulação de listas, dicionários e arquivos<br>• Funções e programação modular<br>• Tratamento de exceções</p>
                </div>

                <div class="projeto">
                    <div class="tech-icon">
                        <i class="fab fa-java"></i>
                    </div>
                    <h3>Projetos Java</h3>
                    <p>• Programação Orientada a Objetos (POO)<br>• Classes, objetos e herança<br>• Estruturas de controle básicas<br>• Arrays e coleções simples<br>• Métodos e encapsulamento</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-chart-line"></i> Status</h2>
            <div class="stats">
                <div class="stat">
                    <i class="fas fa-project-diagram"></i>
                    <h3>+15</h3>
                    <p>Programas criados</p>
                </div>
                <div class="stat">
                    <i class="fab fa-python"></i>
                    <h3>Intermediário</h3>
                    <p>Python</p>
                </div>
                <div class="stat">
                    <i class="fab fa-java"></i>
                    <h3>Básico</h3>
                    <p>Java</p>
                </div>
                <div class="stat">
                    <i class="fas fa-brain"></i>
                    <h3>Em Progresso</h3>
                    <p>Engenharia SW</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Animações de entrada
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.section, .projeto, .stat').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94)';
            observer.observe(el);
        });

        // Efeito de digitação
        const title = document.querySelector('h1');
        const originalText = title.textContent;
        title.textContent = '';
        let i = 0;
        function typeWriter() {
            if (i < originalText.length) {
                title.textContent += originalText.charAt(i);
                i++;
                setTimeout(typeWriter, 80);
            }
        }
        setTimeout(typeWriter, 800);
    </script>
</body>
</html>
