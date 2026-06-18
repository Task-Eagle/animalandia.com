# animalandia.com
Animalandia | Animal General Knowledge


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JungleVerse | Animal General Knowledge</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🦁</text></svg>">
    
    <style>
        /* --- Google Fonts --- */
        @import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600&family=Nunito:wght@400;700&display=swap');

        /* --- Design Tokens / Variables --- */
        :root {
            --jungle-dark: #1b3a24;
            --jungle-green: #2d6a4fe3;
            --jungle-light: #52b788;
            --jungle-accent: #d8f3dc;
            --safari-gold: #ffb703;
            --text-dark: #222222;
            --text-light: #ffffff;
            --card-bg: #ffffff;
        }

        /* --- Reset & Base Styles --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Nunito', sans-serif;
            background-color: #f4f9f4;
            color: var(--text-dark);
            line-height: 1.6;
        }

        h1, h2, h3 {
            font-family: 'Fredoka', sans-serif;
            color: var(--jungle-dark);
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* --- Header & Branding --- */
        header {
            background: linear-gradient(rgba(27, 58, 36, 0.85), rgba(27, 58, 36, 0.95)), 
                        url('https://images.unsplash.com/photo-1516026672322-bc52d61a55d5?auto=format&fit=crop&w=1200&q=80') no-repeat center/cover;
            color: var(--text-light);
            text-align: center;
            padding: 3rem 1rem 2rem 1rem;
            border-bottom: 5px solid var(--safari-gold);
            animation: bounce 7s infinite linear;
        }

        .logo-containe {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            animation: spin 2s infinite;
        }
        
        .logo-container {
  display: inline-block;
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            animation: bounce 2s infinite;
        }

.logo-container:hover {
  animation: spinBounce 0.9s ease-out;
}

