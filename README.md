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
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #1a2a6c);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 500px;
            padding: 30px;
            margin: 20px auto;
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
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .logo i {
            font-size: 50px;
            color: white;
        }
        
        h1 {
            color: #333;
            font-size: 28px;
            margin-bottom: 25px;
            line-height: 1.4;
        }
        
        .warning {
            background-color: #ffeb3b;
            border-radius: 15px;
            padding: 20px;
            margin: 25px 0;
            text-align: left;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
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
            color: #ff9800;
            margin-right: 10px;
        }
        
        .warning-header h2 {
            color: #e65100;
            font-size: 20px;
        }
        
        .warning-content {
            color: #333;
            font-size: 16px;
            line-height: 1.6;
        }
        
        .warning-content p {
            margin-bottom: 10px;
        }
        
        .highlight {
            background-color: #fff9c4;
            padding: 5px 8px;
            border-radius: 5px;
            font-weight: bold;
            color: #e65100;
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
            box-shadow: 0 8px 20px rgba(18, 140, 126, 0.4);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }
        
        .whatsapp-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(18, 140, 126, 0.6);
        }
        
        .whatsapp-btn i {
            font-size: 32px;
        }
        
        .instructions {
            background-color: #f5f5f5;
            border-radius: 15px;
            padding: 20px;
            margin-top: 30px;
            text-align: left;
        }
        
        .instructions h3 {
            color: #128C7E;
            font-size: 20px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .instructions ol {
            padding-left: 20px;
            color: #555;
            line-height: 1.8;
        }
        
        .instructions li {
            margin-bottom: 12px;
        }
        
        .instructions li span {
            font-weight: bold;
            color: #128C7E;
        }
        
        footer {
            margin-top: 20px;
            color: rgba(255, 255, 255, 0.8);
            font-size: 14px;
            width: 100%;
            max-width: 500px;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
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
        }
    </style>
</head>
<body>
    <div class="container">
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
                <p>Você está acessando nosso site através de um navegador embutido (como do Facebook, Instagram ou outro aplicativo).</p>
                <p>Para uma melhor experiência e para que o WhatsApp funcione corretamente:</p>
                <p>1. Clique nos <span class="highlight">três pontinhos</span> (...) no canto superior direito</p>
                <p>2. Selecione a opção <span class="highlight">"Abrir no navegador"</span> ou <span class="highlight">"Abrir no Chrome/Safari"</span></p>
                <p>Assim você poderá falar conosco sem problemas!</p>
            </div>
        </div>
        
        <a href="https://wa.link/tcwm02" id="whatsappLink" class="whatsapp-btn pulse">
            <i class="fab fa-whatsapp"></i>
            Clique para falar conosco
        </a>
        
        <div class="instructions">
            <h3><i class="fas fa-info-circle"></i> Como funciona:</h3>
            <ol>
                <li><span>1.</span> Clique no botão verde acima</li>
                <li><span>2.</span> Você será direcionado para nosso WhatsApp</li>
                <li><span>3.</span> Envie sua mensagem e responderemos rapidamente</li>
                <li><span>4.</span> Atendemos de segunda a sábado, das 9h às 18h</li>
            </ol>
        </div>
    </div>
    
    <footer>
        © 2023 - Todos os direitos reservados
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const whatsappLink = document.getElementById('whatsappLink');
            const warning = document.getElementById('embeddedWarning');
            
            // Função para detectar navegadores embutidos (Facebook, Instagram, etc)
            function isEmbeddedBrowser() {
                const userAgent = navigator.userAgent || navigator.vendor || window.opera;
                
                // Verificar se é Facebook, Instagram, Twitter, etc.
                return /FBAN|FBAV|Instagram|Twitter/i.test(userAgent);
            }
            
            // Mostrar aviso se for navegador embutido
            if (isEmbeddedBrowser()) {
                warning.classList.add('active');
                
                // Tentar abrir no navegador externo quando clicar no botão
                whatsappLink.addEventListener('click', function(e) {
                    e.preventDefault();
                    alert("Por favor, abra esta página no seu navegador (Chrome, Safari, etc) para acessar o WhatsApp corretamente.");
                });
            }
        });
    </script>
</body>
</html>
