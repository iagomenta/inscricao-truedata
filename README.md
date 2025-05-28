<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inscrição Campeonato Valorant - Truedata e-Sports</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Teko:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f1923 0%, #1c2e3a 70%, #111827 100%);
            color: #e5e7eb; /* Light gray text */
        }
        .font-teko {
            font-family: 'Teko', sans-serif;
        }
        .valorant-red {
            color: #ff4655;
        }
        .bg-valorant-red {
            background-color: #ff4655;
        }
        .border-valorant-red {
            border-color: #ff4655;
        }
        .form-input {
            background-color: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: #e5e7eb;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }
        .form-input:focus {
            border-color: #ff4655;
            box-shadow: 0 0 0 3px rgba(255, 70, 85, 0.3);
            outline: none;
        }
        .form-label {
            color: #cbd5e1; /* Lighter gray for labels */
        }
        .btn-submit {
            background-color: #ff4655;
            transition: background-color 0.3s ease, transform 0.2s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1), 0 0 10px rgba(255,70,85,0.5);
        }
        .btn-submit:hover {
            background-color: #e03c4a;
            transform: translateY(-2px);
        }
        .btn-submit:active {
            transform: translateY(0px);
        }
        .logo-glow {
            filter: drop-shadow(0 0 8px rgba(255, 70, 85, 0.6)) drop-shadow(0 0 15px rgba(255, 70, 85, 0.4));
        }
        #confirmationMessage {
            background-color: rgba(70, 255, 150, 0.1);
            border-left: 4px solid #46ff96;
            color: #d1fae5;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center pt-12 sm:pt-16 lg:pt-20 p-4 sm:p-6 lg:p-8">

    <div class="w-full max-w-2xl mx-auto text-center mb-8">
        <img src="Logo-Full.png" alt="Logo Truedata e-Sports"
             class="mx-auto w-32 h-auto sm:w-40 md:w-48 logo-glow mb-6"
             onerror="this.onerror=null; this.src= Logo-Full.png'">
        <h1 class="font-teko text-4xl sm:text-5xl md:text-6xl font-bold uppercase valorant-red tracking-wider">
            Inscrição no Campeonato
        </h1>
        <p class="text-gray-400 text-md sm:text-lg mt-2">Preencha os campos abaixo para registrar sua equipe!</p>
    </div>

    <form id="registrationForm" class="w-full max-w-2xl bg-gray-800 bg-opacity-40 p-6 sm:p-8 md:p-10 rounded-xl shadow-2xl border border-gray-700">
        <div id="formFields">
            <fieldset class="mb-8">
                <legend class="font-teko text-2xl sm:text-3xl valorant-red mb-4 border-b-2 border-valorant-red pb-2">Informações da Equipe</legend>
                <div class="mb-4">
                    <label for="teamName" class="block form-label text-sm font-bold mb-2">Nome da Equipe:</label>
                    <input type="text" id="teamName" name="teamName" class="form-input w-full px-3 py-2 rounded-md focus:outline-none" required placeholder="Ex: Dragões Alados">
                </div>
            </fieldset>

            <fieldset class="mb-8">
                <legend class="font-teko text-2xl sm:text-3xl valorant-red mb-4 border-b-2 border-valorant-red pb-2">Capitão da Equipe</legend>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <label for="captainName" class="block form-label text-sm font-bold mb-2">Nome Completo do Capitão:</label>
                        <input type="text" id="captainName" name="captainName" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Seu Nome Aqui">
                    </div>
                    <div>
                        <label for="captainIgn" class="block form-label text-sm font-bold mb-2">Nickname (IGN) do Capitão no Valorant:</label>
                        <input type="text" id="captainIgn" name="captainIgn" class="form-input w-full px-3 py-2 rounded-md" required placeholder="SeuNick#TAG">
                    </div>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <label for="captainEmail" class="block form-label text-sm font-bold mb-2">E-mail do Capitão:</label>
                        <input type="email" id="captainEmail" name="captainEmail" class="form-input w-full px-3 py-2 rounded-md" required placeholder="email@exemplo.com">
                    </div>
                    <div>
                        <label for="captainDiscord" class="block form-label text-sm font-bold mb-2">Discord do Capitão (Usuário#TAG):</label>
                        <input type="text" id="captainDiscord" name="captainDiscord" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Usuario#1234">
                    </div>
                </div>
            </fieldset>

            <fieldset class="mb-8">
                <legend class="font-teko text-2xl sm:text-3xl valorant-red mb-4 border-b-2 border-valorant-red pb-2">Jogadores (Nicknames no Valorant)</legend>
                <p class="text-gray-400 text-xs mb-4">Inclua a TAG (Ex: Jogador#BR1). Mínimo 5 jogadores.</p>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label for="player2" class="block form-label text-sm font-bold mb-2">Jogador 2 (Titular):</label>
                        <input type="text" id="player2" name="player2" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Jogador2#TAG">
                    </div>
                    <div>
                        <label for="player3" class="block form-label text-sm font-bold mb-2">Jogador 3 (Titular):</label>
                        <input type="text" id="player3" name="player3" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Jogador3#TAG">
                    </div>
                    <div>
                        <label for="player4" class="block form-label text-sm font-bold mb-2">Jogador 4 (Titular):</label>
                        <input type="text" id="player4" name="player4" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Jogador4#TAG">
                    </div>
                    <div>
                        <label for="player5" class="block form-label text-sm font-bold mb-2">Jogador 5 (Titular):</label>
                        <input type="text" id="player5" name="player5" class="form-input w-full px-3 py-2 rounded-md" required placeholder="Jogador5#TAG">
                    </div>
                    <div>
                        <label for="substitutePlayer" class="block form-label text-sm font-bold mb-2">Jogador Reserva (Opcional):</label>
                        <input type="text" id="substitutePlayer" name="substitutePlayer" class="form-input w-full px-3 py-2 rounded-md" placeholder="Reserva#TAG (Opcional)">
                    </div>
                </div>
            </fieldset>

            <div class="mb-6">
                <label class="flex items-center">
                    <input type="checkbox" id="terms" name="terms" class="form-checkbox h-5 w-5 text-valorant-red bg-gray-700 border-gray-600 rounded focus:ring-valorant-red focus:ring-offset-gray-800" required>
                    <span class="ml-2 text-sm text-gray-300">Li e concordo com os <a href="#" class="underline valorant-red hover:text-red-400">termos e regulamento</a> do campeonato.</span>
                </label>
            </div>

            <div class="text-center">
                <button type="submit" class="btn-submit text-white font-bold py-3 px-8 rounded-lg text-lg shadow-md hover:shadow-lg focus:outline-none w-full sm:w-auto">
                    Enviar Inscrição 🚀
                </button>
            </div>
        </div>

        <div id="confirmationMessage" class="mt-6 p-4 rounded-lg text-center" style="display: none;">
            <h3 class="font-teko text-2xl text-green-300">Inscrição Enviada com Sucesso!</h3>
            <p class="text-gray-200">Obrigado por inscrever sua equipe, <strong id="confirmTeamName"></strong>!</p>
            <p class="text-gray-300 text-sm mt-2">Entraremos em contato em breve com mais informações.</p>
            <button type="button" id="newRegistrationButton" class="mt-4 bg-gray-600 hover:bg-gray-500 text-white font-semibold py-2 px-4 rounded-md text-sm">
                Nova Inscrição
            </button>
        </div>
    </form>

    <footer class="mt-12 text-center text-gray-500 text-sm">
        <p>&copy; <span id="currentYear"></span> Truedata e-Sports. Todos os direitos reservados.</p>
        <p>Campeonato de Valorant</p>
    </footer>

    <script>
        const registrationForm = document.getElementById('registrationForm');
        const formFieldsDiv = document.getElementById('formFields');
        const confirmationMessageDiv = document.getElementById('confirmationMessage');
        const confirmTeamNameSpan = document.getElementById('confirmTeamName');
        const newRegistrationButton = document.getElementById('newRegistrationButton');

        if (registrationForm) {
            registrationForm.addEventListener('submit', function(event) {
                event.preventDefault();
                const teamNameInput = document.getElementById('teamName');
                if (teamNameInput && teamNameInput.value) {
                    confirmTeamNameSpan.textContent = teamNameInput.value;
                } else {
                    confirmTeamNameSpan.textContent = "Equipe";
                }
                formFieldsDiv.style.display = 'none';
                confirmationMessageDiv.style.display = 'block';
                confirmationMessageDiv.scrollIntoView({ behavior: 'smooth', block: 'center' });
                console.log('Formulário enviado (simulação):');
                const formData = new FormData(registrationForm);
                for (let [key, value] of formData.entries()) {
                    console.log(key, value);
                }
            });
        }

        if (newRegistrationButton) {
            newRegistrationButton.addEventListener('click', function() {
                confirmationMessageDiv.style.display = 'none';
                formFieldsDiv.style.display = 'block';
                if (registrationForm) {
                    registrationForm.reset();
                }
                registrationForm.scrollIntoView({ behavior: 'smooth', block: 'start' });
            });
        }

        const currentYearSpan = document.getElementById('currentYear');
        if (currentYearSpan) {
            currentYearSpan.textContent = new Date().getFullYear();
        }
    </script>

</body>
</html>


