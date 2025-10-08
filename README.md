<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Windows 11 Customization Hub</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chosen Palette: "Calm Harmony" - A minimalistic palette with a warm neutral background (zinc), dark text for readability, and a subtle slate blue for accents and interactive elements. -->
    <!-- Application Structure Plan: The SPA is designed as an interactive dashboard and guide. The structure prioritizes user exploration over the linear format of the Readme. It begins with a hero section for immediate context and GitHub links. The core of the app is an interactive, filterable grid of "component cards," allowing users to explore each tool visually. This is more engaging than a static table. A clear "How-to-Use" section with a copy-to-clipboard feature follows, streamlining the user's setup process. A modal system provides detailed information for each component without cluttering the main view. This structure was chosen to transform the static documentation into a dynamic, task-oriented experience, making the information more accessible and engaging for users wanting to customize their system. -->
    <!-- Visualization & Content Choices: The source report contains no quantitative data, making traditional charts irrelevant. Instead, the focus is on organizing and presenting qualitative/structural information. Report Info: List of customization tools and their descriptions. -> Goal: Organize & Inform. -> Presentation: Interactive Cards in a responsive grid. -> Interaction: On-click modals displaying detailed descriptions and providing direct links to the tool's website and its specific configuration folder on GitHub. Filter buttons allow users to sort between "Core Tools" and "App Configs". -> Justification: Cards are more visually appealing and scannable than a text table. The modal and filtering system allows for progressive disclosure of information, keeping the UI clean and user-focused. -> Library/Method: Vanilla JS for interactions, Tailwind CSS for layout and styling. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap');
        .modal-backdrop {
            transition: opacity 0.3s ease-in-out;
        }
        .modal-content {
            transition: transform 0.3s ease-in-out;
        }
        .custom-btn {
            transition: background-color 0.2s ease-in-out, transform 0.1s ease-in-out;
        }
        .custom-btn:hover {
            transform: translateY(-2px);
        }
        .component-card {
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .component-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
        }
    </style>
