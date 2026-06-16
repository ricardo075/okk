<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MD Agência MZ | Conhecimento que Transforma</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Plus Jakarta Sans & Playfair Display -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,700;1,400&display=swap" rel="stylesheet">
    <!-- FontAwesome para Ícones -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        agency: {
                            50: '#f3effc',
                            100: '#e1d5fa',
                            500: '#8b5cf6', // Roxo Elétrico
                            600: '#7c3aed',
                            700: '#6d28d9',
                            900: '#3b0764', // Violeta Profundo
                            950: '#1e0236', // Fundo Escuro Místico
                        },
                        neon: {
                            cyan: '#06b6d4',
                            purple: '#a855f7',
                            gold: '#f59e0b'
                        }
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    }
                }
            }
        }
    </script>
    <style>
        html {
            scroll-behavior: smooth;
        }
        .hero-gradient {
            background: radial-gradient(circle at top, #3b0764 0%, #110022 60%, #050010 100%);
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glass-card:hover {
            border-color: rgba(139, 92, 246, 0.5);
            box-shadow: 0 0 35px rgba(139, 92, 246, 0.25);
        }
        /* Carrossel infinito suave para logos de parceiros */
        @keyframes infiniteScroll {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        .animate-infinite-scroll {
            animation: infiniteScroll 25s linear infinite;
        }
        /* Brilho pulsante */
        .neon-glow {
            filter: drop-shadow(0 0 15px rgba(139, 92, 246, 0.6));
        }
    </style>
</head>
<body class="bg-[#050010] text-stone-100 font-sans overflow-x-hidden">

    <!-- BARRA DE URGÊNCIA / AVISO QR CODE -->
    <div class="bg-gradient-to-r from-agency-700 via-purple-600 to-agency-900 text-white text-center py-3 px-4 text-xs sm:text-sm tracking-wider uppercase font-extrabold flex justify-center items-center gap-2 border-b border-white/10">
        <span class="inline-flex h-2.5 w-2.5 rounded-full bg-emerald-400 animate-ping"></span>
        <span>🔥 ATENÇÃO: Criação de Web Sites Profissionais com condições incríveis de lançamento!</span>
    </div>

    <!-- NAVEGAÇÃO PRINCIPAL -->
    <nav class="sticky top-0 z-40 bg-[#050010]/90 backdrop-blur-md border-b border-white/10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logótipo da Agência -->
                <div class="flex-shrink-0 flex items-center">
                    <a href="#" class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-xl bg-gradient-to-tr from-agency-500 to-neon-purple flex items-center justify-center text-white font-black text-xl shadow-lg shadow-agency-500/20">
                            MD
                        </div>
                        <div class="flex flex-col text-left">
                            <span class="text-xl font-extrabold tracking-wider text-white leading-none">MD AGÊNCIA</span>
                            <span class="text-[9px] text-neon-purple font-bold tracking-[0.25em] uppercase mt-1">Conhecimento que Transforma</span>
                        </div>
                    </a>
                </div>

                <!-- Links Desktop Reordenados (Planos de Marketing antes de Websites) -->
                <div class="hidden lg:flex space-x-6 lg:space-x-8 items-center text-sm font-bold">
                    <a href="#quem-somos" class="text-stone-300 hover:text-white transition">Quem Somos</a>
                    <a href="#bastidores" class="text-emerald-400 hover:text-white transition">Trabalho em Ação</a>
                    <a href="#servicos" class="text-stone-300 hover:text-white transition">Serviços</a>
                    <a href="#equipamento" class="text-stone-300 hover:text-white transition">Equipamento & Drone</a>
                    <a href="#planos" class="text-stone-300 hover:text-white transition">Planos de Marketing</a>
                    <a href="#websites" class="text-stone-300 hover:text-white transition">Websites</a>
                    <a href="#contacto" class="bg-agency-600 hover:bg-agency-500 text-white px-5 py-2.5 rounded-full shadow-md shadow-agency-600/20 transition transform hover:-translate-y-0.5">Falar com Especialista</a>
                </div>

                <!-- Botão de Contacto Rápido Móvel -->
                <div class="flex lg:hidden items-center gap-2">
                    <a href="https://wa.me/258852508924" target="_blank" class="bg-emerald-600 text-white p-2.5 rounded-full hover:bg-emerald-500 transition">
                        <i class="fa-brands fa-whatsapp text-lg"></i>
                    </a>
                    <button onclick="toggleMobileMenu()" class="p-2.5 text-stone-300 hover:text-white focus:outline-none">
                        <i class="fa-solid fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Menu Lateral Móvel Reordenado -->
        <div id="mobileMenu" class="hidden lg:hidden bg-[#050010] border-b border-white/5 px-4 py-6 space-y-4">
            <a href="#quem-somos" onclick="toggleMobileMenu()" class="block text-stone-300 font-semibold py-1">Quem Somos</a>
            <a href="#bastidores" onclick="toggleMobileMenu()" class="block text-emerald-400 font-semibold py-1">Trabalho em Ação</a>
            <a href="#servicos" onclick="toggleMobileMenu()" class="block text-stone-300 font-semibold py-1">Serviços</a>
            <a href="#equipamento" onclick="toggleMobileMenu()" class="block text-stone-300 font-semibold py-1">Equipamento & Drone</a>
            <a href="#planos" onclick="toggleMobileMenu()" class="block text-stone-300 font-semibold py-1">Planos de Marketing</a>
            <a href="#websites" onclick="toggleMobileMenu()" class="block text-stone-300 font-semibold py-1">Websites</a>
            <a href="https://wa.me/258852508924" target="_blank" class="block bg-agency-600 text-white text-center font-bold py-3 rounded-xl uppercase text-xs">Falar no WhatsApp 🇲🇿</a>
        </div>
    </nav>

    <!-- SECÇÃO HERO (Apresentação Principal) -->
    <header class="relative hero-gradient py-20 sm:py-32 overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
            
            <!-- Conteúdo de Copywriting de Alta Conversão -->
            <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                <span class="inline-flex items-center gap-2 py-1.5 px-4 rounded-full text-xs font-bold bg-agency-500/10 text-agency-100 border border-agency-500/30 tracking-wider uppercase">
                    🚀 AGÊNCIA DE MARKETING DIGITAL • NAMPULA
                </span>
                <h1 class="text-4xl sm:text-6xl font-extrabold text-white leading-[1.1] tracking-tight">
                    Não fazemos apenas posts.<br>
                    Nós geramos <span class="text-transparent bg-clip-text bg-gradient-to-r from-neon-purple via-agency-500 to-neon-cyan">Vendas Reais</span>.
                </h1>
                <p class="text-stone-300 text-sm sm:text-lg max-w-xl mx-auto lg:mx-0 leading-relaxed font-light">
                    Ajudamos a sua empresa a ser <b>vista, lembrada e escolhida</b> pelo cliente digital. Estratégias completas adaptadas ao mercado de Moçambique para atrair mais clientes e multiplicar a sua faturação de forma garantida.
                </p>
                
                <!-- CTAs e Redes Sociais Rápidas -->
                <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4">
                    <a href="https://wa.me/258852508924" target="_blank" class="w-full sm:w-auto text-center bg-gradient-to-r from-agency-500 to-agency-700 hover:from-agency-600 hover:to-agency-800 text-white font-extrabold px-8 py-4 rounded-full shadow-lg shadow-agency-600/30 transform hover:-translate-y-1 transition duration-300 flex items-center justify-center gap-2">
                        <i class="fa-brands fa-whatsapp text-lg"></i> Iniciar Projeto Grátis
                    </a>
                    <div class="flex gap-3 justify-center">
                        <a href="https://instagram.com/md_agency_mz" target="_blank" class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-stone-300 hover:text-white hover:bg-agency-500/20 transition-all" title="Instagram">
                            <i class="fa-brands fa-instagram text-xl"></i>
                        </a>
                        <a href="https://tiktok.com/@md_agency_mz" target="_blank" class="w-12 h-12 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-stone-300 hover:text-white hover:bg-agency-500/20 transition-all" title="TikTok">
                            <i class="fa-brands fa-tiktok text-lg"></i>
                        </a>
                    </div>
                </div>

                <!-- Benefícios Rápidos -->
                <div class="flex flex-wrap justify-center lg:justify-start gap-4 pt-6 text-xs text-stone-400">
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-circle-check text-emerald-400"></i> Suporte Rápido Moçambique</span>
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-circle-check text-emerald-400"></i> Relatórios Mensais Transparentes</span>
                </div>
            </div>

            <!-- Box Dinâmica de Ofertas em Destaque -->
            <div class="lg:col-span-5 flex justify-center items-center">
                <div class="relative w-full max-w-sm glass-card rounded-[2.5rem] p-6 sm:p-8 space-y-6 shadow-2xl relative overflow-hidden">
                    <div class="absolute -top-24 -right-24 w-48 h-48 rounded-full bg-agency-500/20 blur-2xl"></div>
                    
                    <div class="flex items-center justify-between">
                        <span class="text-[10px] font-bold text-neon-purple uppercase tracking-widest bg-agency-500/10 px-3 py-1 rounded-full border border-agency-500/20">A Solução Completa</span>
                        <span class="text-xs text-stone-400"><i class="fa-solid fa-location-dot text-red-500"></i> Nampula, MZ</span>
                    </div>

                    <div class="space-y-3">
                        <h3 class="font-serif font-bold text-2xl text-white">Presença Digital Sólida</h3>
                        <p class="text-stone-300 text-xs leading-relaxed font-light">
                            Não se limite a existir na internet. Tenha uma estrutura profissional com filmagens com drone de alta resolução, fotografias de topo e um website feito à medida para alavancar a sua faturação.
                        </p>
                    </div>

                    <div class="h-px bg-white/5"></div>

                    <!-- Mini Portfolio ou Destaques de Equipamento -->
                    <div class="grid grid-cols-2 gap-3 text-xs">
                        <div class="bg-[#050010] p-3 rounded-2xl border border-white/5">
                            <span class="text-neon-purple block font-bold mb-0.5">Websites Pro</span>
                            <span class="text-emerald-400 font-extrabold text-[11px]">Sob Consulta 🏷️</span>
                        </div>
                        <div class="bg-[#050010] p-3 rounded-2xl border border-white/5">
                            <span class="text-neon-cyan block font-bold mb-0.5">Drone 4K</span>
                            <span class="text-stone-300 font-extrabold text-[11px]">5 000 MT / Voo</span>
                        </div>
                    </div>

                    <a href="https://wa.me/258852508924" target="_blank" class="block w-full bg-white text-[#050010] font-extrabold text-center py-3.5 rounded-2xl hover:bg-purple-600 hover:text-white transition duration-300 text-xs uppercase tracking-wider">
                        Solicitar Orçamento Rápido 📲
                    </a>
                </div>
            </div>

        </div>
    </header>

    <!-- CARROSSEL DE EMPRESAS PARCEIRAS (PROVA SOCIAL OFICIAL) -->
    <section class="py-12 bg-[#02000a] border-y border-white/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-4">
            <p class="text-stone-400 text-sm tracking-wider uppercase font-bold">Empresas que confiam e crescem com a MD Agência MZ</p>
            
            <div class="w-full overflow-hidden relative">
                <!-- Máscara de desvanecimento nas bordas -->
                <div class="absolute inset-y-0 left-0 w-24 bg-gradient-to-r from-[#02000a] to-transparent z-10 pointer-events-none"></div>
                <div class="absolute inset-y-0 right-0 w-24 bg-gradient-to-l from-[#02000a] to-transparent z-10 pointer-events-none"></div>

                <div class="flex w-[250%] animate-infinite-scroll py-2 gap-12 sm:gap-16 items-center">
                    <!-- Logos Solicitados -->
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-bread-slice text-neon-purple text-base"></i> Casa do Pão</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-glass-cheers text-neon-cyan text-base"></i> Sporting Bar Restaurante</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-store text-neon-purple text-base"></i> China Mall</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-dumbbell text-neon-cyan text-base"></i> M Fitness Store</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-wine-glass text-neon-purple text-base"></i> Dom Vinho</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-utensils text-neon-cyan text-base"></i> A Nova Portuguesa</span>

                    <!-- Duplicado para loop perfeito -->
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-bread-slice text-neon-purple text-base"></i> Casa do Pão</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-glass-cheers text-neon-cyan text-base"></i> Sporting Bar Restaurante</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-store text-neon-purple text-base"></i> China Mall</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-dumbbell text-neon-cyan text-base"></i> M Fitness Store</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-wine-glass text-neon-purple text-base"></i> Dom Vinho</span>
                    <span class="text-stone-300 hover:text-white transition duration-300 text-sm sm:text-base font-extrabold uppercase tracking-widest flex items-center gap-2"><i class="fa-solid fa-utensils text-neon-cyan text-base"></i> A Nova Portuguesa</span>
                </div>
            </div>
            <p class="text-stone-500 text-xs sm:text-sm italic">Parcerias de confiança que consolidam o crescimento das marcas no terreno.</p>
        </div>
    </section>

    <!-- SECÇÃO QUEM SOMOS -->
    <section id="quem-somos" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            
            <!-- Imagem Realista de Bastidores de Gravação de Vídeo / Marketing -->
            <div class="relative rounded-3xl overflow-hidden shadow-2xl h-80 sm:h-[450px] group border border-white/10 bg-brand-950">
                <img src="https://images.unsplash.com/photo-1533750516457-a7f992034fec?auto=format&fit=crop&w=800&q=80" alt="Produtor da MD Agência gravando conteúdo profissional com câmara no local" class="w-full h-full object-cover opacity-90 group-hover:scale-105 transition-transform duration-500">
                <div class="absolute inset-0 bg-gradient-to-t from-[#050010] via-transparent to-transparent"></div>
                <div class="absolute bottom-6 left-6 right-6 p-6 glass-card rounded-2xl space-y-2">
                    <span class="text-neon-purple font-bold text-xs sm:text-sm uppercase tracking-widest">Nampula, Moçambique</span>
                    <h4 class="text-white font-extrabold text-lg sm:text-xl font-serif">MD Agência MZ – Conhecimento que Transforma!</h4>
                </div>
            </div>

            <!-- História da Empresa -->
            <div class="space-y-6">
                <span class="text-sm font-bold text-neon-purple uppercase tracking-widest">A Nossa Essência</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white">Criadores de Ideias, Conquistadores de Resultados</h2>
                <p class="text-stone-200 text-base sm:text-lg leading-relaxed font-normal">
                    A MD Agência MZ é uma empresa jovem, moderna e altamente inovadora sediada em Nampula. Somos especializados em criar e expandir a presença digital de negócios de alta performance no mercado de Moçambique de forma inteligente.
                </p>
                <p class="text-stone-200 text-base sm:text-lg leading-relaxed font-normal">
                    Trabalhamos com uma estratégia simples, prática e focada em resultados rápidos e sólidos. O nosso grande objetivo não é apenas gerir perfis de redes sociais, mas garantir que a sua empresa seja vista, lembrada e escolhida por centenas de novos clientes de verdade.
                </p>
                
                <!-- Diferenciais Rápidos -->
                <div class="grid grid-cols-2 gap-4 text-xs sm:text-sm pt-4 border-t border-white/5">
                    <div class="flex items-start gap-2.5">
                        <span class="text-emerald-400 text-xl font-bold">✓</span>
                        <div>
                            <h5 class="font-bold text-white text-sm sm:text-base">Foco em Resultados</h5>
                            <p class="text-stone-300 text-xs leading-snug">Aumentamos as suas vendas de forma palpável.</p>
                        </div>
                    </div>
                    <div class="flex items-start gap-2.5">
                        <span class="text-emerald-400 text-xl font-bold">✓</span>
                        <div>
                            <h5 class="font-bold text-white text-sm sm:text-base">Suporte Direto</h5>
                            <p class="text-stone-300 text-xs leading-snug">Atendimento rápido e de alta proximidade.</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- GALERIA DE TRABALHOS EM AÇÃO (BASTIDORES - FOTOS DOS LOCAIS REAIS) -->
    <section id="bastidores" class="py-20 bg-gradient-to-b from-[#050010] to-[#02000a] border-t border-white/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
            
            <div class="text-center space-y-3">
                <span class="text-sm font-bold text-emerald-400 uppercase tracking-widest font-extrabold">Produção ao Vivo</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white leading-tight">O Nosso Trabalho em Ação</h2>
                <p class="text-stone-200 text-base sm:text-lg max-w-xl mx-auto">
                    Captamos o dinamismo e a essência do seu negócio no local com fotografias profissionais e filmagens completas em Nampula.
                </p>
            </div>

            <!-- Grid com Imagens Temáticas de Produção Real para Substituição Posterior -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Card 1: Equipa a tirar fotos no local -->
                <div class="glass-card rounded-3xl overflow-hidden border border-white/10 flex flex-col justify-between group">
                    <div class="relative h-64 overflow-hidden bg-black">
                        <!-- Imagem de equipa de marketing tirando fotos no local comercial -->
                        <img src="https://images.unsplash.com/photo-1542744094-3a31f103e35f?auto=format&fit=crop&w=600&q=80" alt="Fotógrafo da agência no local tirando fotos profissionais" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500 opacity-90">
                        <div class="absolute inset-0 bg-gradient-to-t from-[#050010] via-transparent to-transparent"></div>
                        <span class="absolute bottom-4 left-4 bg-purple-600 text-white font-extrabold text-xs py-1 px-3 rounded-full uppercase tracking-wider shadow-lg">
                            BASTIDORES DE SESSÃO
                        </span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-white font-bold text-xl font-serif">Sessões Fotográficas no Local</h4>
                        <p class="text-stone-200 text-sm leading-relaxed font-normal">
                            Registamos a equipa de produção a captar os melhores detalhes nos vossos estabelecimentos. Perfeito para transmitir credibilidade e atrair novos parceiros comerciais.
                        </p>
                        <span class="text-xs text-stone-400 block italic font-semibold mt-2">📍 Espaço reservado para colocar as vossas fotos reais em ação!</span>
                    </div>
                </div>

                <!-- Card 2: Gravação de Vídeos de Reels/TikTok -->
                <div class="glass-card rounded-3xl overflow-hidden border border-white/10 flex flex-col justify-between group">
                    <div class="relative h-64 overflow-hidden bg-black">
                        <!-- Imagem de gravação de vídeo dinâmico para redes sociais -->
                        <img src="https://images.unsplash.com/photo-1611162617213-7d7a39e9b1d7?auto=format&fit=crop&w=600&q=80" alt="Equipa gravando conteúdo de vídeo com tripé e gimbal" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500 opacity-90">
                        <div class="absolute inset-0 bg-gradient-to-t from-[#050010] via-transparent to-transparent"></div>
                        <span class="absolute bottom-4 left-4 bg-emerald-600 text-white font-extrabold text-xs py-1 px-3 rounded-full uppercase tracking-wider shadow-lg">
                            PRODUÇÃO DE VÍDEO DYNAMIC
                        </span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-white font-bold text-xl font-serif">Criação de Vídeos & Reels</h4>
                        <p class="text-stone-200 text-sm leading-relaxed font-normal">
                            Desenvolvemos vídeos envolvventes e dinâmicos para plataformas como TikTok e Instagram Reels, acompanhando o ritmo acelerado e o gosto do vosso público.
                        </p>
                        <span class="text-xs text-stone-400 block italic font-semibold mt-2">📍 Espaço reservado para colocar as vossas fotos reais em ação!</span>
                    </div>
                </div>

                <!-- Card 3: Voo de Drone Prático -->
                <div class="glass-card rounded-3xl overflow-hidden border border-white/10 flex flex-col justify-between group">
                    <div class="relative h-64 overflow-hidden bg-black">
                        <!-- Imagem de operação de drone profissional ao vivo -->
                        <img src="https://images.unsplash.com/photo-1508614589041-895b88991e3e?auto=format&fit=crop&w=600&q=80" alt="Operador controlando drone no terreno" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500 opacity-90">
                        <div class="absolute inset-0 bg-gradient-to-t from-[#050010] via-transparent to-transparent"></div>
                        <span class="absolute bottom-4 left-4 bg-neon-cyan text-slate-950 font-black text-xs py-1 px-3 rounded-full uppercase tracking-wider shadow-lg">
                            CAPTAÇÃO AÉREA 4K
                        </span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-white font-bold text-xl font-serif">Filmagem com Drone no Terreno</h4>
                        <p class="text-stone-200 text-sm leading-relaxed font-normal">
                            Mostramos a preparação e execução dos voos de drone para captar imagens deslumbrantes que diferenciam por completo a vossa infraestrutura.
                        </p>
                        <span class="text-xs text-stone-400 block italic font-semibold mt-2">📍 Espaço reservado para colocar as vossas fotos reais em ação!</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECÇÃO SERVIÇOS -->
    <section id="servicos" class="py-20 bg-[#02000a] border-y border-white/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-16">
            
            <div class="text-center space-y-3">
                <span class="text-sm font-bold text-neon-purple uppercase tracking-widest font-extrabold">O que fazemos de melhor</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white">Soluções Criativas para Crescer</h2>
                <p class="text-stone-300 text-sm sm:text-base max-w-xl mx-auto font-light">Desenvolvemos todo o ecossistema digital que a sua marca necessita para liderar o mercado de Moçambique.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                
                <!-- Serviço 1: Redes Sociais -->
                <div class="glass-card p-8 rounded-3xl space-y-4 hover:-translate-y-1 transition duration-300">
                    <div class="w-12 h-12 bg-agency-500/10 text-neon-purple rounded-xl flex items-center justify-center text-xl">
                        <i class="fa-solid fa-hashtag"></i>
                    </div>
                    <h3 class="font-serif font-bold text-xl sm:text-2xl text-white">Gestão Profissional de Redes</h3>
                    <p class="text-stone-200 text-sm sm:text-base leading-relaxed font-normal">
                        Criamos publicações diárias, vídeos curtos irresistíveis para Reels/TikTok, planeamos o seu calendário editorial e gerimos campanhas de anúncios patrocinados (Meta e TikTok Ads) focadas em captação direta de clientes.
                    </p>
                    <ul class="text-sm text-stone-300 space-y-1.5 pt-2 font-bold">
                        <li>• Planeamento estratégico mensal</li>
                        <li>• Anúncios Patrocinados Focados em WhatsApp</li>
                        <li>• Criação de Textos de Venda (Copywriting)</li>
                    </ul>
                </div>

                <!-- Serviço 2: Websites Profissionais (Regularizado e Acessível) -->
                <div class="glass-card p-8 rounded-3xl space-y-4 hover:-translate-y-1 transition duration-300 border border-emerald-500/30 relative">
                    <div class="absolute top-4 right-4 bg-emerald-600 text-white font-bold text-[9px] py-1 px-3 rounded-full uppercase tracking-wider">
                        SUPER ACESSÍVEL!
                    </div>
                    
                    <div class="w-12 h-12 bg-neon-cyan/10 text-neon-cyan rounded-xl flex items-center justify-center text-xl">
                        <i class="fa-solid fa-code"></i>
                    </div>
                    <h3 class="font-serif font-bold text-xl sm:text-2xl text-white">Desenvolvimento Web Pro</h3>
                    <p class="text-stone-200 text-sm sm:text-base leading-relaxed font-normal">
                        Criamos sites profissionais, rápidos e perfeitamente adaptados para o telemóvel para converter visitantes em clientes. Ajustamos os preços de forma justa e acessível para qualquer empresa começar a faturar mais online.
                    </p>
                    <ul class="text-sm text-stone-300 space-y-1.5 pt-2 font-bold">
                        <li>• Páginas de Venda Rápidas e Otimizadas</li>
                        <li>• Design Moderno e Integração com WhatsApp</li>
                        <li>• Domínio Próprio e Contas de Email Grátis</li>
                    </ul>
                </div>

                <!-- Serviço 3: Branding & Identidade -->
                <div class="glass-card p-8 rounded-3xl space-y-4 hover:-translate-y-1 transition duration-300">
                    <div class="w-12 h-12 bg-amber-500/10 text-amber-500 rounded-xl flex items-center justify-center text-xl">
                        <i class="fa-solid fa-palette"></i>
                    </div>
                    <h3 class="font-serif font-bold text-xl sm:text-2xl text-white">Identidade Visual & Logótipo</h3>
                    <p class="text-stone-200 text-sm sm:text-base leading-relaxed font-normal">
                        Criamos logótipos únicos e impactantes para a sua empresa, definindo as cores de marca corretas e desenvolvendo peças gráficas que transmitem seriedade e profissionalismo absoluto no mercado.
                    </p>
                    <ul class="text-sm text-stone-300 space-y-1.5 pt-2 font-bold">
                        <li>• Criação de Logótipos Profissionais Vetoriais</li>
                        <li>• Paleta de Cores e Tipografias Completas</li>
                        <li>• Design para Flyers, Menus e Merchandising</li>
                    </ul>
                </div>

            </div>
        </div>
    </section>

    <!-- SECÇÃO EQUIPAMENTOS: TRIPÉS, GIMBALS E LUZES JUNTOS (Drone 4K - 5000 MT) -->
    <section id="equipamento" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-16">
        
        <div class="flex flex-col lg:flex-row justify-between items-start lg:items-end gap-6">
            <div class="space-y-2">
                <span class="text-sm font-bold text-neon-purple uppercase tracking-widest font-extrabold">Produção de Alta Resolução</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white leading-tight">A Nossa Estrutura de Gravação</h2>
                <p class="text-stone-200 text-sm sm:text-base max-w-xl">Trabalhamos com equipamentos de última geração perfeitamente combinados para garantir um resultado visual digno de cinema.</p>
            </div>
            <!-- Destaque de Preço do Drone -->
            <div class="bg-agency-900 border border-agency-500/30 p-5 rounded-3xl text-center shadow-lg relative min-w-[220px]">
                <span class="text-[9px] font-bold text-gold-400 uppercase tracking-wider block">Serviço de Drone DJI</span>
                <span class="text-3xl font-extrabold text-white block mt-1">5 000 MT</span>
                <span class="text-xs text-stone-300 font-bold">Sessão / Voo em Nampula</span>
            </div>
        </div>

        <!-- Galeria Interativa de Equipamento Reais -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            
            <!-- Equipamento 1: Drone 4K -->
            <div class="bg-white/5 rounded-3xl border border-white/5 overflow-hidden shadow-lg flex flex-col justify-between group">
                <div class="h-56 relative overflow-hidden bg-black">
                    <!-- Foto de Drone Profissional -->
                    <img src="https://images.unsplash.com/photo-1527977966376-1c8408f9f108?auto=format&fit=crop&w=600&q=80" alt="Drone Fotografia Profissional" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <span class="absolute top-3 left-3 bg-agency-950/80 text-gold-400 border border-gold-500/30 text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wider backdrop-blur-sm">Imagens Aéreas Únicas</span>
                </div>
                <div class="p-6 space-y-3">
                    <h4 class="font-serif font-bold text-lg sm:text-xl text-white">Drones DJI de Alta Resolução (4K)</h4>
                    <p class="text-stone-200 text-sm leading-relaxed font-normal">
                        Vistas aéreas incríveis que dão escala, prestígio e autoridade ao seu negócio físico. Ideal para hotéis, imobiliárias, armazéns e grandes restaurantes.
                    </p>
                </div>
                <div class="p-6 pt-0 border-t border-white/5 mt-4 flex items-center justify-between">
                    <span class="text-sm sm:text-base font-bold text-white">Preço por Voo</span>
                    <span class="text-lg sm:text-xl font-black text-neon-purple">5 000 MT</span>
                </div>
            </div>

            <!-- Equipamento 2: Câmaras Profissionais -->
            <div class="bg-white/5 rounded-3xl border border-white/5 overflow-hidden shadow-lg flex flex-col justify-between group">
                <div class="h-56 relative overflow-hidden bg-black">
                    <!-- Foto de Câmaras de topo -->
                    <img src="https://images.unsplash.com/photo-1516035069371-29a1b244cc32?auto=format&fit=crop&w=600&q=80" alt="Câmara Profissional e Lentes" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                </div>
                <div class="p-6 space-y-3">
                    <h4 class="font-serif font-bold text-lg sm:text-xl text-white">Câmaras Mirrorless Profissionais</h4>
                    <p class="text-stone-200 text-sm leading-relaxed font-normal">
                        Sensores modernos de alta definição e lentes de grande abertura para captar fotografias extremamente nítidas e vídeos com focagem impecável dos seus produtos.
                    </p>
                </div>
                <div class="p-6 pt-0 border-t border-white/5 mt-4 flex items-center justify-between">
                    <span class="text-sm sm:text-base font-bold text-white">Incluído</span>
                    <span class="text-xs sm:text-sm text-stone-300 uppercase font-bold">Nos Nossos Planos</span>
                </div>
            </div>

            <!-- Equipamento 3: Tripés, Estabilizadores (Gimbals) e Iluminação JUNTOS -->
            <div class="bg-white/5 rounded-3xl border border-white/5 overflow-hidden shadow-lg flex flex-col justify-between group">
                <div class="h-56 relative overflow-hidden bg-black">
                    <!-- Foto Unificada: Tripé, Gimbal e Iluminação Led trabalhando em conjunto no local -->
                    <img src="https://images.unsplash.com/photo-1622737133809-d95047b9e673?auto=format&fit=crop&w=600&q=80" alt="Tripé profissional estabilizador gimbal e painel de iluminação juntos" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    <span class="absolute top-3 left-3 bg-emerald-600/90 text-white border border-emerald-500/30 text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wider backdrop-sm">Estabilização & Luz</span>
                </div>
                <div class="p-6 space-y-3">
                    <h4 class="font-serif font-bold text-lg sm:text-xl text-white">Tripés, Gimbals & Luzes RGB</h4>
                    <p class="text-stone-200 text-sm leading-relaxed font-normal">
                        Estabilizadores eletrónicos (Gimbals de 3 eixos), tripés de alumínio e iluminadores de alta fidelidade cromática para garantir gravações sem tremores e perfeitamente iluminadas no terreno.
                    </p>
                </div>
                <div class="p-6 pt-0 border-t border-white/5 mt-4 flex items-center justify-between">
                    <span class="text-sm sm:text-base font-bold text-white">Garantia</span>
                    <span class="text-xs sm:text-sm text-stone-300 uppercase font-bold">Produção Fluida</span>
                </div>
            </div>

        </div>
    </section>

    <!-- SECÇÃO PLANOS DE MARKETING (Tabela de preços oficial do PDF - PLANOS EM PRIMEIRO LUGAR) -->
    <section id="planos" class="py-20 bg-[#02000a] border-t border-b border-white/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-16">
            
            <div class="text-center space-y-3">
                <span class="text-sm font-bold text-neon-purple uppercase tracking-widest font-extrabold">Investimento Inteligente</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white">Escolha o Seu Plano de Crescimento</h2>
                <p class="text-stone-200 text-sm sm:text-base max-w-xl mx-auto font-light">
                    Ajudámos dezenas de empresas em Nampula e arredores a crescer de forma exponencial. Escolha o vosso plano ideal para começar!
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                
                <!-- Plano 1: Plano Presença (15 000 MT) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl transition relative">
                    <div class="space-y-4">
                        <span class="text-[10px] text-stone-400 uppercase tracking-widest font-extrabold block">Ideal para começar</span>
                        <h4 class="font-serif font-bold text-2xl text-white">Plano Presença</h4>
                        <div class="h-px bg-white/5 my-2"></div>
                        <p class="text-stone-200 text-sm leading-relaxed font-normal">
                            Desenvolvido para criar a base sólida do seu marketing digital em Moçambique e garantir um fluxo inicial constante de potenciais clientes no seu WhatsApp.
                        </p>
                        
                        <!-- Valor Real PDF -->
                        <div class="pt-2">
                            <span class="text-3xl sm:text-4xl font-black text-white">15 000 MT</span>
                            <span class="text-sm text-stone-400">/ Mês</span>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-3 pt-4 border-t border-white/10 font-medium">
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>8 Publicações Mensais</b> Personalizadas</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>Design de Imagens</b> de Alta Qualidade</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Configuração de <b>Anúncios Patrocinados</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Escrita Criativa de <b>Legendas & Copys</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>Relatório Mensal</b> de Desempenho</li>
                        </ul>
                    </div>
                    <div class="pt-6 border-t border-white/5">
                        <a href="https://wa.me/258852508924?text=Olá! Gostaria de iniciar o Plano Presença de 15.000 MT." target="_blank" class="block w-full text-center bg-white/5 border border-white/10 hover:bg-white/10 text-white font-bold py-3.5 rounded-xl transition text-xs uppercase tracking-wider">
                            Iniciar Plano Presença 📲
                        </a>
                    </div>
                </div>

                <!-- Plano 2: Plano Premium (Destaque Campeão de Vendas - 20 500 MT) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl transition border-2 border-agency-500/50 relative">
                    <div class="absolute -top-3 right-6 bg-gradient-to-r from-agency-500 to-neon-purple text-white font-black text-[9px] py-1.5 px-4 rounded-full uppercase tracking-wider shadow-md">
                        RECOMENDADO • ALTA PERFORMANCE
                    </div>
                    
                    <div class="space-y-4">
                        <span class="text-[10px] text-neon-purple uppercase tracking-widest font-extrabold block">Domínio Completo e Captação</span>
                        <h4 class="font-serif font-bold text-2xl text-white">Plano Premium</h4>
                        <div class="h-px bg-white/5 my-2"></div>
                        <p class="text-stone-200 text-sm leading-relaxed font-normal">
                            O nosso plano campeão de resultados! Unimos filmagens dinâmicas, fotografias profissionais do seu negócio físico e uma gestão focada no aumento do volume de faturação diário.
                        </p>
                        
                        <!-- Valor Real PDF -->
                        <div class="pt-2">
                            <span class="text-3xl sm:text-4xl font-black text-white">20 500 MT</span>
                            <span class="text-sm text-stone-400">/ Mês</span>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-3 pt-4 font-bold border-t border-white/10">
                            <li class="text-purple-300"><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> 12 Publicações (Imagens + Reels)</li>
                            <li class="text-purple-300"><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> 1 Sessão Fotográfica / Vídeo no Local</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Gestão de <b>Campanhas de WhatsApp</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Monitorização de <b>Anúncios (Patrocinados)</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>Relatório Analítico</b> de Resultados</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Apoio Estratégico com <b>Diretor de Conta</b></li>
                        </ul>
                    </div>
                    <div class="pt-6 border-t border-white/5">
                        <a href="https://wa.me/258852508924?text=Olá! Gostaria de aderir ao Plano Premium de 20.500 MT para o meu negócio." target="_blank" class="block w-full text-center bg-gradient-to-r from-agency-500 to-agency-700 hover:from-agency-600 hover:to-agency-800 text-white font-extrabold py-3.5 rounded-xl transition text-xs uppercase tracking-wider shadow-lg shadow-agency-600/20">
                            Ativar Plano Premium ⚡
                        </a>
                    </div>
                </div>

                <!-- Plano 3: Plano VIP Personalizado (28 500 MT) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl transition">
                    <div class="space-y-4">
                        <span class="text-[10px] text-stone-400 uppercase tracking-widest font-extrabold block">Máxima Escala & Prestígio</span>
                        <h4 class="font-serif font-bold text-2xl text-white">Plano VIP Personalizado</h4>
                        <div class="h-px bg-white/5 my-2"></div>
                        <p class="text-stone-300 text-sm leading-relaxed font-normal">
                            Desenhado para empresas que pretendem liderança absoluta no ecossistema digital. Inclui desenvolvimento de websites, campanhas de tráfego complexas e sessões aéreas.
                        </p>
                        
                        <!-- Valor Real PDF -->
                        <div class="pt-2">
                            <span class="text-3xl sm:text-4xl font-black text-white">28 500 MT</span>
                            <span class="text-sm text-stone-400">/ Mês</span>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-3 pt-4 border-t border-white/10 font-medium">
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Frequência <b>Diária de Conteúdos</b></li>
                            <li class="text-cyan-300"><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Sessão de <b>Drone 4K incluída</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>Criação de Web Site</b> Profissional</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Consultoria de <b>Branding & Identidade</b></li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> <b>Coprodução e Roteiros</b> para Vídeos</li>
                        </ul>
                    </div>
                    <div class="pt-6 border-t border-white/5">
                        <a href="https://wa.me/258852508924?text=Olá! Gostaria de marcar uma reunião para estruturar o meu Plano VIP Personalizado de 28.500 MT." target="_blank" class="block w-full text-center bg-white/5 border border-white/10 hover:bg-white/10 text-white font-bold py-3.5 rounded-xl transition text-xs uppercase tracking-wider">
                            Montar Plano à Medida 📲
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECÇÃO: TABELA DE PREÇOS DE WEBSITES REGULARIZADOS -->
    <section id="websites" class="py-20 bg-gradient-to-b from-[#02000a] to-[#050010] border-b border-white/5">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-16">
            
            <div class="text-center space-y-3">
                <span class="text-sm font-bold text-neon-cyan uppercase tracking-widest font-extrabold">A Sua Empresa 24 Horas no Ar</span>
                <h2 class="text-3xl sm:text-5xl font-serif font-bold text-white leading-tight">Criação de Web Sites Profissionais</h2>
                <p class="text-stone-300 text-sm sm:text-base max-w-xl mx-auto">
                    Desenvolvemos estruturas otimizadas e com foco na conversão para garantir que a sua marca tenha o melhor posicionamento digital de Moçambique.
                </p>
            </div>

            <!-- Tabela Dinâmica de Websites -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                
                <!-- Website Tipo 1: Landing Page (Página Única) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl border border-white/5 relative">
                    <div class="space-y-4">
                        <div class="flex justify-between items-center">
                            <span class="text-[9px] text-emerald-400 uppercase tracking-widest font-extrabold bg-emerald-500/10 px-2.5 py-1 rounded-full">Altamente Recomendada</span>
                            <span class="text-[10px] text-stone-500">Única Parcela</span>
                        </div>
                        <h4 class="font-serif font-bold text-xl text-white">Landing Page Vendedora</h4>
                        <p class="text-stone-400 text-xs sm:text-sm leading-relaxed font-light">
                            Uma página de alta conversão ideal para campanhas de anúncios e para apresentar um produto ou serviço específico, guiando o cliente direto ao seu WhatsApp.
                        </p>
                        
                        <!-- Preços -->
                        <div class="pt-4 space-y-1">
                            <span class="text-stone-500 line-through text-xs">Antes: 15 000 MT</span>
                            <div class="flex items-baseline gap-2">
                                <span class="text-3xl font-black text-white">8 500 MT</span>
                                <span class="text-xs text-stone-400">Preço Fixo</span>
                            </div>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-2.5 pt-2 border-t border-white/10 font-bold">
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> 1 Página de Alto Impacto</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Design Adaptado ao Telemóvel</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Atendimento Integrado WhatsApp</li>
                            <li><i class="fa-solid fa-check text-emerald-400 mr-2 text-base"></i> Configuração de Pixel de Rastreio</li>
                        </ul>
                    </div>
                    <div>
                        <a href="https://wa.me/258852508924?text=Olá! Gostava de saber mais sobre a Landing Page de 8.500 MT." target="_blank" class="block w-full text-center bg-white/5 hover:bg-white/10 text-white font-bold py-3 rounded-xl transition text-xs uppercase tracking-wider">
                            Quero o meu Website 📲
                        </a>
                    </div>
                </div>

                <!-- Website Tipo 2: Site Institucional (Destaque Pro) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl border-2 border-neon-cyan/40 relative">
                    <div class="absolute -top-3 right-6 bg-gradient-to-r from-neon-cyan to-agency-500 text-slate-950 font-black text-[9px] py-1.5 px-4 rounded-full uppercase tracking-wider shadow-md">
                        Mais Procurado • Autoridade Completa
                    </div>
                    
                    <div class="space-y-4">
                        <div class="flex justify-between items-center">
                            <span class="text-[9px] text-neon-cyan uppercase tracking-widest font-extrabold bg-neon-cyan/10 px-2.5 py-1 rounded-full">Completo</span>
                            <span class="text-[10px] text-stone-500">Única Parcela</span>
                        </div>
                        <h4 class="font-serif font-bold text-xl text-white">Site Institucional Multi-página</h4>
                        <p class="text-stone-400 text-xs sm:text-sm leading-relaxed font-light">
                            O site ideal para apresentar a história da sua empresa, serviços detalhados, equipa, galeria de fotografias e formulário de contacto profissional.
                        </p>
                        
                        <!-- Preços -->
                        <div class="pt-4 space-y-1">
                            <span class="text-stone-500 line-through text-xs">Antes: 25 000 MT</span>
                            <div class="flex items-baseline gap-2">
                                <span class="text-3xl font-black text-neon-cyan">14 500 MT</span>
                                <span class="text-xs text-stone-400">Preço Fixo</span>
                            </div>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-2.5 pt-2 border-t border-white/10 font-bold">
                            <li><i class="fa-solid fa-check text-neon-cyan mr-2 text-base"></i> Até 5 Páginas Completas</li>
                            <li><i class="fa-solid fa-check text-neon-cyan mr-2 text-base"></i> Atendimento integrado WhatsApp</li>
                            <li><i class="fa-solid fa-check text-neon-cyan mr-2 text-base"></i> Galeria de Fotos e Bastidores</li>
                            <li><i class="fa-solid fa-check text-neon-cyan mr-2 text-base"></i> Otimização para pesquisa no Google (SEO)</li>
                        </ul>
                    </div>
                    <div>
                        <a href="https://wa.me/258852508924?text=Olá! Gostava de saber mais sobre o Website Institucional de 14.500 MT." target="_blank" class="block w-full text-center bg-gradient-to-r from-neon-cyan to-agency-500 hover:from-cyan-500 hover:to-agency-600 text-slate-950 font-black py-3 rounded-xl transition text-xs uppercase tracking-wider shadow-lg shadow-cyan-500/20">
                            Garantir Site Profissional 🚀
                        </a>
                    </div>
                </div>

                <!-- Website Tipo 3: Loja Online (E-commerce - 32 000 MT até 50 produtos com WhatsApp Integrado) -->
                <div class="glass-card p-8 rounded-3xl flex flex-col justify-between space-y-6 hover:shadow-xl border border-white/5 relative">
                    <div class="space-y-4">
                        <div class="flex justify-between items-center">
                            <span class="text-[9px] text-neon-purple uppercase tracking-widest font-extrabold bg-neon-purple/10 px-2.5 py-1 rounded-full">Vendas Automáticas</span>
                            <span class="text-[10px] text-stone-500">Única Parcela</span>
                        </div>
                        <h4 class="font-serif font-bold text-xl text-white">E-commerce / Loja Digital</h4>
                        <p class="text-stone-400 text-xs sm:text-sm leading-relaxed font-light">
                            Desenvolvido para marcas que pretendem listar os seus produtos, gerir inventário de forma limpa, receber encomendas diretas e centralizar os pagamentos.
                        </p>
                        
                        <!-- Preços Atualizados -->
                        <div class="pt-4 space-y-1">
                            <span class="text-stone-500 line-through text-xs">Antes: 45 000 MT</span>
                            <div class="flex items-baseline gap-2">
                                <span class="text-3xl font-black text-white">32 000 MT</span>
                                <span class="text-xs text-stone-400">Até 50 Produtos</span>
                            </div>
                        </div>

                        <ul class="text-sm sm:text-base text-stone-300 space-y-2.5 pt-2 border-t border-white/10 font-bold">
                            <li class="text-emerald-400"><i class="fa-solid fa-check mr-2 text-base"></i> Receba Encomendas via WhatsApp</li>
                            <li class="text-emerald-400"><i class="fa-solid fa-check mr-2 text-base"></i> Receba Leads Direto no WhatsApp</li>
                            <li class="text-emerald-400"><i class="fa-solid fa-check mr-2 text-base"></i> Atendimento Integrado WhatsApp</li>
                            <li><i class="fa-solid fa-check text-neon-purple mr-2 text-base"></i> Cadastro de até 50 Produtos</li>
                            <li><i class="fa-solid fa-check text-neon-purple mr-2 text-base"></i> Integração de Pagamento Móvel (M-Pesa)</li>
                            <li><i class="fa-solid fa-check text-neon-purple mr-2 text-base"></i> Área de Gestão de Clientes e Pedidos</li>
                        </ul>
                    </div>
                    <div>
                        <a href="https://wa.me/258852508924?text=Olá! Gostava de saber mais sobre a Loja Online de 32.000 MT." target="_blank" class="block w-full text-center bg-white/5 hover:bg-white/10 text-white font-bold py-3 rounded-xl transition text-xs uppercase tracking-wider">
                            Falar com Programador 📲
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECÇÃO CONTACTO E LOCALIZAÇÃO (Foco em conversão direta) -->
    <section id="contacto" class="py-20 max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
        <div class="bg-gradient-to-br from-agency-950 to-[#050010] rounded-[2.5rem] p-8 sm:p-12 border border-white/5 relative overflow-hidden flex flex-col md:flex-row items-center justify-between gap-12">
            
            <div class="space-y-6 text-center md:text-left flex-grow">
                <span class="text-xs uppercase tracking-widest text-neon-purple font-bold">Contacto Imediato</span>
                <h3 class="text-3xl sm:text-4xl font-serif font-bold text-white leading-tight">Vamos impulsionar o seu negócio hoje?</h3>
                <p class="text-stone-300 text-sm sm:text-base leading-relaxed max-w-md mx-auto md:mx-0 font-light">
                    Não perca tempo nem dinheiro com estratégias que não trazem novos clientes. Agende agora uma conversa rápida com o nosso especialista e descubra o plano ideal para a sua empresa.
                </p>
                <div class="space-y-3 text-stone-400 text-sm font-bold">
                    <p><i class="fa-solid fa-location-dot text-red-500 mr-2"></i> Nampula, Moçambique</p>
                    <p><i class="fa-brands fa-whatsapp text-emerald-400 mr-2"></i> +258 85 250 8924</p>
                </div>
            </div>

            <!-- Formulário Rápido para simulação ou redirecionamento -->
            <div class="bg-white/5 p-6 rounded-3xl border border-white/10 max-w-sm w-full space-y-4">
                <h4 class="font-serif font-bold text-lg text-white">Solicitar Diagnóstico Grátis</h4>
                <form id="leadForm" onsubmit="handleLeadSubmit(event)" class="space-y-3 text-xs">
                    <input type="text" id="leadName" required placeholder="O seu nome..." class="w-full bg-[#050010] border border-white/10 rounded-xl p-3 text-white focus:outline-none focus:border-agency-500 transition">
                    <input type="tel" id="leadPhone" required placeholder="O seu telefone..." class="w-full bg-[#050010] border border-white/10 rounded-xl p-3 text-white focus:outline-none focus:border-agency-500 transition">
                    <button type="submit" class="w-full bg-agency-600 hover:bg-agency-500 text-white font-extrabold py-3.5 rounded-xl transition uppercase tracking-wider text-[10px]">
                        Enviar Mensagem Directa 🚀
                    </button>
                </form>
            </div>

        </div>
    </section>

    <!-- RODAPÉ DA PÁGINA (Footer) -->
    <footer class="bg-[#02000a] text-stone-400 py-16 px-4 sm:px-6 lg:px-8 border-t border-white/5 text-center sm:text-left">
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-12">
            <div class="space-y-4">
                <span class="text-xl font-serif font-black text-white tracking-wider">MD<span class="text-neon-purple font-medium">AGÊNCIA</span></span>
                <p class="text-xs text-stone-500 leading-relaxed max-w-sm mx-auto sm:mx-0">
                    Estratégias inovadoras, conteúdos com grande engajamento e web design profissional feitos sob medida para vender no mercado de Moçambique.
                </p>
            </div>
            <div>
                <h4 class="font-bold text-white text-xs uppercase tracking-widest mb-4">Nossos Serviços</h4>
                <ul class="space-y-3 text-xs text-stone-500 font-semibold">
                    <li><a href="#servicos" class="hover:text-neon-purple transition">Gestão de Redes Sociais</a></li>
                    <li><a href="#websites" class="hover:text-neon-purple transition">Criação de Web Sites</a></li>
                    <li><a href="#equipamento" class="hover:text-neon-purple transition">Filmagens com Drone 4K</a></li>
                    <li><a href="#servicos" class="hover:text-neon-purple transition">Identidade Visual & Branding</a></li>
                </ul>
            </div>
            <div>
                <h4 class="font-bold text-white text-xs uppercase tracking-widest mb-4">Contacto Direto</h4>
                <ul class="space-y-3 text-xs text-stone-400 font-bold">
                    <li><i class="fa-solid fa-phone text-neon-purple mr-2"></i> +258 85 250 8924</li>
                    <li><i class="fa-solid fa-envelope text-neon-purple mr-2"></i> contacto@mdagency.com</li>
                    <li><i class="fa-solid fa-location-dot text-neon-purple mr-2"></i> Nampula, Moçambique</li>
                </ul>
            </div>
            <div>
                <h4 class="font-bold text-white text-xs uppercase tracking-widest mb-4">Acompanhe-nos</h4>
                <p class="text-xs text-stone-500 mb-4 font-light">Siga a nossa equipa de criativos nas nossas redes oficiais.</p>
                <div class="flex gap-3 justify-center sm:justify-start">
                    <a href="https://instagram.com/md_agency_mz" target="_blank" class="w-10 h-10 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-stone-400 hover:text-white hover:bg-agency-500/20 transition-all"><i class="fa-brands fa-instagram text-base"></i></a>
                    <a href="https://tiktok.com/@md_agency_mz" target="_blank" class="w-10 h-10 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-stone-400 hover:text-white hover:bg-agency-500/20 transition-all"><i class="fa-brands fa-tiktok text-sm"></i></a>
                    <a href="https://wa.me/258852508924" target="_blank" class="w-10 h-10 rounded-full bg-white/5 border border-white/10 flex items-center justify-center text-stone-400 hover:text-white hover:bg-agency-500/20 transition-all"><i class="fa-brands fa-whatsapp text-base"></i></a>
                </div>
            </div>
        </div>
        <div class="max-w-7xl mx-auto border-t border-white/5 mt-12 pt-6 text-center text-xs text-stone-600 flex flex-col sm:flex-row justify-between items-center gap-4">
            <p>© 2026 MD Agência MZ. Todos os direitos reservados.</p>
            <div class="flex gap-4 text-[10px] uppercase tracking-wider">
                <a href="#" class="hover:text-neon-purple transition">Política de Privacidade</a>
                <span>•</span>
                <a href="#" class="hover:text-neon-purple transition">Termos de Serviço</a>
            </div>
        </div>
    </footer>

    <!-- MODAL DE CONFIRMAÇÃO DO DIAGNÓSTICO (SUBSTITUI ALERTS) -->
    <div id="alertModal" class="fixed inset-0 bg-black/85 flex items-center justify-center p-4 z-50 hidden">
        <div class="bg-[#050010] rounded-3xl p-6 sm:p-8 max-w-md w-full text-center space-y-4 shadow-2xl border border-white/10">
            <span id="modalIcon" class="text-5xl block animate-bounce">⚡</span>
            <h3 id="modalTitle" class="font-serif font-bold text-2xl text-white uppercase tracking-wide">Mensagem Recebida</h3>
            <p id="modalBody" class="text-stone-300 text-xs sm:text-sm leading-relaxed">Detalhe...</p>
            <button onclick="closeModal()" class="bg-agency-600 hover:bg-agency-500 text-white font-bold py-3 px-8 rounded-full text-xs uppercase tracking-wide transition">
                Fechar Janela
            </button>
        </div>
    </div>

    <!-- CONTROLADORES JAVASCRIPT DO SISTEMA -->
    <script>
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Enviar os dados do lead diretamente para o WhatsApp do Ricardo
        function handleLeadSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('leadName').value;
            const phone = document.getElementById('leadPhone').value;

            // Criar a mensagem encriptada para envio no WhatsApp
            const customMessage = `Olá MD Agência! O meu nome é ${name} (${phone}) e gostaria de receber o meu Diagnóstico de Marketing Gratuito no WhatsApp.`;
            const whatsappUrl = `https://wa.me/258852508924?text=${encodeURIComponent(customMessage)}`;

            // Exibir popup de feedback e redirecionar
            showAlert(
                '🚀',
                'Obrigado!',
                'O seu pedido foi gerado com sucesso. Vamos redirecioná-lo agora mesmo para o nosso WhatsApp para falarmos sobre o seu projeto.'
            );

            // Redireciona para o WhatsApp após 2.5 segundos de delay
            setTimeout(() => {
                window.open(whatsappUrl, '_blank');
            }, 2500);

            event.target.reset();
        }

        // Funções para controle do modal customizado
        function showAlert(icon, title, body) {
            document.getElementById('modalIcon').innerText = icon;
            document.getElementById('modalTitle').innerText = title;
            document.getElementById('modalBody').innerHTML = body;
            document.getElementById('alertModal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('alertModal').classList.add('hidden');
        }
    </script>
</body>
</html>
