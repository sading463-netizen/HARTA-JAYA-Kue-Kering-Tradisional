<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="HARTA JAYA - Jajanan kering dengan cita rasa autentik dan bahan berkualitas.">
    <title>HARTA JAYA - Kue Kering Tradisional Berkualitas</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;500;600;700&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        cream: '#FDF6E3',
                        warmBg: '#FAF3E8',
                        terracotta: '#C4654A',
                        terracottaDark: '#A84E35',
                        brown: '#5D4037',
                        brownLight: '#8D6E63',
                        gold: '#D4A574',
                        goldLight: '#E8C9A0',
                    },
                    fontFamily: {
                        display: ['Playfair Display', 'serif'],
                        body: ['Nunito', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    
    <style>
        :root { --bg: #FDF6E3; --fg: #3E2723; --muted: #8D6E63; --accent: #C4654A; --accent-dark: #A84E35; --card: #FFFFFF; --border: #E8D5C4; --gold: #D4A574; }
        * { scroll-behavior: smooth; }
        body { font-family: 'Nunito', sans-serif; background-color: var(--bg); color: var(--fg); }
        .font-display { font-family: 'Playfair Display', serif; }
        
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes float { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-10px); } }
        @keyframes pulse-ring { 0% { transform: scale(1); opacity: 1; } 100% { transform: scale(1.5); opacity: 0; } }
        
        .animate-fade-up { animation: fadeInUp 0.8s ease-out forwards; }
        .animate-float { animation: float 3s ease-in-out infinite; }
        
        .reveal { opacity: 0; transform: translateY(30px); transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1); }
        .reveal.active { opacity: 1; transform: translateY(0); }
        
        @media (prefers-reduced-motion: reduce) { .reveal, .animate-fade-up, .animate-float { animation: none; opacity: 1; transform: none; } }
        
        .pattern-bg { background-image: radial-gradient(circle at 20% 80%, rgba(212, 165, 116, 0.15) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(196, 101, 74, 0.1) 0%, transparent 50%); }
        .hero-pattern { background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23D4A574' fill-opacity='0.08'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E"); }
        
        .menu-card { transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1); }
        .menu-card:hover { transform: translateY(-8px); box-shadow: 0 20px 40px rgba(93, 64, 55, 0.15); }
        .menu-card:hover .menu-image { transform: scale(1.08); }
        .menu-image { transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1); }
        
        .btn-primary { background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%); transition: all 0.3s ease; position: relative; overflow: hidden; }
        .btn-primary::before { content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent); transition: left 0.5s ease; }
        .btn-primary:hover::before { left: 100%; }
        .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 20px rgba(196, 101, 74, 0.35); }
        
        .wa-float { position: fixed; bottom: 24px; right: 24px; z-index: 999; animation: float 3s ease-in-out infinite; }
        .wa-float::before { content: ''; position: absolute; width: 100%; height: 100%; background-color: #25D366; border-radius: 50%; animation: pulse-ring 1.5s infinite; }
        
        .nav-link { position: relative; }
        .nav-link::after { content: ''; position: absolute; bottom: -4px; left: 0; width: 0; height: 2px; background-color: var(--accent); transition: width 0.3s ease; }
        .nav-link:hover::after { width: 100%; }
        
        .mobile-menu { transform: translateX(100%); transition: transform 0.3s ease; }
        .mobile-menu.active { transform: translateX(0); }
        
        button:focus-visible, a:focus-visible { outline: 3px solid var(--accent); outline-offset: 2px; }
    </style>
</head>
<body class="font-body antialiased">
    
    <!-- Header -->
    <header id="header" class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 bg-cream/95 backdrop-blur-md shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <nav class="flex items-center justify-between h-16 lg:h-20">
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <img src="https://z-cdn-media.chatglm.cn/files/579bc5e8-23ac-477a-a397-e55188254173.jpg?auth_key=1872718070-52341495cfae481d9ba1a804f1511838-0-4c389e2eb65b1f3965399572e3a0139d" alt="Logo HARTA JAYA" class="h-10 w-10 lg:h-12 lg:w-12 rounded-full object-cover shadow-lg group-hover:shadow-terracotta/30 transition-shadow">
                    <div>
                        <h1 class="font-display text-lg lg:text-xl font-bold text-brown">HARTA JAYA</h1>
                        <p class="text-xs text-brownLight hidden sm:block">Kue Kering Tradisional</p>
                    </div>
                </a>
                
                <!-- Desktop Navigation -->
                <ul class="hidden lg:flex items-center gap-8">
                    <li><a href="#beranda" class="nav-link text-brown font-medium hover:text-terracotta transition-colors">Beranda</a></li>
                    <li><a href="#tentang" class="nav-link text-brown font-medium hover:text-terracotta transition-colors">Tentang Kami</a></li>
                    <li><a href="#menu" class="nav-link text-brown font-medium hover:text-terracotta transition-colors">Menu</a></li>
                    <li><a href="#testimoni" class="nav-link text-brown font-medium hover:text-terracotta transition-colors">Testimoni</a></li>
                    <li><a href="#kontak" class="nav-link text-brown font-medium hover:text-terracotta transition-colors">Kontak</a></li>
                </ul>
                
                <!-- CTA Button Desktop -->
                <a href="https://wa.me/6285792599030" target="_blank" rel="noopener" class="hidden lg:flex btn-primary text-white px-6 py-2.5 rounded-full font-semibold text-sm items-center gap-2">
                    <svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                    Pesan Sekarang
                </a>
                
                <!-- Mobile Menu Button -->
                <button id="menuToggle" class="lg:hidden p-2 text-brown hover:text-terracotta transition-colors" aria-label="Toggle menu">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
                </button>
            </nav>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobileMenu" class="mobile-menu fixed inset-y-0 right-0 w-72 bg-cream shadow-2xl lg:hidden">
            <div class="p-6">
                <button id="closeMenu" class="absolute top-4 right-4 p-2 text-brown hover:text-terracotta" aria-label="Close menu">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
                </button>
                <nav class="mt-12 space-y-4">
                    <a href="#beranda" class="block py-3 text-lg font-medium text-brown hover:text-terracotta border-b border-goldLight/50">Beranda</a>
                    <a href="#tentang" class="block py-3 text-lg font-medium text-brown hover:text-terracotta border-b border-goldLight/50">Tentang Kami</a>
                    <a href="#menu" class="block py-3 text-lg font-medium text-brown hover:text-terracotta border-b border-goldLight/50">Menu</a>
                    <a href="#testimoni" class="block py-3 text-lg font-medium text-brown hover:text-terracotta border-b border-goldLight/50">Testimoni</a>
                    <a href="#kontak" class="block py-3 text-lg font-medium text-brown hover:text-terracotta border-b border-goldLight/50">Kontak</a>
                </nav>
            </div>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section id="beranda" class="min-h-screen pt-20 lg:pt-0 flex items-center relative overflow-hidden pattern-bg hero-pattern">
        <div class="absolute top-20 right-10 w-64 h-64 bg-goldLight/20 rounded-full blur-3xl"></div>
        <div class="absolute bottom-20 left-10 w-80 h-80 bg-terracotta/10 rounded-full blur-3xl"></div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 lg:py-20">
            <div class="grid lg:grid-cols-2 gap-8 lg:gap-12 items-center">
                <div class="order-2 lg:order-1 text-center lg:text-left">
                    <span class="animate-fade-up inline-block px-4 py-1.5 bg-goldLight/50 text-brown rounded-full text-sm font-medium mb-4">Sejak 2005 Melayani dengan Cinta</span>
                    <h2 class="animate-fade-up font-display text-3xl sm:text-4xl lg:text-5xl xl:text-6xl font-bold text-brown leading-tight mb-6" style="animation-delay: 0.1s">
                        Rasakan Keunikan Kue Kering Tradisional 
                        <span class="text-terracotta">HARTA JAYA</span>
                    </h2>
                    <p class="animate-fade-up text-base lg:text-lg text-brownLight mb-8 max-w-xl mx-auto lg:mx-0" style="animation-delay: 0.2s">
                        Kue kering tradisional dari Harta Jaya adalah kuliner lokal yang tak terlupakan, setiap gigitannya membawa kita dalam perjalanan rasa nusantara yang kaya dan autentik.
                    </p>
                    <div class="animate-fade-up flex flex-col sm:flex-row gap-4 justify-center lg:justify-start" style="animation-delay: 0.3s">
                        <a href="https://wa.me/6285792599030?text=Halo,%20saya%20ingin%20memesan" target="_blank" rel="noopener" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg flex items-center justify-center gap-2">
                            <svg class="w-5 h-5" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                            Pesan Sekarang
                        </a>
                        <a href="#menu" class="bg-goldLight text-brown px-8 py-4 rounded-full font-semibold text-lg flex items-center justify-center gap-2 border-2 border-gold hover:bg-gold transition-colors">
                            Lihat Menu
                        </a>
                    </div>
                </div>
                
                <!-- Hero Image -->
                <div class="order-1 lg:order-2 relative">
                    <div class="animate-fade-right relative z-10" style="animation-delay: 0.2s">
                        <div class="relative aspect-square max-w-md mx-auto rounded-3xl overflow-hidden shadow-2xl">
                            <img src="https://z-cdn-media.chatglm.cn/files/6b061353-4433-43df-a0a4-942d423f3545.jpg?auth_key=1872718717-b55788fa82f94ff5b25a5a293e24a1c2-0-b8eb6b65371926692ddb147ee1448261" alt="Kue Kering Harta Jaya" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700">
                        </div>
                        <div class="absolute -bottom-4 -left-4 lg:-left-8 bg-white p-4 rounded-2xl shadow-xl animate-float">
                            <div class="flex items-center gap-3">
                                <div class="w-12 h-12 rounded-full bg-green-100 flex items-center justify-center">
                                    <svg class="w-6 h-6 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                </div>
                                <div>
                                    <p class="font-semibold text-brown">100% Halal</p>
                                    <p class="text-xs text-brownLight">Bahan Terjamin</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="absolute inset-0 bg-gradient-to-br from-goldLight to-terracotta/20 rounded-3xl transform rotate-6 -z-10"></div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Tentang Kami -->
    <section id="tentang" class="py-20 lg:py-28 bg-warmBg relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
                <div class="reveal relative">
                    <div class="relative">
                        <img src="https://z-cdn-media.chatglm.cn/files/22d8be0e-e735-4b8f-acab-1dfaade89d06.jpg?auth_key=1872718717-0a29add55be14a3d9967397493753d4e-0-90b87a847ebc616f5cc5cbb1b9948763" alt="Proses pembuatan" class="rounded-3xl shadow-2xl w-full">
                        <div class="absolute -bottom-6 -right-6 bg-terracotta text-white p-6 rounded-2xl shadow-xl">
                            <p class="font-display text-4xl font-bold">15+</p>
                            <p class="text-sm">Tahun Pengalaman</p>
                        </div>
                    </div>
                </div>
                
                <div class="reveal">
                    <span class="inline-block px-4 py-1.5 bg-terracotta/10 text-terracotta rounded-full text-sm font-medium mb-4">Tentang Kami</span>
                    <h3 class="font-display text-3xl lg:text-4xl font-bold text-brown mb-6">Cerita di Balik Hadirnya Harta Jaya</h3>
                    <div class="space-y-4 text-brownLight leading-relaxed">
                        <p><strong class="text-brown">HARTA JAYA</strong> Dimulai dengan sebuah keberanian kecil untuk merintis bisnis sendiri setelah tahun-tahun mengumpulkan wawasan.</p>
                        <p>Setiap kue kering kami dibuat dengan penuh ketelitian dan cinta, selalu segar karena dibuat setiap hari tanpa menggunakan pengawet.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Menu Section -->
    <section id="menu" class="py-20 lg:py-28 bg-cream relative">
        <div class="absolute inset-0 pattern-bg"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
            <div class="text-center mb-16 reveal">
                <span class="inline-block px-4 py-1.5 bg-goldLight text-brown rounded-full text-sm font-medium mb-4">Menu Kami</span>
                <h3 class="font-display text-3xl lg:text-4xl font-bold text-brown mb-4">Pilihan Kue Kering Tradisional</h3>
            </div>
            <div id="menuGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-8"></div>
        </div>
    </section>
    
    <!-- Testimoni Section -->
    <section id="testimoni" class="py-20 lg:py-28 bg-gradient-to-b from-warmBg to-cream relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
            <div class="text-center mb-16 reveal">
                <span class="inline-block px-4 py-1.5 bg-terracotta/10 text-terracotta rounded-full text-sm font-medium mb-4">Testimoni</span>
                <h3 class="font-display text-3xl lg:text-4xl font-bold text-brown mb-4">Kata Mereka Tentang Kami</h3>
            </div>
            <div id="testimonialGrid" class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto"></div>
        </div>
    </section>
    
    <!-- Kontak Section -->
    <section id="kontak" class="py-20 lg:py-28 bg-warmBg relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 reveal">
                <span class="inline-block px-4 py-1.5 bg-terracotta/10 text-terracotta rounded-full text-sm font-medium mb-4">Kontak</span>
                <h3 class="font-display text-3xl lg:text-4xl font-bold text-brown mb-4">Hubungi Kami</h3>
            </div>
            
            <div class="grid lg:grid-cols-2 gap-12">
                <div class="reveal space-y-8">
                    <div class="bg-white p-6 rounded-2xl shadow-lg flex gap-5">
                        <div class="w-14 h-14 rounded-xl bg-terracotta/10 flex items-center justify-center flex-shrink-0">
                            <svg class="w-7 h-7 text-terracotta" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/></svg>
                        </div>
                        <div>
                            <h4 class="font-semibold text-brown text-lg mb-1">Alamat</h4>
                            <p class="text-brownLight">Jl. Kereban Langit 1 No 4, Kelurahan Sading<br>Kecamatan Mengwi, Badung 80351</p>
                        </div>
                    </div>
                    
                    <div class="bg-white p-6 rounded-2xl shadow-lg flex gap-5">
                        <div class="w-14 h-14 rounded-xl bg-green-100 flex items-center justify-center flex-shrink-0">
                            <svg class="w-7 h-7 text-green-600" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                        </div>
                        <div>
                            <h4 class="font-semibold text-brown text-lg mb-1">WhatsApp Order</h4>
                            <a href="https://wa.me/6285792599030" target="_blank" class="text-terracotta hover:text-terracottaDark font-medium">085792599030</a>
                        </div>
                    </div>
                </div>
                
                <div class="reveal">
                    <div class="bg-white p-4 rounded-2xl shadow-lg h-full min-h-[400px]">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3944.5877744566847!2d115.17732481478158!3d-8.583339988702747!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd23f57177bb2b1%3A0x6f4d6c6d8c5e5f5e!2sMengwi%2C%20Badung%2C%20Bali!5e0!3m2!1sid!2sid!4v1620000000000!5m2!1sid!2sid" width="100%" height="100%" style="border:0; min-height: 380px; border-radius: 12px;" allowfullscreen="" loading="lazy"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer class="bg-brown text-cream py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-10 mb-12">
                <div class="lg:col-span-2">
                    <div class="flex items-center gap-3 mb-4">
                        <img src="https://z-cdn-media.chatglm.cn/files/579bc5e8-23ac-477a-a397-e55188254173.jpg?auth_key=1872718070-52341495cfae481d9ba1a804f1511838-0-4c389e2eb65b1f3965399572e3a0139d" alt="Logo HARTA JAYA" class="h-12 w-12 rounded-full object-cover">
                        <div>
                            <h4 class="font-display text-xl font-bold">HARTA JAYA</h4>
                            <p class="text-sm text-cream/70">Kue Kering Tradisional</p>
                        </div>
                    </div>
                    <p class="text-cream/80 mb-6 max-w-md">
                        Menghadirkan kelezatan jajanan tradisional dengan resep dan bahan berkualitas.
                    </p>
                </div>
                <div>
                    <h5 class="font-semibold text-lg mb-4">Link Cepat</h5>
                    <ul class="space-y-3">
                        <li><a href="#beranda" class="text-cream/80 hover:text-terracotta transition-colors">Beranda</a></li>
                        <li><a href="#tentang" class="text-cream/80 hover:text-terracotta transition-colors">Tentang Kami</a></li>
                        <li><a href="#menu" class="text-cream/80 hover:text-terracotta transition-colors">Menu</a></li>
                    </ul>
                </div>
                <div>
                    <h5 class="font-semibold text-lg mb-4">Kontak</h5>
                    <ul class="space-y-3 text-cream/80">
                        <li>Jl. Kereban Langit 1 No 4, Badung</li>
                        <li>+62 85792599030</li>
                    </ul>
                </div>
            </div>
            <div class="pt-8 border-t border-cream/20 flex flex-col md:flex-row justify-between items-center gap-4">
                <p class="text-cream/70 text-sm text-center md:text-left">2024 Harta Jaya. Hak Cipta Dilindungi.</p>
            </div>
        </div>
    </footer>
    
    <!-- WhatsApp Floating Button -->
    <a href="https://wa.me/6285792599030" target="_blank" class="wa-float w-16 h-16 bg-green-500 rounded-full flex items-center justify-center text-white shadow-lg hover:bg-green-600 hover:scale-110 transition-all" aria-label="Chat via WhatsApp">
        <svg class="w-8 h-8 relative z-10" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
    </a>
    
    <script>
        const menuData = [
            {
                id: 1,
                name: "Jaje Sengait Kotak",
                description: "Kue kering premium dengan lapisan gula aren, berbentuk bulat dan rasa manis",
                price: 6000,
                image: "https://z-cdn-media.chatglm.cn/files/4588ac59-810f-43d1-9dc0-d9d2994f2a87.jpg?auth_key=1872718717-cb977cbf6d2146d69269c255d753337c-0-4b0aed748dd096b4f694fc51717617f0",
                rating: 4.9,
                waLink: "https://wa.me/6285792599030?text=Halo,%20saya%20ingin%20pesan%20Jaje%20Sengait%20Kotak"
            },
            {
                id: 2,
                name: "Keripik Sela Gula Aren",
                description: "Keripik ubi dengan lapisan gula aren dan rasa manis yang pas",
                price: 6000,
                image: "https://z-cdn-media.chatglm.cn/files/8557f9d2-69e9-47d3-b1ee-5d89ec360191.jpg?auth_key=1872718717-75cf30c8a1094c73b20cbc7ca93ec394-0-f24f4a712749c34aeff9217cb3ded643",
                rating: 4.8,
                waLink: "https://wa.me/6285792599030?text=Halo,%20saya%20ingin%20pesan%20Keripik%20Sela%20Gula%20Aren"
            },
            {
                id: 3,
                name: "Jaje Sengait Ikat",
                description: "Jajanan tradisional khas Bali yang diikat, cocok untuk oleh-oleh",
                price: 6000,
                image: "https://z-cdn-media.chatglm.cn/files/3fb8ca44-390e-4440-8e91-3791ebf7f648.jpg?auth_key=1872718717-53834d8e58234d8ebe2f2ded633e9e08-0-6988b5e6a5b6d00753d72b8a38b8b5d6",
                rating: 4.9,
                waLink: "https://wa.me/6285792599030?text=Halo,%20saya%20ingin%20pesan%20Jaje%20Sengait%20Ikat"
            }
        ];
        
        // PERUBAHAN: Data Testimoni sesuai permintaan
        const testimonialData = [
            { 
                id: 1, 
                name: "Ni Luh Putu Ayu", 
                location: "Kintamani", 
                // Menggunakan foto ripiu 1 (foto pertama untuk review)
                image: "https://z-cdn-media.chatglm.cn/files/c4b05876-811d-4698-b540-3fceae1a8234.jpg?auth_key=1872719545-1ef2485d9ee4453f8357b246bd93efba-0-307afb9cd96d51cebaad9a8a2833f3a9", 
                text: "kue kerinya kriuk banget, manisnya pas dan harga terjangkau" 
            },
            { 
                id: 2, 
                name: "I Nyoman Sujanayasa", 
                location: "Denpasar", 
                // Menggunakan foto ripiu 2 (foto kedua untuk review)
                image: "https://z-cdn-media.chatglm.cn/files/3b02db12-1501-44a6-a2df-ce9658af88da.jpg?auth_key=1872719545-f9234ad913be4b0c8ae1a8ba259f31ba-0-2dbbe3abe644ea0c94cfe1bd7b320087", 
                text: "Ternyata kue tradisional lezat banget ya, langsung beli banyak buat stok galungan dan kuningan" 
            }
        ];
        
        function renderMenu() {
            const menuGrid = document.getElementById('menuGrid');
            menuGrid.innerHTML = menuData.map((item, index) => `
                <div class="menu-card bg-white rounded-2xl overflow-hidden shadow-lg reveal" style="transition-delay: ${index * 0.1}s">
                    <div class="relative overflow-hidden aspect-[4/3]">
                        <img src="${item.image}" alt="${item.name}" class="menu-image w-full h-full object-cover">
                    </div>
                    <div class="p-5">
                        <h4 class="font-display text-lg font-bold text-brown mb-2">${item.name}</h4>
                        <p class="text-sm text-brownLight mb-4 line-clamp-2">${item.description}</p>
                        <p class="font-display text-xl font-bold text-terracotta mb-4">Rp ${item.price.toLocaleString('id-ID')}</p>
                        <a href="${item.waLink}" target="_blank" class="flex items-center justify-center gap-2 bg-green-500 text-white py-2.5 rounded-xl font-medium hover:bg-green-600 transition-colors w-full">
                            <svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
                            Pesan via WhatsApp
                        </a>
                    </div>
                </div>
            `).join('');
            initScrollReveal();
        }
        
        function renderTestimonials() {
            const grid = document.getElementById('testimonialGrid');
            // PERUBAHAN: Layout testimoni diubah, foto produk di atas, teks di bawah
            grid.innerHTML = testimonialData.map((item, index) => `
                <div class="bg-white rounded-2xl shadow-lg overflow-hidden reveal" style="transition-delay: ${index * 0.1}s">
                    <div class="aspect-[4/3] overflow-hidden">
                        <img src="${item.image}" alt="Review Produk" class="w-full h-full object-cover hover:scale-105 transition-transform duration-500">
                    </div>
                    <div class="p-6">
                        <div class="mb-3">
                            <h4 class="font-semibold text-brown text-lg">${item.name}</h4>
                            <p class="text-sm text-brownLight">${item.location}</p>
                        </div>
                        <p class="text-brownLight leading-relaxed">"${item.text}"</p>
                    </div>
                </div>
            `).join('');
            initScrollReveal();
        }
        
        const menuToggle = document.getElementById('menuToggle');
        const closeMenu = document.getElementById('closeMenu');
        const mobileMenu = document.getElementById('mobileMenu');
        
        menuToggle.addEventListener('click', () => { mobileMenu.classList.add('active'); });
        closeMenu.addEventListener('click', () => { mobileMenu.classList.remove('active'); });
        mobileMenu.querySelectorAll('a').forEach(link => { link.addEventListener('click', () => { mobileMenu.classList.remove('active'); }); });
        
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.pageYOffset > 50) { header.classList.add('shadow-md'); } 
            else { header.classList.remove('shadow-md'); }
        });
        
        function initScrollReveal() {
            const reveals = document.querySelectorAll('.reveal');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => { if (entry.isIntersecting) { entry.target.classList.add('active'); } });
            }, { threshold: 0.1 });
            reveals.forEach(el => observer.observe(el));
        }
        
        document.addEventListener('DOMContentLoaded', () => {
            renderMenu();
            renderTestimonials();
            initScrollReveal();
        });
    </script>
</body>
</html>
# HARTA-JAYA-Kue-Kering-Tradisional
Rasa Nusantara
