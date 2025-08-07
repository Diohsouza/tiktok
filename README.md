<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fale Conosco pelo WhatsApp</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            transition: all 0.3s ease;
        }
        
        body {
            background: linear-gradient(135deg, #010101, #121212, #2a2a2a);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow-x: hidden;
        }
        
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, rgba(0, 230, 118, 0.1) 0%, transparent 70%);
            z-index: -1;
        }
        
        .container {
            background: rgba(25, 25, 25, 0.95);
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5), 0 0 15px rgba(0, 230, 118, 0.3);
            width: 100%;
            max-width: 500px;
            padding: 30px;
            margin: 20px auto;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #00e676, #00bcd4, #3f51b5);
            border-radius: 25px 25px 0 0;
        }
        
        .tiktok-warning {
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 100;
            padding: 20px;
            text-align: center;
        }
        
        .tiktok-box {
            background: linear-gradient(135deg, #121212, #000);
            border-radius: 20px;
            padding: 30px;
            max-width: 90%;
            width: 400px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 0 2px #00e676;
            position: relative;
        }
        
        .tiktok-icon {
            font-size: 50px;
            color: #fff;
            margin-bottom: 20px;
            text-shadow: 0 0 15px #00e676;
        }
        
        .tiktok-box h2 {
            color: #00e676;
            font-size: 24px;
            margin-bottom: 20px;
        }
        
        .tiktok-box p {
            color: #ddd;
            font-size: 16px;
            line-height: 1.6;
            margin-bottom: 30px;
        }
        
        .open-btn {
            background: linear-gradient(135deg, #00e676, #00b0ff);
            color: #000;
            border: none;
            font-size: 20px;
            font-weight: bold;
            padding: 15px 40px;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0, 230, 118, 0.4);
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        
        .open-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 230, 118, 0.6);
        }
        
        .logo {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, #25D366, #128C7E);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3), 0 0 20px rgba(37, 211, 102, 0.4);
        }
        
        .logo i {
            font-size: 50px;
            color: white;
        }
        
        h1 {
            color: #fff;
            font-size: 28px;
            margin-bottom: 25px;
            line-height: 1.4;
            text-shadow: 0 0 10px rgba(0, 230, 118, 0.5);
        }
        
        .warning {
            background: rgba(255, 193, 7, 0.15);
            border-radius: 15px;
            padding: 20px;
            margin: 25px 0;
            text-align: left;
            border: 1px solid rgba(255, 193, 7, 0.3);
            backdrop-filter: blur(5px);
            display: none;
        }
        
        .warning.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        .warning-header {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
        }
        
        .warning-header i {
            font-size: 24px;
            color: #ffc107;
            margin-right: 10px;
            text-shadow: 0 0 10px rgba(255, 193, 7, 0.5);
        }
        
        .warning-header h2 {
            color: #ffc107;
            font-size: 20px;
        }
        
        .warning-content {
            color: #eee;
            font-size: 16px;
            line-height: 1.6;
        }
        
        .warning-content p {
            margin-bottom: 10px;
        }
        
        .highlight {
            background: rgba(255, 255, 255, 0.1);
            padding: 3px 8px;
            border-radius: 5px;
            font-weight: bold;
            color: #ffc107;
            display: inline-block;
            margin: 3px 0;
            border: 1px solid rgba(255, 193, 7, 0.3);
        }
        
        .whatsapp-btn {
            display: block;
            background: linear-gradient(135deg, #25D366, #128C7E);
            color: white;
            text-decoration: none;
            font-size: 22px;
            font-weight: bold;
            padding: 18px 25px;
            border-radius: 50px;
            margin: 30px auto;
            width: 90%;
            max-width: 350px;
            box-shadow: 0 8px 20px rgba(18, 140, 126, 0.4), 0 0 15px rgba(37, 211, 102, 0.5);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            position: relative;
            overflow: hidden;
        }
        
        .whatsapp-btn::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -60%;
            width: 20px;
            height: 200%;
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(25deg);
            transition: all 0.8s;
        }
        
        .whatsapp-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(18, 140, 126, 0.6), 0 0 25px rgba(37, 211, 102, 0.7);
        }
        
        .whatsapp-btn:hover::before {
            left: 120%;
        }
        
        .whatsapp-btn i {
            font-size: 32px;
        }
        
        .instructions {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-top: 30px;
            text-align: left;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .instructions h3 {
            color: #00e676;
            font-size: 20px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions ol {
            padding-left: 20px;
            color: #ddd;
            line-height: 1.8;
        }
        
        .instructions li {
            margin-bottom: 12px;
            position: relative;
        }
        
        .instructions li::before {
            content: '';
            position: absolute;
            left: -20px;
            top: 8px;
            width: 8px;
            height: 8px;
            background: #00e676;
            border-radius: 50%;
        }
        
        footer {
            margin-top: 20px;
            color: rgba(255, 255, 255, 0.6);
            font-size: 14px;
            width: 100%;
            max-width: 500px;
            text-align: center;
        }
        
        .iphone-demo {
            display: flex;
            justify-content: center;
            margin: 15px 0;
        }
        
        .iphone-demo img {
            max-width: 80%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(0, 230, 118, 0.7); }
            70% { transform: scale(1.02); box-shadow: 0 0 0 15px rgba(0, 230, 118, 0); }
            100% { transform: scale(1); box-shadow: 0 0 0 0 rgba(0, 230, 118, 0); }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            .whatsapp-btn {
                font-size: 20px;
                padding: 16px 20px;
            }
            
            .tiktok-box {
                padding: 20px;
            }
            
            .tiktok-box h2 {
                font-size: 22px;
            }
        }
    </style>
</head>
<body>
    <!-- Aviso inicial para TikTok -->
    <div class="tiktok-warning" id="tiktokWarning">
        <div class="tiktok-box">
            <div class="tiktok-icon">
                <i class="fab fa-tiktok"></i>
            </div>
            <h2>Você está saindo do TikTok</h2>
            <p>Você está acessando um site externo. Por favor, confirme que deseja continuar.</p>
            <button class="open-btn pulse" id="openBtn">
                <i class="fas fa-external-link-alt"></i> Abrir
            </button>
        </div>
    </div>
    
    <!-- Conteúdo principal -->
    <div class="container" id="mainContent" style="display:none;">
        <div class="logo">
            <i class="fab fa-whatsapp"></i>
        </div>
        
        <h1>Fale diretamente com a nossa equipe pelo WhatsApp</h1>
        
        <div class="warning" id="embeddedWarning">
            <div class="warning-header">
                <i class="fas fa-exclamation-triangle"></i>
                <h2>ATENÇÃO: Navegador Embutido Detectado</h2>
            </div>
            <div class="warning-content">
                <p>Você está acessando nosso site através do navegador embutido do TikTok.</p>
                <p>Para uma melhor experiência e para que o WhatsApp funcione corretamente:</p>
                <p>1. Clique nos <span class="highlight">três pontinhos</span> (...) no canto superior direito</p>
                <p>2. Selecione a opção <span class="highlight">"Abrir no navegador"</span> ou <span class="highlight">"Abrir no Safari"</span></p>
                <p>Assim você poderá falar conosco sem problemas!</p>
                
                <div class="iphone-demo">
                    <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNDAiIGhlaWdodD0iNDgwIiB2aWV3Qm94PSIwIDAgMjQwIDQ4MCIgZmlsbD0ibm9uZSI+PHJlY3QgeD0iMTAiIHk9IjEwIiB3aWR0aD0iMjIwIiBoZWlnaHQ9IjQ2MCIgcng9IjQwIiByeT0iNDAiIGZpbGw9IiMyQTJBMkEiIHN0cm9rZT0iIzVBNUE1QSIgc3Ryb2tlLXdpZHRoPSIyIi8+PHBhdGggZD0iTTEyMCA3NUgxMzAiIHN0cm9rZT0iI0ZGRiIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiLz48Y2lyY2xlIGN4PSIxMjAiIGN5PSIxMjAiIHI9IjYwIiBmaWxsPSIjMjVDMzY2Ii8+PHBhdGggZD0iTTE0MCAxMjBMMTYwIDE0MEwxNDAgMTYwTDEyMCAxNDBMMTQwIDEyMFoiIGZpbGw9IiNGRkYiLz48cmVjdCB4PSI0MCIgeT0iMjAwIiB3aWR0aD0iMTYwIiBoZWlnaHQ9IjIwMCIgcng9IjEwIiByeT0iMTAiIGZpbGw9IiMzMzMiLz48cGF0aCBkPSJNNTAgMzA1SDE5MCIgc3Ryb2tlPSIjNjY2IiBzdHJva2Utd2lkdGg9IjIiLz48cGF0aCBkPSJNNjAgMzM1SDE4MCIgc3Ryb2tlPSIjNjY2IiBzdHJva2Utd2lkdGg9IjIiLz48cGF0aCBkPSJNNzAgMzY1SDE3MCIgc3Ryb2tlPSIjNjY2IiBzdHJva2Utd2lkdGg9IjIiLz48cGF0aCBkPSJNMTU1IDM5NUg4NSIgc3Ryb2tlPSIjRkZGIiBzdHJva2Utd2lkdGg9IjMiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPjwvc3ZnPg==" alt="Demonstração iPhone">
                </div>
            </div>
        </div>
        
        <a href="https://wa.link/tcwm02" id="whatsappLink" class="whatsapp-btn">
            <i class="fab fa-whatsapp"></i>
            Clique para falar conosco
        </a>
        
        <div class="instructions">
            <h3><i class="fas fa-info-circle"></i> Como funciona:</h3>
            <ol>
                <li>Clique no botão verde acima</li>
                <li>Você será direcionado para nosso WhatsApp</li>
                <li>Envie sua mensagem e responderemos rapidamente</li>
                <li>Atendemos de segunda a sábado, das 9h às 18h</li>
            </ol>
        </div>
    </div>
    
    <footer>
        © 2023 - Todos os direitos reservados
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const tiktokWarning = document.getElementById('tiktokWarning');
            const mainContent = document.getElementById('mainContent');
            const openBtn = document.getElementById('openBtn');
            const whatsappLink = document.getElementById('whatsappLink');
            const warning = document.getElementById('embeddedWarning');
            
            // Mostrar aviso inicial para TikTok
            tiktokWarning.style.display = 'flex';
            
            // Botão "Abrir" - redireciona para a mesma página (simulando abertura no navegador embutido)
            openBtn.addEventListener('click', function() {
                tiktokWarning.style.display = 'none';
                mainContent.style.display = 'block';
            });
            
            // Função para detectar navegadores embutidos (TikTok, Instagram, etc)
            function isEmbeddedBrowser() {
                const userAgent = navigator.userAgent || navigator.vendor || window.opera;
                
                // Verificar se é TikTok ou outros navegadores embutidos
                return /tiktok|musical_ly|fb_iab|fbav|instagram|twitter/i.test(userAgent);
            }
            
            // Mostrar aviso se for navegador embutido
            if (isEmbeddedBrowser()) {
                warning.classList.add('active');
                
                // Tentar abrir no navegador externo quando clicar no botão
                whatsappLink.addEventListener('click', function(e) {
                    e.preventDefault();
                    alert("Por favor, siga as instruções acima para abrir no navegador externo. Clique nos três pontinhos e selecione 'Abrir no navegador' para acessar o WhatsApp corretamente.");
                });
            }
        });
    </script>
</body>
</html>
