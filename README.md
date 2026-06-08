# hardik
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Patience Test for My Bestie</title>
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <!-- Canvas Confetti Library for the grand reveal explosion -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }
        .floating-emoji {
            animation: float 3s ease-in-out infinite;
        }
        .bg-gradient-mesh {
            background-color: #df97ff;
            background-image: 
                radial-gradient(at 80% 20%, #4ae7ff 0px, transparent 50%),
                radial-gradient(at 20% 80%, #ff62b2 0px, transparent 50%),
                radial-gradient(at 50% 50%, #ffeb3b 0px, transparent 50%);
        }
    </style>
</head>
<body class="bg-gradient-mesh min-h-screen font-sans flex flex-col items-center justify-center overflow-x-hidden p-4">

    <!-- ================= PHASE 1: THE GATE ================= -->
    <div id="phase1" class="max-w-md w-full bg-white/90 backdrop-blur-md rounded-3xl p-8 shadow-2xl text-center border-4 border-black transform transition duration-500 scale-100">
        <div class="text-6xl mb-4 floating-emoji">🛑</div>
        <h1 class="text-3xl font-black text-gray-900 uppercase tracking-tight mb-2">Access Denied (For Now)</h1>
        <p class="text-gray-700 font-medium mb-6">Before we celebrate Best Friend Day, we must verify if you actually possess the clearance and patience required.</p>
        <button onclick="startJourney()" class="w-full bg-yellow-400 hover:bg-yellow-300 text-black font-black text-xl py-4 px-6 rounded-2xl border-4 border-black shadow-[4px_4px_0px_0px_rgba(0,0,0,1)] active:translate-x-1 active:translate-y-1 active:shadow-none transition-all cursor-pointer uppercase tracking-wider">
            Begin Worthiness Test 🚀
        </button>
    </div>

    <!-- ================= PHASE 2: THE LOADING JOURNEY ================= -->
    <div id="phase2" class="hidden max-w-lg w-full bg-slate-900 rounded-3xl p-8 shadow-2xl border-4 border-cyan-400 text-center text-white">
        <!-- Progress Steps Indicator -->
        <div class="flex justify-between items-center text-xs font-bold uppercase tracking-widest text-slate-400 mb-8 border-b border-slate-800 pb-4">
            <span class="text-cyan-400">1. Security ✓</span>
            <span class="text-pink-500 animate-pulse">2. Analyzing Quirks ●</span>
            <span>3. Grand Reveal</span>
        </div>

        <div id="loading-emoji" class="text-7xl mb-6 inline-block animate-bounce">🧠</div>
        
        <!-- Dynamic Phrase Display -->
        <h2 id="phrase-display" class="text-2xl md:text-3xl font-black mb-6 text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 via-pink-500 to-yellow-300 min-h-[4rem] flex items-center justify-center">
            Initializing scanners...
        </h2>

        <!-- Custom Rainbow Progress Bar -->
        <div class="w-full bg-slate-800 h-6 rounded-full p-1 border-2 border-slate-700 mb-2 overflow-hidden">
            <div id="progress-bar" class="h-full bg-gradient-to-r from-cyan-400 via-pink-500 to-yellow-300 rounded-full transition-all duration-100 ease-out" style="width: 0%"></div>
        </div>
        <div class="flex justify-between text-xs font-mono text-slate-400">
            <span id="sub-status">CALCULATING DELAY PATTERNS</span>
            <span id="percentage">0%</span>
        </div>
    </div>

    <!-- ================= PHASE 3: THE GRAND REVEAL ================= -->
    <div id="phase3" class="hidden max-w-2xl w-full bg-white/95 backdrop-blur-md rounded-3xl p-6 md:p-8 shadow-2xl border-4 border-black text-center transform transition duration-700 translate-y-10">
        
        <!-- Floating celebratory icons -->
        <div class="absolute -top-12 left-10 text-5xl floating-emoji hidden md:block">🎉</div>
        <div class="absolute -top-16 right-12 text-5xl floating-emoji hidden md:block" style="animation-delay: 1.5s;">🌮</div>
        
        <h1 class="text-4xl md:text-6xl font-black text-gray-900 uppercase tracking-tighter mb-4 leading-none">
            Happy Best Friend Day!<br>
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-purple-600 via-pink-500 to-red-500">Veere! 🎉</span>
        </h1>
        
        <p class="text-lg md:text-xl font-bold text-gray-700 mb-8 max-w-md mx-auto">
            You survived the gauntlet. You're officially stuck with me for another calendar year. No refunds.
        </p>

        <!-- Stats Dashboard Grid -->
        <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8">
            <div class="bg-cyan-100 border-2 border-black p-4 rounded-2xl shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]">
                <div class="text-3xl mb-1">🗣️</div>
                <div class="font-black text-xl">999,999+</div>
                <div class="text-xs font-bold uppercase text-gray-600">Hours spent gossiping</div>
            </div>
            <div class="bg-pink-100 border-2 border-black p-4 rounded-2xl shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]">
                <div class="text-3xl mb-1">🧠</div>
                <div class="font-black text-xl">1 Shared</div>
                <div class="text-xs font-bold uppercase text-gray-600">Brain cell active</div>
            </div>
            <div class="bg-yellow-100 border-2 border-black p-4 rounded-2xl shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]">
                <div class="text-3xl mb-1">🍕</div>
                <div class="font-black text-xl">0% Ability</div>
                <div class="text-xs font-bold uppercase text-gray-600">To pick a restaurant</div>
            </div>
        </div>

        <!-- Interactive Compliment/Roast Component -->
        <div class="bg-purple-50 border-4 border-dashed border-purple-400 rounded-2xl p-6 mb-8 text-center">
            <h3 class="font-black uppercase text-purple-700 tracking-wider mb-2">The Ultimate Roulette</h3>
            <p id="roulette-text" class="text-gray-800 font-bold text-lg italic mb-4">Click below to see if the AI chooses violence or kindness today...</p>
            <button onclick="generateRoulette()" class="bg-purple-600 hover:bg-purple-700 text-white font-black py-2 px-6 rounded-xl transition cursor-pointer">
                Spin the Wheel 🎲
            </button>
        </div>

        <!-- Dopamine Button -->
        <button onclick="shootConfetti()" class="w-full bg-red-500 hover:bg-red-400 text-white font-black text-2xl py-4 px-6 rounded-2xl border-4 border-black shadow-[6px_6px_0px_0px_rgba(0,0,0,1)] active:translate-x-1 active:translate-y-1 active:shadow-none transition-all cursor-pointer uppercase mb-4">
            Click for Dopamine Hit ⚡
        </button>
        <p class="text-xs font-mono text-gray-500">Warning: Repeated clicking may result in pure joy.</p>
    </div>

    <!-- ================= JAVASCRIPT LOGIC ================= -->
    <script>
        // Custom phrases and their corresponding emoji/sub-status tags
        const journeyPhrases = [
            { text: "Scanning brain cells... <br><span class='text-sm text-red-400'>(Error: Minimal data found)</span>", emoji: "🧠", status: "PROCESSING DATA DEPTHS" },
            { text: "Analyzing total text response delays...", emoji: "⏳", status: "CALCULATING DELAY PATTERNS" },
            { text: "Calculating total money owed for shared food...", emoji: "💸", status: "AUDITING THE BILLS" },
            { text: "Retrieving embarrassing memories from the vault...", emoji: "🔐", status: "DECRYPTING COMPROMISING MEDIA" },
            { text: "Loading terrible dating decisions history...", emoji: "🤦‍♂️", status: "COMPILING REGRETS" },
            { text: "Verifying total tolerability levels... 99% loaded...", emoji: "📊", status: "STRESS TESTING FRIENDSHIP" },
            { text: "Finalizing friendship clearance...", emoji: "✨", status: "PREPARING IMPACT ZONE" }
        ];

        let currentPhraseIndex = 0;

        function startJourney() {
            // Hide Phase 1 and Show Phase 2
            document.getElementById('phase1').classList.add('hidden');
            document.getElementById('phase2').classList.remove('hidden');
            
            runPhraseCycle();
        }

        function runPhraseCycle() {
            if (currentPhraseIndex < journeyPhrases.length) {
                const currentData = journeyPhrases[currentPhraseIndex];
                
                // Update text, emoji, and sub-status
                document.getElementById('phrase-display').innerHTML = currentData.text;
                document.getElementById('loading-emoji').innerText = currentData.emoji;
                document.getElementById('sub-status').innerText = currentData.status;

                // Reset progress bar animation simulation for this phrase
                let progress = 0;
                const progressBar = document.getElementById('progress-bar');
                const percentageText = document.getElementById('percentage');
                
                // Animate progress filling up aggressively over 2 seconds
                const progressInterval = setInterval(() => {
                    progress += 5;
                    progressBar.style.width = `${progress}%`;
                    percentageText.innerText = `${progress}%`;

                    if (progress >= 100) {
                        clearInterval(progressInterval);
                        // Move to next phrase after a brief pause
                        setTimeout(() => {
                            currentPhraseIndex++;
                            runPhraseCycle();
                        }, 300);
                    }
                }, 90); // 90ms * 20 steps = ~1.8 seconds per phrase

            } else {
                revealFinalPage();
            }
        }

        function revealFinalPage() {
            // Hide loading phase
            document.getElementById('phase2').classList.add('hidden');
            
            // Show Grand Reveal phase
            const phase3 = document.getElementById('phase3');
            phase3.classList.remove('hidden');
            setTimeout(() => {
                phase3.classList.remove('translate-y-10');
            }, 50);

            // Trigger epic initial confetti explosion
            shootConfetti();
            // Secondary delay explosions for extra drama
            setTimeout(shootConfetti, 400);
            setTimeout(shootConfetti, 800);
        }

        function shootConfetti() {
            confetti({
                particleCount: 150,
                spread: 80,
                origin: { y: 0.6 }
            });
        }

        // Custom Roasts & Compliments array for the roulette wheel
        const mixedResponses = [
            "🏆 COMPLIMENT: Honestly, you're the family I actually got to choose. Love you!",
            "🔥 ROAST: I love how we don't even have to say out loud that I'm the funny one.",
            "🏆 COMPLIMENT: Thank you for always listening to my repeated rants about the same exact things.",
            "🔥 ROAST: Your taste in fashion is almost as questionable as your reply times.",
            "🏆 COMPLIMENT: Life would be incredibly boring (and much quieter) without you around.",
            "🔥 ROAST: I'd take a bullet for you. Not in the head, but like, the leg or something."
        ];

        function generateRoulette() {
            const display = document.getElementById('roulette-text');
            display.classList.add('animate-ping');
            
            // Add a slight delay to simulate a spinning wheel choice
            setTimeout(() => {
                display.classList.remove('animate-ping');
                const randomIndex = Math.floor(Math.random() * mixedResponses.length);
                display.innerText = mixedResponses[randomIndex];
            }, 300);
        }
    </script>
</body>
</html>