@keyframes spinBounce {
  0% {
    transform: rotate(0deg);
  }

  70% {
    transform: rotate(360deg);
  }

  85% {
    transform: rotate(380deg); /* overshoot */
  }

  95% {
    transform: rotate(360deg); /* bounce back */
  }

  100% {
    animation: bounce 2s infinite; /* settle */
  }
}

        header h1 {
            color: var(--safari-gold);
            font-size: 3rem;
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        header p {
            font-size: 1.1rem;
            color: var(--jungle-accent);
            margin-top: 0.5rem;
        }

        /* --- Navigation Ribbon --- */
        nav {
            background-color: var(--jungle-green);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            list-style: none;
        }

        /* Main Menu Items */
        .menu-item {
            position: relative;
        }

        .menu-link {
            display: block;
            padding: 1rem 1.5rem;
            color: var(--text-light);
            font-weight: 700;
            font-family: 'Fredoka', sans-serif;
            transition: background 0.3s, color 0.3s;
            cursor: pointer;
        }

        .menu-item:hover .menu-link,
        .menu-link:focus {
            background-color: var(--jungle-dark);
            color: var(--safari-gold);
        }

        /* --- Dropdown Menus (Multi-level) --- */
        .dropdown {
            position: absolute;
            top: 100%;
            left: 0;
            background-color: var(--card-bg);
            min-width: 200px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
            list-style: none;
            display: none;
            border-radius: 0 0 8px 8px;
            overflow: hidden;
        }

        .dropdown a {
            display: block;
            padding: 0.75rem 1rem;
            color: var(--text-dark);
            border-bottom: 1px solid #eee;
            transition: background 0.2s;
        }

        .dropdown a:hover {
            background-color: var(--jungle-accent);
            color: var(--jungle-dark);
        }

        /* Nested Sub-Dropdowns */
        .sub-dropdown-item {
            position: relative;
        }

        .sub-dropdown {
            position: absolute;
            top: 0;
            left: 100%;
            background-color: var(--card-bg);
            min-width: 180px;
            list-style: none;
            display: none;
            box-shadow: 4px 8px 16px rgba(0,0,0,0.15);
        }

        /* Trigger visibility on Hover & Focus (for Taps/Mobile accessibility) */
        .menu-item:hover > .dropdown,
        .menu-item:focus-within > .dropdown {
            display: block;
        }

        .sub-dropdown-item:hover > .sub-dropdown,
        .sub-dropdown-item:focus-within > .sub-dropdown {
            display: block;
        }

        /* --- Main Layout --- */
        main {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1rem;
        }

        section {
            margin-bottom: 3rem;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            border-left: 5px solid var(--jungle-green);
            padding-left: 0.5rem;
        }

        /* --- Animal of the Day (Wide Card) --- */
        .featured-card {
            background: linear-gradient(135deg, var(--jungle-dark), var(--jungle-green));
            color: var(--text-light);
            border-radius: 16px;
            overflow: hidden;
            display: flex;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            animation: bounce 3s infinite;
        }

        .featured-img {
            width: 45%;
            object-fit: cover;
            min-height: 300px;
        }

        .featured-content {
            padding: 2.5rem;
            width: 55%;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .badge {
            background-color: var(--safari-gold);
            color: var(--jungle-dark);
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-weight: 700;
            font-size: 0.85rem;
            width: fit-content;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .featured-content h3 {
            color: var(--text-light);
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .scientific-name {
            font-style: italic;
            color: var(--jungle-accent);
            margin-bottom: 1rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--safari-gold);
            color: var(--jungle-dark);
            padding: 0.75rem 1.5rem;
            border-radius: 30px;
            font-weight: 700;
            margin-top: 1.5rem;
            width: fit-content;
            transition: transform 0.2s, background 0.2s;
        }

        .btn:hover {
            transform: scale(1.05);
            background-color: #ffe066;
        }

        /* --- Categories Grid --- */
        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .category-card {
            background-color: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid rgba(0,0,0,0.05);
        }

        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(45, 106, 79, 0.2);
        }

        .category-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .category-info {
            padding: 1.5rem;
        }

        .category-info h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }

        /* --- Footer --- */
        footer {
            background-color: var(--jungle-dark);
            color: var(--jungle-accent);
            text-align: center;
            padding: 2rem 1rem;
            margin-top: 4rem;
            border-top: 4px solid var(--jungle-light);
        }

        /* --- Animations --- */
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-8px); }
        }

        /* --- Responsive Design --- */
        @media (max-width: 850px) {
            .featured-card {
                flex-direction: column;
            }
            .featured-img {
                width: 100%;
                height: 250px;
            }
            .featured-content {
                width: 100%;
                padding: 1.5rem;
            }
            .nav-container {
                flex-wrap: wrap;
            }
            .menu-link {
                padding: 0.75rem 1rem;
                font-size: 0.9rem;
            }
            /* Adjust dropdown stack direction on mobile if needed */
            .sub-dropdown {
                left: 0;
                top: 100%;
                z-index: 1001;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-container">🦁</div>
        <h1>Animalandia</h1>
        <p>Your Ultimate Kingdom of Animal General Knowledge</p>
    </header>

    <nav>
        <ul class="nav-container">
            <li class="menu-item"><a href="index.html" class="menu-link">Home</a></li>
            
            <li class="menu-item">
                <span class="menu-link" tabindex="0">Mammals ▾</span>
                <ul class="dropdown">
                    <li class="sub-dropdown-item">
                        <a href="categories/felines.html">Felines &raquo;</a>
                        <ul class="sub-dropdown">
                            <li class="sub-dropdown-item">
                                <a href="categories/felines.html#big-cats">Big Cats &raquo;</a>
                                <ul class="sub-dropdown">
                                    <li><a href="animals/lion.html">Lion</a></li>
                                    <li><a href="animals/tiger.html">Tiger</a></li>
                                    <li><a href="animals/leopard.html">Leopard</a></li>
                                    <li><a href="animals/jaguar.html">Jaguar</a></li>
                                </ul>
                            </li>
                            <li><a href="categories/felines.html#small-cats">Small Cats</a></li>
                        </ul>
                    </li>
                    <li><a href="categories/primates.html">Primates</a></li>
                    <li><a href="categories/cetaceans.html">Cetaceans (Whales/Dolphins)</a></li>
                </ul>
            </li>

            <li class="menu-item">
                <span class="menu-link" tabindex="0">Birds ▾</span>
                <ul class="dropdown">
                    <li><a href="categories/birds.html#raptors">Birds of Prey</a></li>
                    <li><a href="categories/birds.html#waterfowl">Waterfowl</a></li>
                    <li><a href="categories/birds.html#flightless">Flightless Birds</a></li>
                </ul>
            </li>

            <li class="menu-item">
                <span class="menu-link" tabindex="0">Reptiles ▾</span>
                <ul class="dropdown">
                    <li><a href="categories/reptiles.html#snakes">Snakes</a></li>
                    <li><a href="categories/reptiles.html#lizards">Lizards</a></li>
                    <li><a href="categories/reptiles.html#crocodilians">Crocodilians</a></li>
                </ul>
            </li>

            <li class="menu-item"><a href="categories/amphibians.html" class="menu-link">Amphibians</a></li>
            <li class="menu-item"><a href="categories/marine.html" class="menu-link">Marine Life</a></li>
        </ul>
    </nav>

    <main>
        
        <section>
            <h2 class="section-title">Animal of the Day</h2>
            <div class="featured-card">
                <img src="https://images.unsplash.com/photo-1614027164847-1b2809eb7b9b?auto=format&fit=crop&w=600&q=80" alt="Majestic Lion" class="featured-img">
                <div class="featured-content">
                    <span class="badge">Featured Mammal</span>
                    <h3>African Lion</h3>
                    <p class="scientific-name">Panthera leo</p>
                    <p>Known as the "King of the Jungle" (despite primarily living in grasslands and savannas), the lion is a magnificent apex predator known for its social prides, terrifying roar, and cooperative hunting strategies.</p>
                    <a href="animals/lion.html" class="btn">Explore Profile</a>
                </div>
            </div>
        </section>

        <section>
            <h2 class="section-title">Explore by Kingdom Category</h2>
            <div class="categories-grid">
                
                <div class="category-card">
                    <img src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?auto=format&fit=crop&w=400&q=80" alt="Mammals" class="category-img">
                    <div class="category-info">
                        <h3>Mammals</h3>
                        <p>Warm-blooded vertebrates characterized by the presence of hair or fur, and females that produce milk for nourishing their young.</p>
                        <a href="categories/felines.html" class="btn">Browse Mammals</a>
                    </div>
                </div>

                <div class="category-card">
                    <img src="https://images.unsplash.com/photo-1452570053594-1b985d6ea890?auto=format&fit=crop&w=400&q=80" alt="Birds" class="category-img">
                    <div class="category-info">
                        <h3>Birds</h3>
                        <p>Feathered, winged, bipedal, endothermic (warm-blooded), egg-laying, vertebrates known for their incredible flights.</p>
                        <a href="categories/birds.html" class="btn">Browse Birds</a>
                    </div>
                </div>

                <div class="category-card">
                    <img src="https://images.unsplash.com/photo-1604608684575-0497c3a5270c?auto=format&fit=crop&w=400&q=80" alt="Reptiles" class="category-img">
                    <div class="category-info">
                        <h3>Reptiles</h3>
                        <p>Air-breathing, ectothermic (cold-blooded) vertebrates covered in special skin made up of scales, bony plates, or both.</p>
                        <a href="categories/reptiles.html" class="btn">Browse Reptiles</a>
                    </div>
                </div>

            </div>
        </section>

    </main>

    <footer>
        <p>&copy; 2026 ANIMALANDIA Project.
            Contact us: taskeagle313@proton.me
        </p>
        <!-- modify this form HTML and place wherever you want your form -->
<form
  action="https://formspree.io/f/xqejnqyg"
  method="POST"
>
  <label>
    Your email:
    <input type="email" name="email">
  </label>
  <label>
    Your message:
    <textarea name="message"></textarea>
  </label>
  <!-- your other form fields go here -->
  <button type="submit">Send</button>
</form>
    </footer>

</body>
</html>
