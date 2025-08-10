<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Excursão Hopi Hari - ETOPS</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #0a0a0a;
            color: #ffffff;
            background-image: url('https://i.imgur.com/your-image.jpg');
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
            line-height: 1.6;
        }
        
        .content-wrapper {
            background-color: rgba(0, 0, 0, 0.85);
            border-radius: 15px;
            padding: 30px;
            backdrop-filter: blur(8px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4CAF50;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 10px;
            color: #4CAF50;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        h1, h2 {
            color: #4CAF50;
        }
        
        .participant-list {
            margin-bottom: 40px;
            background-color: rgba(20, 20, 20, 0.7);
            padding: 25px;
            border-radius: 10px;
            border: 1px solid #333;
        }
        
        .participant-item {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
            padding: 10px;
            background-color: rgba(30, 30, 30, 0.7);
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .participant-item:hover {
            background-color: rgba(40, 40, 40, 0.7);
        }
        
        .participant-number {
            width: 35px;
            margin-right: 15px;
            font-weight: bold;
            color: #4CAF50;
            font-size: 16px;
        }
        
        .name-input {
            flex-grow: 1;
            padding: 10px;
            margin-right: 15px;
            border: 1px solid #444;
            border-radius: 6px;
            background-color: #222;
            color: #fff;
            font-size: 14px;
        }
        
        .name-display {
            flex-grow: 1;
            margin-right: 15px;
            padding: 8px;
            color: #fff;
            font-weight: bold;
        }
        
        .confirmation-input {
            width: 100px;
            margin-right: 15px;
            padding: 10px;
            border: 1px solid #444;
            border-radius: 6px;
            background-color: #222;
            color: #fff;
            font-size: 14px;
        }
        
        .confirmation-button {
            padding: 10px 20px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .confirmation-button:hover {
            background-color: #45a049;
        }
        
        .confirmed {
            color: #4CAF50;
            font-weight: bold;
            margin-left: 15px;
            font-size: 16px;
        }
        
        .trip-info {
            background-color: rgba(20, 20, 20, 0.7);
            padding: 30px;
            border-radius: 10px;
            border: 1px solid #333;
            margin-bottom: 30px;
        }
        
        .discord-link {
            margin: 25px auto;
            padding: 15px;
            background-color: #7289DA;
            color: white;
            text-align: center;
            border-radius: 8px;
            text-decoration: none;
            display: block;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s;
            max-width: 500px;
        }
        
        .discord-link:hover {
            background-color: #5a6fb3;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .emoji {
            font-size: 1.3em;
            margin: 0 3px;
        }
        
        .highlight {
            background-color: rgba(255, 235, 59, 0.3);
            padding: 3px 6px;
            border-radius: 4px;
            color: #FFEB3B;
            font-weight: bold;
        }
        
        .alert-box {
            background-color: rgba(255, 152, 0, 0.2);
            border-left: 4px solid #FF9800;
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .payment-info {
            background-color: rgba(76, 175, 80, 0.2);
            border-left: 4px solid #4CAF50;
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 8px 8px 0;
        }
        
        .security-info {
            background-color: rgba(33, 150, 243, 0.2);
            border-left: 4px solid #2196F3;
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 8px 8px 0;
        }
        
        input:disabled {
            background-color: #333;
            color: #999;
            cursor: not-allowed;
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #333;
            color: #aaa;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="content-wrapper">
        <div class="header">
            <div class="logo">Excursão Hopi Hari</div>
            <h1>Centro Educacional ETOPS</h1>
            <p>Um passeio organizado por alunos para alunos</p>
        </div>

        <div class="participant-list">
            <h2>📋 Lista de Participantes</h2>
            <p>Preencha seu nome e o código de confirmação para garantir sua vaga:</p>
            
            <div id="participants-container">
                <!-- Lista de participantes será gerada aqui -->
            </div>
        </div>

        <div class="trip-info">
            <div class="alert-box">
                <h2>🚨 Atenção, galera do ETOPS!</h2>
                <p>Este site foi criado exclusivamente para organizar nossa excursão para o Hopi Hari, já que a escola não oferece suporte para esse tipo de evento. Esta organização está sendo feita por fora da escola, somente entre colegas, com o objetivo de proporcionar um rolê legal para quem quer participar.</p>
                <p>Não estamos aqui para criticar a escola, e sim para garantir que a galera tenha uma experiência única e divertida! 🎢</p>
            </div>

            <h2>📌 Como vai funcionar?</h2>
            <p>O objetivo é fazer tudo de forma organizada e com total transparência. Aqui vamos compartilhar todas as informações:</p>
            <ul>
                <li>📍 Local de encontro</li>
                <li>⏰ Horário da viagem</li>
                <li>🏢 Agência responsável</li>
                <li>📅 Data do passeio</li>
                <li>💲 Valores e formas de pagamento</li>
            </ul>
            <p>Tudo será atualizado regularmente para que você possa se programar!</p>

            <div class="payment-info">
                <h2>💳 Sobre o pagamento</h2>
                <p>Fiquem tranquilos que o pagamento será feito <strong>diretamente para a agência de viagens</strong>, sem passar por ninguém da nossa organização ou professores. Tudo direto e seguro, sem intermediários!</p>
            </div>

            <div class="security-info">
                <h2>🔐 Segurança</h2>
                <p>A agência vai cuidar de todo o transporte e da logística da viagem, desde nosso embarque até o retorno. O local e horário exatos serão divulgados com antecedência para que ninguém fique perdido.</p>
                <p>Tudo pensado para garantir um passeio seguro e bem organizado!</p>
            </div>

            <h2>📢 Importante!</h2>
            <p>Todos os detalhes e o código de confirmação serão compartilhados no nosso grupo exclusivo do Discord:</p>

            <a href="https://discord.gg/3FhMgaYt" class="discord-link">
                <span class="emoji">💥</span> ENTRAR NO DISCORD AGORA <span class="emoji">💥</span>
            </a>

            <p style="text-align: center; font-weight: bold; font-size: 1.2em; margin-top: 30px;">
                <span class="emoji">🎡</span> Vai ser um dia incrível! Nos vemos no Hopi Hari! <span class="emoji">🎡</span>
            </p>
        </div>

        <div class="footer">
            <p>Organização independente de alunos do ETOPS • Não vinculado à escola</p>
            <p>© 2025 - Todos os direitos reservados</p>
        </div>
    </div>

    <script>
        // Gerar lista de 60 participantes
        const participantsContainer = document.getElementById('participants-container');
        
        for (let i = 1; i <= 60; i++) {
            const participantDiv = document.createElement('div');
            participantDiv.className = 'participant-item';
            participantDiv.innerHTML = `
                <div class="participant-number">${i}.</div>
                <input type="text" class="name-input" placeholder="Seu nome completo">
                <input type="text" class="confirmation-input" placeholder="Código" maxlength="6" disabled>
                <button class="confirmation-button" disabled>Confirmar</button>
                <span class="confirmed" style="display:none;">✓ Confirmado</span>
            `;
            participantsContainer.appendChild(participantDiv);
        }

        // Habilitar campo de código quando nome for preenchido
        document.querySelectorAll('.name-input').forEach(input => {
            input.addEventListener('input', function() {
                const participantItem = this.closest('.participant-item');
                const codeInput = participantItem.querySelector('.confirmation-input');
                const confirmButton = participantItem.querySelector('.confirmation-button');
                
                if (this.value.trim() !== '') {
                    codeInput.disabled = false;
                    confirmButton.disabled = false;
                } else {
                    codeInput.disabled = true;
                    confirmButton.disabled = true;
                }
            });
        });

        // Adicionar eventos aos botões de confirmação
        document.querySelectorAll('.confirmation-button').forEach(button => {
            button.addEventListener('click', function() {
                const participantItem = this.closest('.participant-item');
                const nameInput = participantItem.querySelector('.name-input');
                const codeInput = participantItem.querySelector('.confirmation-input');
                const confirmedSpan = participantItem.querySelector('.confirmed');
                
                if (codeInput.value === '211234') {
                    // Travar todos os campos
                    nameInput.disabled = true;
                    codeInput.disabled = true;
                    this.disabled = true;
                    
                    // Mostrar confirmação
                    confirmedSpan.style.display = 'inline';
                    
                    // Substituir input por texto
                    const nameDisplay = document.createElement('div');
                    nameDisplay.className = 'name-display';
                    nameDisplay.textContent = nameInput.value;
                    nameInput.replaceWith(nameDisplay);
                    
                    // Feedback visual
                    participantItem.style.backgroundColor = 'rgba(76, 175, 80, 0.2)';
                    participantItem.style.borderLeft = '4px solid #4CAF50';
                } else {
                    alert('Código incorreto! O código de confirmação será fornecido no Discord.');
                }
            });
        });
    </script>
</body>
</html>