</head>
<body class="bg-zinc-50 text-zinc-800">

    <header class="bg-white/80 backdrop-blur-md sticky top-0 z-40 border-b border-zinc-200">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-xl font-bold text-zinc-900">🎨 Win11 Customization Hub</h1>
            <nav class="hidden md:flex items-center space-x-6">
                <a href="#introduction" class="text-sm font-medium text-zinc-600 hover:text-slate-600">Introduction</a>
                <a href="#components" class="text-sm font-medium text-zinc-600 hover:text-slate-600">Components</a>
                <a href="#setup" class="text-sm font-medium text-zinc-600 hover:text-slate-600">Setup Guide</a>
            </nav>
            <a href="https://github.com/abdullah-al-faahim/win11-customization" target="_blank" class="hidden md:inline-block bg-slate-800 text-white text-sm font-medium px-4 py-2 rounded-lg custom-btn hover:bg-slate-900">View on GitHub</a>
        </div>
    </header>

    <main class="container mx-auto px-6 py-12 md:py-20">

        <section id="hero" class="text-center">
            <h2 class="text-4xl md:text-6xl font-extrabold text-zinc-900 leading-tight">Transform Your Windows 11 Experience</h2>
            <p class="mt-4 max-w-2xl mx-auto text-lg text-zinc-600">
                A curated collection of tools and configurations to build a personalized, beautiful, and productive desktop environment.
            </p>
            <div class="mt-8 flex justify-center gap-4">
                <a href="#components" class="bg-slate-600 text-white px-8 py-3 rounded-lg font-semibold custom-btn hover:bg-slate-700">Explore Components</a>
                <a href="https://github.com/abdullah-al-faahim/win11-customization" target="_blank" class="bg-white text-slate-600 px-8 py-3 rounded-lg font-semibold custom-btn border border-zinc-200 hover:bg-zinc-100">View on GitHub →</a>
            </div>
        </section>

        <section id="introduction" class="mt-20 md:mt-32 max-w-4xl mx-auto scroll-mt-20">
             <div class="bg-white p-8 rounded-2xl border border-zinc-200">
                <h3 class="text-2xl font-bold text-zinc-900">🚀 What is this project?</h3>
                <p class="mt-4 text-zinc-600">This project provides all the configuration files, scripts, and links to the tools needed to completely overhaul the look and feel of Windows 11. Whether you're a developer, a power user, or just someone who loves an efficient and aesthetically pleasing desktop, you'll find everything you need to get started right here.</p>
                <div class="mt-6 flex flex-col sm:flex-row gap-4">
                     <a href="https://github.com/abdullah-al-faahim/win11-customization/issues/new?assignees=&labels=bug&template=bug_report.md&title=" target="_blank" class="flex-1 text-center bg-red-50 text-red-700 font-medium px-4 py-3 rounded-lg hover:bg-red-100 transition-colors">Report a Bug</a>
                     <a href="https://github.com/abdullah-al-faahim/win11-customization/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=" target="_blank" class="flex-1 text-center bg-sky-50 text-sky-700 font-medium px-4 py-3 rounded-lg hover:bg-sky-100 transition-colors">Request a Feature</a>
                </div>
            </div>
        </section>

        <section id="components" class="mt-20 md:mt-32 scroll-mt-20">
            <div class="text-center">
                <h3 class="text-3xl font-bold text-zinc-900">✨ Core Components & Configs</h3>
                <p class="mt-2 max-w-xl mx-auto text-zinc-600">
                    Explore the essential tools and application configurations that power this setup. Click on any card to see more details.
                </p>
                 <div id="filter-buttons" class="mt-6 flex justify-center gap-2">
                    <button data-filter="all" class="filter-btn bg-slate-600 text-white px-4 py-2 rounded-full text-sm font-medium">All</button>
                    <button data-filter="core" class="filter-btn bg-white text-zinc-600 px-4 py-2 rounded-full text-sm font-medium border border-zinc-200">Core Tools</button>
                    <button data-filter="app" class="filter-btn bg-white text-zinc-600 px-4 py-2 rounded-full text-sm font-medium border border-zinc-200">App Configs</button>
                </div>
            </div>

            <div id="component-grid" class="mt-12 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            </div>
        </section>
        
        <section id="setup" class="mt-20 md:mt-32 max-w-4xl mx-auto scroll-mt-20">
            <div class="text-center">
                 <h3 class="text-3xl font-bold text-zinc-900">🛠️ Setup Guide</h3>
                 <p class="mt-2 max-w-xl mx-auto text-zinc-600">Follow these steps to apply the customizations to your own system.</p>
            </div>
            <div class="mt-12 space-y-8">
                <div class="flex items-start gap-4">
                    <div class="flex-shrink-0 w-10 h-10 bg-slate-600 text-white rounded-full flex items-center justify-center font-bold text-lg">1</div>
                    <div>
                        <h4 class="text-lg font-semibold">Clone the Repository</h4>
                        <p class="text-zinc-600">Get all the necessary configuration files by cloning the GitHub repository to your local machine.</p>
                        <div class="mt-3 relative bg-zinc-800 text-white p-4 rounded-lg font-mono text-sm">
                            <code id="clone-command">git clone https://github.com/abdullah-al-faahim/win11-customization.git</code>
                            <button id="copy-btn" class="absolute top-3 right-3 bg-zinc-700 hover:bg-zinc-600 text-zinc-300 text-xs px-2 py-1 rounded">Copy</button>
                        </div>
                    </div>
                </div>
                 <div class="flex items-start gap-4">
                    <div class="flex-shrink-0 w-10 h-10 bg-slate-600 text-white rounded-full flex items-center justify-center font-bold text-lg">2</div>
                    <div>
                        <h4 class="text-lg font-semibold">Install the Tools</h4>
                        <p class="text-zinc-600">Download and install the applications listed in the Components section from their official websites. You can find the links by clicking on each component card.</p>
                    </div>
                </div>
                 <div class="flex items-start gap-4">
                    <div class="flex-shrink-0 w-10 h-10 bg-slate-600 text-white rounded-full flex items-center justify-center font-bold text-lg">3</div>
                    <div>
                        <h4 class="text-lg font-semibold">Apply Configurations</h4>
                        <p class="text-zinc-600">Navigate to the folder corresponding to the tool you want to customize (e.g., `GlazeWM`, `yasb`). Follow any instructions inside that folder, or copy the configuration files to the appropriate directory for that application. For example, `yasb` configs usually go in <code class="bg-zinc-200 text-zinc-700 text-xs px-1 py-0.5 rounded">C:\Users\YourUser\.config\yasb\</code>.</p>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="mt-20 md:mt-32 border-t border-zinc-200 bg-white">
        <div class="container mx-auto px-6 py-8 text-center text-zinc-500">
            <p>&copy; 2024 Abdullah Al-Faahim. All configurations are open-source.</p>
            <p class="mt-1 text-sm">This interactive guide was generated based on the GitHub repository.</p>
        </div>
    </footer>
    
    <div id="modal" class="modal-backdrop fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50 opacity-0 pointer-events-none">
        <div id="modal-content" class="modal-content bg-white w-full max-w-lg rounded-2xl shadow-xl p-8 transform scale-95">
            <div class="flex justify-between items-start">
                 <div class="flex-1">
                    <h2 id="modal-title" class="text-2xl font-bold text-zinc-900"></h2>
                    <p id="modal-category" class="text-sm font-medium text-slate-500 mt-1"></p>
                 </div>
                 <button id="modal-close" class="text-zinc-400 hover:text-zinc-600">&times;</button>
            </div>
            <p id="modal-description" class="mt-4 text-zinc-600"></p>
            <div class="mt-6 flex flex-col sm:flex-row gap-4">
                <a id="modal-website-link" href="#" target="_blank" class="flex-1 text-center bg-slate-600 text-white font-medium px-4 py-3 rounded-lg custom-btn hover:bg-slate-700">Visit Website</a>
                <a id="modal-config-link" href="#" target="_blank" class="flex-1 text-center bg-white text-slate-600 font-medium px-4 py-3 rounded-lg custom-btn border border-zinc-200 hover:bg-zinc-100">View Config Files</a>
            </div>
        </div>
    </div>


    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const components = [
                {
                    name: 'GlazeWM',
                    category: 'Core Tool',
                    type: 'core',
                    icon: '🪟',
                    description: 'A dynamic, tiling window manager for Windows that helps in organizing windows and improving workflow.',
                    websiteUrl: 'https://glazewm.com/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/GlazeWM'
                },
                {
                    name: 'yasb',
                    category: 'Core Tool',
                    type: 'core',
                    icon: '📊',
                    description: '(Yet Another Status Bar) A highly customizable status bar for Windows, perfect for displaying system info.',
                    websiteUrl: 'https://github.com/DaniloI/yasb',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/YASB'
                },
                {
                    name: 'Windhawk',
                    category: 'Core Tool',
                    type: 'core',
                    icon: '🦅',
                    description: 'An advanced customization tool for Windows, allowing for system-wide modifications and tweaks.',
                    websiteUrl: 'https://windhawk.net/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Windhawk'
                },
                {
                    name: 'Flow Launcher',
                    category: 'Core Tool',
                    type: 'core',
                    icon: '🚀',
                    description: 'An elegant and fast application launcher for Windows that boosts productivity with plugins and themes.',
                    websiteUrl: 'https://www.flowlauncher.com/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Flow%20Launcher'
                },
                {
                    name: 'Windows Terminal',
                    category: 'Core Tool',
                    type: 'core',
                    icon: 'TERMINAL',
                    description: 'The official modern Windows Terminal with custom PowerShell configurations for a better CLI experience.',
                    websiteUrl: 'https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Terminal'
                },
                {
                    name: 'JetBrains Mono',
                    category: 'Core Tool',
                    type: 'core',
                    icon: '🎨',
                    description: 'A beautiful, readable typeface used as the default system font for a clean, modern look.',
                    websiteUrl: 'https://www.jetbrains.com/lp/mono/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Change%20Windows%20Default%20Font'
                },
                {
                    name: 'Discord',
                    category: 'Application Config',
                    type: 'app',
                    icon: '💬',
                    description: 'Custom themes and styles for the Discord application to match the overall desktop aesthetic.',
                    websiteUrl: 'https://discord.com/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Discord'
                },
                {
                    name: 'File Explorer',
                    category: 'Application Config',
                    type: 'app',
                    icon: '📁',
                    description: 'Tweaks and modifications for the Windows File Explorer for a more streamlined and functional experience.',
                    websiteUrl: '#',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/File%20Explorer'
                },
                 {
                    name: 'OBS',
                    category: 'Application Config',
                    type: 'app',
                    icon: '📹',
                    description: 'Configuration settings for Open Broadcaster Software (OBS) for optimized recording and streaming.',
                    websiteUrl: 'https://obsproject.com/',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/OBS'
                },
                {
                    name: 'Wallpaper',
                    category: 'Application Config',
                    type: 'app',
                    icon: '🖼️',
                    description: 'A collection of wallpapers that complement the customization theme.',
                    websiteUrl: '#',
                    configUrl: 'https://github.com/abdullah-al-faahim/win11-customization/tree/main/Wallpaper'
                }
            ];

            const grid = document.getElementById('component-grid');
            const modal = document.getElementById('modal');
            const modalContent = document.getElementById('modal-content');
            const modalClose = document.getElementById('modal-close');

            const renderComponents = (filter = 'all') => {
                grid.innerHTML = '';
                const filteredComponents = filter === 'all' ? components : components.filter(c => c.type === filter);
                
                filteredComponents.forEach(component => {
                    const card = document.createElement('div');
                    card.className = 'component-card bg-white p-6 rounded-2xl border border-zinc-200 cursor-pointer';
                    card.innerHTML = `
                        <div class="text-3xl">${component.icon}</div>
                        <h4 class="mt-4 font-bold text-lg text-zinc-900">${component.name}</h4>
                        <p class="mt-1 text-sm text-zinc-600">${component.description.split(') ')[1] || component.description.split('. ')[0]}.</p>
                    `;
                    card.addEventListener('click', () => openModal(component));
                    grid.appendChild(card);
                });
            };
            
            const openModal = (component) => {
                document.getElementById('modal-title').textContent = component.name;
                document.getElementById('modal-category').textContent = component.category;
                document.getElementById('modal-description').textContent = component.description;
                document.getElementById('modal-website-link').href = component.websiteUrl;
                document.getElementById('modal-website-link').style.display = component.websiteUrl === '#' ? 'none' : 'block';
                document.getElementById('modal-config-link').href = component.configUrl;

                modal.classList.remove('opacity-0', 'pointer-events-none');
                modalContent.classList.remove('scale-95');
            };

            const closeModal = () => {
                modal.classList.add('opacity-0');
                modalContent.classList.add('scale-95');
                setTimeout(() => modal.classList.add('pointer-events-none'), 300);
            };

            modalClose.addEventListener('click', closeModal);
            modal.addEventListener('click', (e) => {
                if (e.target === modal) {
                    closeModal();
                }
            });

            document.getElementById('copy-btn').addEventListener('click', (e) => {
                const command = document.getElementById('clone-command').innerText;
                navigator.clipboard.writeText(command).then(() => {
                    e.target.innerText = 'Copied!';
                    setTimeout(() => { e.target.innerText = 'Copy'; }, 2000);
                });
            });

            const filterButtons = document.querySelectorAll('.filter-btn');
            filterButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const filter = button.dataset.filter;
                    renderComponents(filter);
                    
                    filterButtons.forEach(btn => {
                         btn.classList.remove('bg-slate-600', 'text-white');
                         btn.classList.add('bg-white', 'text-zinc-600');
                    });
                    button.classList.add('bg-slate-600', 'text-white');
                    button.classList.remove('bg-white', 'text-zinc-600');
                });
            });

            renderComponents();
        });
    </script>
</body>
</html>
