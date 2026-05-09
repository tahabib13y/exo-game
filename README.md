<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Exo Game Arena - 100+ Free Online Games | Play Free Games Instantly</title>
    
    <!-- SEO Meta Tags -->
    <meta name="description" content="Play 100+ free online games instantly on Exo Game Arena. No download required, play action, puzzle, racing, sports & arcade games directly in your browser.">
    <meta name="keywords" content="free games, online games, play games, game arena, exo games, action games, puzzle games, racing games, sports games, arcade games">
    <meta name="author" content="Exo Game Arena">
    <meta name="robots" content="index, follow">
    <meta name="googlebot" content="index, follow">
    <meta name="revisit-after" content="1 day">
    <meta name="language" content="Bengali">
    <meta name="theme-color" content="#1e1b4b">
    
    <!-- Open Graph / Social Media -->
    <meta property="og:title" content="Exo Game Arena - Free Online Games">
    <meta property="og:description" content="Play 100+ free games instantly! Action, Puzzle, Racing, Sports & Arcade games.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://exogamearena.com">
    <meta property="og:image" content="https://placehold.co/1200x630/1e1b4b/ffffff?text=Exo+Game+Arena">
    
    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Exo Game Arena - Free Online Games">
    <meta name="twitter:description" content="Play 100+ free games instantly!">
    
    <!-- Canonical URL -->
    <link rel="canonical" href="https://exogamearena.com">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🎮</text></svg>">
    
    <!-- Schema.org markup for Google -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "WebSite",
        "name": "Exo Game Arena",
        "url": "https://exogamearena.com",
        "description": "Play 100+ free online games instantly",
        "potentialAction": {
            "@type": "SearchAction",
            "target": "https://exogamearena.com/search?q={search_term_string}",
            "query-input": "required name=search_term_string"
        }
    }
    </script>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.2/papaparse.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body { 
            font-family: 'Fredoka', sans-serif; 
            background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            min-height: 100vh;
        }
        
        /* Fixed Top Button - Only shows when scrolled */
        .fixed-action-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: linear-gradient(135deg, #f97316, #dc2626);
            color: white;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
        }
        
        .fixed-action-btn.show {
            opacity: 1;
            visibility: visible;
        }
        
        .fixed-action-btn:hover {
            transform: scale(1.1);
            background: linear-gradient(135deg, #ea580c, #dc2626);
        }
        
        /* Fixed Reset Button */
        .fixed-reset-btn {
            position: fixed;
            bottom: 30px;
            right: 100px;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: linear-gradient(135deg, #3b82f6, #8b5cf6);
            color: white;
            border: none;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            z-index: 1000;
        }
        
        .fixed-reset-btn:hover {
            transform: scale(1.1);
        }
        
        /* Category Buttons */
        .category-btn {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 10px 24px;
            border-radius: 50px;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 1px solid rgba(255,255,255,0.2);
            color: white;
        }
        
        .category-btn:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }
        
        .category-btn.active {
            background: linear-gradient(135deg, #ec4899, #8b5cf6);
            border-color: transparent;
            box-shadow: 0 4px 15px rgba(236,72,153,0.3);
        }
        
        /* Game Cards */
        .game-card { 
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            animation: fadeInUp 0.4s ease-out forwards;
            opacity: 0;
        }
        
        .game-card:hover { 
            transform: translateY(-8px) scale(1.02); 
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.5);
            background: rgba(255,255,255,0.15) !important;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Sticky Header - No Shaking */
        .sticky-header {
            position: sticky;
            top: 0;
            background: rgba(15,23,42,0.95);
            backdrop-filter: blur(15px);
            z-index: 99;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
        }
        
        /* Loader */
        .loader { 
            border-top-color: #f97316; 
            animation: spin 1s linear infinite; 
        }
        
        @keyframes spin { 
            0% { transform: rotate(0deg); } 
            100% { transform: rotate(360deg); } 
        }
        
        /* Search Clear Button */
        .search-clear {
            position: absolute;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background: rgba(255,255,255,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            color: white;
            font-size: 14px;
            transition: all 0.2s;
        }
        
        .search-clear:hover {
            background: rgba(255,255,255,0.4);
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #1e1b4b;
        }
        
        ::-webkit-scrollbar-thumb {
            background: #f97316;
            border-radius: 4px;
        }
        
        /* Responsive */
        @media (max-width: 640px) {
            .fixed-reset-btn {
                bottom: 20px;
                right: 80px;
                width: 45px;
                height: 45px;
                font-size: 20px;
            }
            .fixed-action-btn {
                bottom: 20px;
                right: 20px;
                width: 45px;
                height: 45px;
                font-size: 20px;
            }
            .category-btn {
                padding: 6px 16px;
                font-size: 12px;
            }
        }
    </style>
</head>
<body>

    <!-- Fixed Action Buttons -->
    <button id="fixedTopBtn" class="fixed-action-btn" title="Go to top">↑</button>
    <button id="fixedResetBtn" class="fixed-reset-btn" title="Reset all filters">⟳</button>

    <!-- Sticky Header (No Shaking) -->
    <div class="sticky-header">
        <div class="max-w-7xl mx-auto px-4 py-4">
            <div class="text-center">
                <h1 class="text-3xl md:text-5xl font-extrabold">
                    <span class="text-white">play on</span> 
                    <span class="text-pink-500">Exo game!</span>
                </h1>
                <p class="text-indigo-300 text-sm md:text-base mt-1">🎮 100+ free games | Play instantly | No downloads 🎮</p>
            </div>
        </div>
    </div>

    <div class="max-w-7xl mx-auto px-4 py-6">
        
        <!-- Search Box -->
        <div class="relative max-w-lg mx-auto mb-8">
            <input type="text" id="searchInput" placeholder="🔎 Search your favorite game..." 
                class="w-full px-6 py-4 rounded-full bg-white/10 backdrop-blur-md border border-white/20 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:border-transparent text-lg pr-12">
            <div id="searchClearBtn" class="search-clear hidden">✕</div>
        </div>
        
        <!-- Categories (Working) -->
        <div class="mb-8">
            <div class="flex flex-wrap justify-center gap-3">
                <button class="category-btn active" data-category="all">🎲 All Games</button>
                <button class="category-btn" data-category="action">🏃 Action</button>
                <button class="category-btn" data-category="puzzle">🧩 Puzzle</button>
                <button class="category-btn" data-category="racing">🏎️ Racing</button>
                <button class="category-btn" data-category="sports">⚽ Sports</button>
                <button class="category-btn" data-category="arcade">👾 Arcade</button>
            </div>
        </div>

        <!-- Stats -->
        <div class="flex justify-between items-center mb-6">
            <p id="gameCount" class="text-gray-300 font-semibold">🎮 Loading games...</p>
        </div>

        <!-- Loading -->
        <div id="loading" class="flex flex-col items-center justify-center py-20">
            <div class="loader rounded-full border-8 border-gray-700 border-t-orange-500 h-16 w-16 mb-4"></div>
            <p class="text-gray-300 text-xl">Fetching game universe... 🚀</p>
        </div>
        
        <!-- Error -->
        <div id="error" class="hidden text-center py-20 bg-red-900/30 rounded-2xl">
            <p class="text-red-400 text-xl font-bold">⚠️ Unable to load games</p>
            <button onclick="location.reload()" class="mt-4 bg-red-500 hover:bg-red-600 px-6 py-2 rounded-full text-white transition">
                🔄 Try Again
            </button>
        </div>

        <!-- Game Grid -->
        <div id="gameGrid" class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-6"></div>
        
        <!-- Footer -->
        <footer class="mt-16 pt-8 border-t border-white/10 text-center text-gray-400 text-sm">
            <p>© 2024 Exo Game Arena | All games are property of their respective owners</p>
            <p class="mt-2">🎮 Play responsibly | Have fun! 🎮</p>
        </footer>
    </div>

    <script>
        const csvUrl = 'https://docs.google.com/spreadsheets/d/1KOYxfabYXTEi0QaGxO-zzZUhAQL15zZlhflrqwRLeEE/export?format=csv';
        let allGames = [];
        let currentCategory = 'all';
        let currentSearch = '';
        
        // Function to get category (you can modify based on your CSV data)
        function getGameCategory(game) {
            const name = (game.Name || game.name || '').toLowerCase();
            if (name.includes('race') || name.includes('car') || name.includes('driving')) return 'racing';
            if (name.includes('puzzle') || name.includes('match') || name.includes('brain')) return 'puzzle';
            if (name.includes('sport') || name.includes('football') || name.includes('basketball')) return 'sports';
            if (name.includes('arcade') || name.includes('classic')) return 'arcade';
            return 'action';
        }
        
        // Filter games based on category and search
        function filterGames() {
            let filtered = [...allGames];
            
            // Apply search filter
            if (currentSearch) {
                filtered = filtered.filter(g => {
                    const name = (g.Name || g.name || '').toLowerCase();
                    return name.includes(currentSearch);
                });
            }
            
            // Apply category filter
            if (currentCategory !== 'all') {
                filtered = filtered.filter(g => getGameCategory(g) === currentCategory);
            }
            
            displayGames(filtered);
        }
        
        async function fetchGames() {
            const loadingEl = document.getElementById('loading');
            const errorEl = document.getElementById('error');
            
            loadingEl.classList.remove('hidden');
            errorEl.classList.add('hidden');
            
            try {
                const response = await fetch(csvUrl);
                if (!response.ok) throw new Error('Network issue');
                const csvData = await response.text();
                
                Papa.parse(csvData, {
                    header: true,
                    skipEmptyLines: true,
                    complete: (results) => {
                        if (!results.data || results.data.length === 0) throw new Error('No data');
                        allGames = results.data;
                        filterGames();
                        loadingEl.classList.add('hidden');
                    },
                    error: () => {
                        loadingEl.classList.add('hidden');
                        errorEl.classList.remove('hidden');
                    }
                });
            } catch (error) {
                loadingEl.classList.add('hidden');
                errorEl.classList.remove('hidden');
            }
        }
        
        function displayGames(games) {
            const grid = document.getElementById('gameGrid');
            grid.innerHTML = '';
            
            if (!games || games.length === 0) {
                grid.innerHTML = `<div class="col-span-full text-center py-20 text-gray-400 text-xl">😔 No games found!</div>`;
                document.getElementById('gameCount').innerHTML = `🎮 0 games`;
                return;
            }
            
            games.forEach((game, index) => {
                const name = game.Name || game.name || 'Unknown Game';
                let icon = game.Icon || game.icon || '';
                const link = game.Link || game.link || '#';
                
                if (!icon || icon === '') {
                    icon = 'https://placehold.co/400x400/1e1b4b/ffffff?text=🎮';
                }
                
                const card = document.createElement('div');
                card.className = 'game-card bg-white/10 backdrop-blur-sm rounded-2xl p-4 border border-white/20';
                card.style.animationDelay = `${Math.min(index * 0.03, 0.3)}s`;
                
                card.innerHTML = `
                    <div class="w-full aspect-square rounded-xl overflow-hidden bg-gray-800 mb-3">
                        <img src="${icon}" alt="${name}" class="w-full h-full object-cover" loading="lazy"
                             onerror="this.src='https://placehold.co/400x400/2d2d5e/ffffff?text=🎮'">
                    </div>
                    <h3 class="text-white font-bold text-md truncate">${name}</h3>
                    <button class="play-btn mt-3 w-full bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700 text-white py-2 rounded-full text-sm font-semibold transition">
                        🎮 Play Now
                    </button>
                `;
                
                const playBtn = card.querySelector('.play-btn');
                playBtn.addEventListener('click', (e) => {
                    e.stopPropagation();
                    if (link !== '#') window.open(link, '_blank');
                    else alert('Game link coming soon!');
                });
                
                grid.appendChild(card);
            });
            
            document.getElementById('gameCount').innerHTML = `       🎮 ${games.length} games`;
        }
        
        // Search functionality
        const searchInput = document.getElementById('searchInput');
        const searchClearBtn = document.getElementById('searchClearBtn');
        
        searchInput.addEventListener('input', (e) => {
            currentSearch = e.target.value.toLowerCase().trim();
            if (currentSearch === '') {
                searchClearBtn.classList.add('hidden');
            } else {
                searchClearBtn.classList.remove('hidden');
            }
            filterGames();
        });
        
        searchClearBtn.addEventListener('click', () => {
            searchInput.value = '';
            currentSearch = '';
            searchClearBtn.classList.add('hidden');
            filterGames();
        });
        
        // Category functionality
        const categoryBtns = document.querySelectorAll('.category-btn');
        categoryBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                categoryBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                currentCategory = btn.dataset.category;
                filterGames();
            });
        });
        
        // Fixed Top Button - Shows only when scrolled
        const topBtn = document.getElementById('fixedTopBtn');
        const resetBtn = document.getElementById('fixedResetBtn');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                topBtn.classList.add('show');
            } else {
                topBtn.classList.remove('show');
            }
        });
        
        topBtn.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        
        // Reset button - clears search and resets category
        resetBtn.addEventListener('click', () => {
            searchInput.value = '';
            currentSearch = '';
            searchClearBtn.classList.add('hidden');
            currentCategory = 'all';
            categoryBtns.forEach(b => b.classList.remove('active'));
            document.querySelector('[data-category="all"]').classList.add('active');
            filterGames();
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        
        // Initialize
        fetchGames();
    </script>
</body>
</html>
