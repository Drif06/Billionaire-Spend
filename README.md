<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-lang-key="gameTitle">Billionaire Spend Game</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Link to external CSS file -->
    <link rel="stylesheet" href="style.css">
</head>
<body class="bg-gray-900 text-gray-100 p-4">

    <!-- Start Screen -->
    <div id="start-screen" class="game-container bg-gray-800 p-6 sm:p-8 rounded-xl shadow-2xl w-full max-w-2xl flex flex-col items-center space-y-6">
        <h1 class="text-3xl sm:text-4xl md:text-5xl font-extrabold text-center text-indigo-400 mb-4" data-lang-key="gameTitle">
            Billionaire Spend Game
        </h1>
        <p class="text-xl sm:text-2xl text-gray-300 text-center mb-6" data-lang-key="selectBusinessmanPrompt">
            खेलने के लिए एक व्यवसायी चुनें (Select a businessman to play)
        </p>

        <div class="language-selection mb-4 w-full flex flex-col sm:flex-row items-center justify-center space-y-2 sm:space-y-0 sm:space-x-4">
            <label for="language-select" class="text-lg text-gray-300" data-lang-key="selectLanguage">भाषा चुनें:</label>
            <select id="language-select" class="select-option">
                <option value="en">English</option>
                <option value="hi">हिंदी</option>
                <option value="ta">தமிழ்</option>
                <option value="te">తెలుగు</option>
            </select>
        </div>

        <div class="businessman-selection mb-8 w-full flex flex-col sm:flex-row items-center justify-center space-y-4 sm:space-y-0 sm:space-x-6">
            <select id="start-businessman-select" class="select-option text-center">
                <!-- Options will be populated by JavaScript -->
            </select>
            <img id="start-businessman-image" class="businessman-image" src="https://placehold.co/80x80/2d3748/e2e8f0?text=Ambani" alt="Businessman Image">
        </div>

        <button id="start-game-button" class="start-button" data-lang-key="startGameButton">
            खेल शुरू करें (Start Game)
        </button>
    </div>

    <!-- Main Game Container (hidden initially) -->
    <div id="game-container" class="game-container bg-gray-800 p-6 sm:p-8 rounded-xl shadow-2xl w-full max-w-4xl flex-col items-center space-y-6 hidden">
        <h1 class="text-3xl sm:text-4xl md:text-5xl font-extrabold text-center text-indigo-400 mb-4" data-lang-key="gameTitle">
            Billionaire Spend Game
        </h1>

        <div class="money-display-section text-center mb-6 w-full">
            <div class="money-display mb-2">
                <p class="text-lg sm:text-xl text-gray-400" data-lang-key="currentBalance">वर्तमान शेष (Current Balance):</p>
                <p id="current-money" class="money-display">$100,000,000,000</p>
            </div>
            <div class="total-spent-display mb-2">
                <p class="text-sm sm:text-base text-gray-400" data-lang-key="totalSpent">कुल खर्च (Total Spent):</p>
                <p id="total-spent" class="total-spent-display">$0</p>
            </div>
            <div class="total-bill-display">
                <p class="text-sm sm:text-base text-gray-400" data-lang-key="totalBill">कुल बिल (खरीदी गई वस्तुओं का मूल्य) (Total Bill (Value of Owned Items)):</p>
                <p id="total-bill" class="total-bill-display">$0</p>
            </div>
        </div>

        <div class="items-container w-full max-h-[60vh] overflow-y-auto pr-2">
            <div id="game-items" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Game items will be rendered here by JavaScript -->
            </div>
        </div>

        <button id="reset-game" class="reset-button mt-6" data-lang-key="resetGameButton">
            गेम रीसेट करें (Reset Game)
        </button>
    </div>

    <!-- Link to external JavaScript file -->
    <script src="script.js"></script>
</body>
</html>
