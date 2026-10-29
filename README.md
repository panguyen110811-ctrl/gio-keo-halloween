[Uploading gi_k_o_b_ng_halloween.html…]()

<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🎃 Giỏ Kẹo Bí Ngô Halloween - Trạm Lời Nhắn</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600;700&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            spooky: {
              bg: '#0F061F',
              card: '#1B0E38',
              cardLight: '#2A1754',
              orange: '#FF7A00',
              orangeGlow: '#FFA043',
              purple: '#A642F4',
              neonGreen: '#39FF14',
              gold: '#FFD166',
              blood: '#FF3366'
            }
          },
          fontFamily: {
            title: ['Fredoka', 'sans-serif'],
            body: ['Nunito', 'sans-serif']
          }
        }
      }
    }
  </script>

  <style>
    body {
      font-family: 'Nunito', sans-serif;
      background-color: #0F061F;
      background-image: 
        radial-gradient(circle at 80% 15%, rgba(166, 66, 244, 0.18) 0%, transparent 40%),
        radial-gradient(circle at 20% 45%, rgba(255, 122, 0, 0.15) 0%, transparent 45%),
        radial-gradient(circle at 50% 85%, rgba(57, 255, 20, 0.08) 0%, transparent 50%);
      min-height: 100vh;
      overflow-x: hidden;
      user-select: none;
    }

    /* Đèn lồng & trăng phát sáng */
    .moon-glow {
      box-shadow: 0 0 60px 15px rgba(255, 230, 140, 0.45);
    }

    .jack-glow {
      filter: drop-shadow(0 0 25px rgba(255, 122, 0, 0.75));
    }

    .mouth-glow {
      filter: drop-shadow(0 0 16px rgba(255, 230, 0, 0.9));
    }

    /* Hiệu ứng rung giỏ bí ngô khi đón kẹo */
    @keyframes pumpkinBounce {
      0% { transform: scale(1) translateY(0); }
      20% { transform: scale(1.18, 0.82) translateY(12px); }
      45% { transform: scale(0.9, 1.15) translateY(-16px); }
      70% { transform: scale(1.05, 0.95) translateY(4px); }
      100% { transform: scale(1) translateY(0); }
    }

    .bounce-active {
      animation: pumpkinBounce 0.65s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    /* Hiệu ứng lơ lửng giỏ bí ngô */
    @keyframes gentleFloat {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-7px) rotate(1deg); }
    }

    .basket-float {
      animation: gentleFloat 4s ease-in-out infinite;
    }

    /* Đom đóm/sao lấp lánh */
    @keyframes twinkle {
      0%, 100% { opacity: 0.2; transform: scale(0.8); }
      50% { opacity: 1; transform: scale(1.2); }
    }

    .star-twinkle {
      animation: twinkle 3s ease-in-out infinite;
    }

    /* Dơi bay */
    @keyframes batFly {
      0% { transform: translate(0, 0) scaleX(1); }
      25% { transform: translate(15px, -12px) scaleX(1); }
      50% { transform: translate(30px, 0px) scaleX(1); }
      75% { transform: translate(15px, 8px) scaleX(1); }
      100% { transform: translate(0, 0) scaleX(1); }
    }

    .bat-animated {
      animation: batFly 6s ease-in-out infinite;
    }

    /* Kẹo bay vào giỏ */
    .flying-candy-clone {
      position: fixed;
      pointer-events: none;
      z-index: 9999;
      transition: all 0.85s cubic-bezier(0.25, 1, 0.5, 1);
      filter: drop-shadow(0 10px 15px rgba(255, 122, 0, 0.6));
    }

    /* Custom scrollbar */
    ::-webkit-scrollbar {
      width: 7px;
    }
    ::-webkit-scrollbar-track {
      background: #1B0E38;
    }
    ::-webkit-scrollbar-thumb {
      background: #FF7A00;
      border-radius: 999px;
    }
  </style>
</head>
<body class="text-white relative flex flex-col justify-between p-3 sm:p-6">

  <!-- ==================== HIỆU ỨNG NỀN HALLOWEEN ==================== -->
  <div class="fixed inset-0 pointer-events-none overflow-hidden z-0">
    <!-- Mặt trăng rằm ma mị -->
    <div class="absolute -top-10 -right-10 w-44 h-44 sm:w-60 sm:h-60 rounded-full bg-gradient-to-br from-yellow-100 via-amber-200 to-amber-400 opacity-90 moon-glow">
      <div class="absolute w-8 h-8 rounded-full bg-amber-300 opacity-30 top-12 left-10"></div>
      <div class="absolute w-12 h-12 rounded-full bg-amber-300 opacity-25 top-20 left-24"></div>
      <div class="absolute w-6 h-6 rounded-full bg-amber-300 opacity-30 bottom-12 left-16"></div>
    </div>

    <!-- Đàn dơi bóng đêm -->
    <svg class="absolute top-16 right-56 w-10 h-10 text-slate-900 opacity-80 bat-animated" viewBox="0 0 24 24" fill="currentColor">
      <path d="M12 9c-1.5-2-4-3-7-3-2 0-3.5.5-4.5 1 1 2 2.5 3 4.5 3 1.5 0 2.5-.5 3.5-1.5.3 1.8 1.5 3.5 3.5 3.5s3.2-1.7 3.5-3.5c1 1 2 1.5 3.5 1.5 2 0 3.5-1 4.5-3-1-.5-2.5-1-4.5-1-3 0-5.5 1-7 3z"/>
    </svg>
    <svg class="absolute top-28 right-36 w-6 h-6 text-slate-900 opacity-60 bat-animated" style="animation-delay: -2.5s;" viewBox="0 0 24 24" fill="currentColor">
      <path d="M12 9c-1.5-2-4-3-7-3-2 0-3.5.5-4.5 1 1 2 2.5 3 4.5 3 1.5 0 2.5-.5 3.5-1.5.3 1.8 1.5 3.5 3.5 3.5s3.2-1.7 3.5-3.5c1 1 2 1.5 3.5 1.5 2 0 3.5-1 4.5-3-1-.5-2.5-1-4.5-1-3 0-5.5 1-7 3z"/>
    </svg>

    <!-- Sao lập lòe -->
    <div class="absolute top-1/4 left-12 w-2 h-2 bg-yellow-200 rounded-full star-twinkle" style="animation-delay: 0.2s;"></div>
    <div class="absolute top-1/3 left-1/3 w-3 h-3 bg-amber-300 rounded-full star-twinkle" style="animation-delay: 1.5s;"></div>
    <div class="absolute top-16 left-1/2 w-2 h-2 bg-purple-300 rounded-full star-twinkle" style="animation-delay: 0.8s;"></div>
    <div class="absolute top-2/3 right-16 w-2.5 h-2.5 bg-yellow-100 rounded-full star-twinkle" style="animation-delay: 2.1s;"></div>
    <div class="absolute bottom-24 left-20 w-3 h-3 bg-orange-400 rounded-full star-twinkle" style="animation-delay: 1.1s;"></div>
  </div>

  <!-- ==================== HEADER & THANH CÔNG CỤ ==================== -->
  <header class="relative z-10 max-w-4xl mx-auto w-full flex items-center justify-between py-2 mb-2">
    <div class="flex items-center space-x-2">
      <span class="text-2xl sm:text-3xl animate-bounce">🎃</span>
      <div>
        <h1 class="font-title text-xl sm:text-2xl font-bold tracking-wide text-transparent bg-clip-text bg-gradient-to-r from-spooky-orange via-spooky-gold to-spooky-purple">
          GIỎ KẸO BÍ NGÔ
        </h1>
        <p class="text-xs text-purple-300/80 hidden sm:block">Trao kẹo ngọt - Gửi lời chúc Halloween bí ẩn</p>
      </div>
    </div>

    <!-- Nút cài đặt & Bật tắt âm thanh -->
    <div class="flex items-center space-x-2">
      <button id="toggleAudioBtn" onclick="toggleAudio()" class="px-3 py-1.5 rounded-full bg-spooky-card border border-purple-500/30 hover:border-spooky-orange text-xs text-purple-200 flex items-center gap-1.5 transition shadow">
        <span id="audioIcon">🔊</span>
        <span class="hidden sm:inline">Âm thanh</span>
      </button>

      <button onclick="openSettingsModal()" class="px-3 py-1.5 rounded-full bg-spooky-card border border-purple-500/30 hover:border-spooky-orange text-xs text-purple-200 flex items-center gap-1.5 transition shadow" title="Cài đặt kết nối Google Sheets">
        <span>⚙️</span>
        <span class="hidden sm:inline">Google Sheets</span>
      </button>
    </div>
  </header>

  <!-- ==================== KHU VỰC TRUNG TÂM: GIỎ BÍ NGÔ ==================== -->
  <main class="relative z-10 max-w-4xl mx-auto w-full flex-1 flex flex-col items-center justify-center my-1 sm:my-3">

    <!-- Huy hiệu đếm số lượng kẹo -->
    <div class="mb-2 sm:mb-4 inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-spooky-card/90 border border-spooky-orange/50 shadow-lg shadow-orange-950/40 backdrop-blur">
      <span class="text-lg">🍬</span>
      <span class="text-xs sm:text-sm font-semibold text-purple-100">
        Giỏ đang chứa: 
        <span id="candyCountBadge" class="text-spooky-gold text-base sm:text-lg font-bold font-title">0</span> viên kẹo
      </span>
      <span class="w-2 h-2 rounded-full bg-spooky-neonGreen animate-pulse"></span>
    </div>

    <!-- SVG GIỎ BÍ NGÔ KHỔNG LỒ (VỚI TÍNH NĂNG ĐÓN KẸO) -->
    <div id="basketContainer" class="relative basket-float cursor-pointer group" onclick="reactToBasketClick()" title="Bấm vào bụng giỏ bí ngô nè!">
      <!-- Điểm đích để viên kẹo bay trúng vào miệng -->
      <div id="targetMouth" class="absolute top-[48%] left-[50%] -translate-x-1/2 -translate-y-1/2 w-14 h-14 pointer-events-none z-20"></div>

      <!-- Vầng sáng bao quanh giỏ -->
      <div class="absolute -inset-4 bg-gradient-to-t from-orange-600/30 to-purple-600/20 rounded-full blur-2xl group-hover:from-orange-500/50 transition-all duration-500"></div>

      <!-- Hình vẽ vector Giỏ Bí Ngô Jack-O'-Lantern -->
      <svg id="pumpkinBasketSvg" class="w-64 h-64 sm:w-80 sm:h-80 jack-glow transition-transform duration-300" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
        <!-- Quai xách giỏ bằng dây leo cong ma mị -->
        <path d="M45 80 C 45 10, 155 10, 155 80" stroke="#4A2E18" stroke-width="8" stroke-linecap="round" fill="none"/>
        <path d="M47 80 C 47 15, 153 15, 153 80" stroke="#8D5B2E" stroke-width="4" stroke-linecap="round" fill="none"/>
        
        <!-- Cuống bí ngô màu xanh rêu -->
        <path d="M96 48 C96 35, 108 26, 116 23 C113 32, 106 43, 104 48 Z" fill="#2E6F40" stroke="#1B4D29" stroke-width="1.5"/>

        <!-- Thân bí ngô tròn múi -->
        <!-- Múi viền ngoài -->
        <ellipse cx="60" cy="118" rx="36" ry="54" fill="#E65100"/>
        <ellipse cx="140" cy="118" rx="36" ry="54" fill="#E65100"/>
        <!-- Múi trung gian -->
        <ellipse cx="76" cy="120" rx="36" ry="58" fill="#F57C00"/>
        <ellipse cx="124" cy="120" rx="36" ry="58" fill="#F57C00"/>
        <!-- Múi chính diện -->
        <ellipse cx="100" cy="122" rx="34" ry="60" fill="#FFA000"/>

        <!-- Chi tiết vân bóng nổi 3D -->
        <path d="M90 66 C75 80, 72 160, 92 180" stroke="#FFB74D" stroke-width="3" stroke-linecap="round" opacity="0.6"/>
        <path d="M120 70 C132 85, 134 155, 116 178" stroke="#E65100" stroke-width="3" stroke-linecap="round" opacity="0.5"/>

        <!-- Mắt trái khoét rực lửa -->
        <polygon points="68,98 84,106 66,114" fill="#2D0600" />
        <polygon points="68,98 84,106 66,114" fill="#FFF176" class="mouth-glow" opacity="0.95"/>

        <!-- Mắt phải khoét rực lửa -->
        <polygon points="132,98 116,106 134,114" fill="#2D0600" />
        <polygon points="132,98 116,106 134,114" fill="#FFF176" class="mouth-glow" opacity="0.95"/>

        <!-- Mũi tam giác nhỏ -->
        <polygon points="100,108 94,118 106,118" fill="#FFF176" class="mouth-glow"/>

        <!-- Miệng cười rộng răng cưa ngộ nghĩnh (Nơi đón kẹo rớt vào) -->
        <path d="M56 128 C64 158, 136 158, 144 128 C136 138, 126 130, 118 138 C110 130, 90 130, 82 138 C74 130, 64 138, 56 128 Z" fill="#2D0600"/>
        <path d="M59 130 C66 155, 134 155, 141 130 C134 139, 125 132, 117 139 C109 132, 91 132, 83 139 C75 132, 66 139, 59 130 Z" fill="#FFEA00" class="mouth-glow"/>

        <!-- Răng ma cà rồng nhỏ nhô ra ngộ nghĩnh -->
        <polygon points="78,131 84,131 81,139" fill="#FFA000"/>
        <polygon points="116,131 122,131 119,139" fill="#FFA000"/>
      </svg>

      <!-- Hạt phát sáng nảy ra từ giỏ -->
      <div id="sparkleZone" class="absolute inset-0 pointer-events-none"></div>
    </div>

    <!-- 2 NÚT TƯƠNG TÁC GIẢI QUYẾT SỰ NHÀM CHÁN -->
    <div class="mt-4 sm:mt-5 flex flex-wrap items-center justify-center gap-3 w-full px-2">
      <!-- Bốc ngẫu nhiên (Trick or Treat) -->
      <button onclick="pickRandomCandy()" class="flex-1 max-w-xs py-3 px-4 rounded-2xl bg-gradient-to-r from-amber-500 via-orange-500 to-spooky-orange text-white font-title font-bold text-sm sm:text-base tracking-wide shadow-lg shadow-orange-600/30 hover:shadow-orange-500/60 hover:-translate-y-0.5 active:translate-y-0 transition-all flex items-center justify-center gap-2 border border-yellow-300/40">
        <span class="text-xl">🎲</span>
        <span>Bốc Kẹo (Trick or Treat!)</span>
      </button>

      <!-- Khám phá toàn bộ giỏ -->
      <button onclick="openBasketExplorer()" class="flex-1 max-w-xs py-3 px-4 rounded-2xl bg-spooky-cardLight/90 hover:bg-spooky-card border border-purple-400/40 text-purple-100 font-title font-semibold text-sm sm:text-base tracking-wide shadow-lg shadow-purple-950/50 hover:-translate-y-0.5 active:translate-y-0 transition-all flex items-center justify-center gap-2">
        <span class="text-xl">📜</span>
        <span>Khám Phá Toàn Bộ Giỏ</span>
      </button>
    </div>
  </main>

  <!-- ==================== KHAY 5 LOẠI KẸO HALLOWEEN ĐỂ CHỌN ==================== -->
  <footer class="relative z-10 max-w-3xl mx-auto w-full pt-2 pb-1">
    <div class="bg-spooky-card/85 backdrop-blur-md p-3 sm:p-4 rounded-3xl border border-purple-500/25 shadow-2xl">
      <div class="text-center mb-2.5">
        <span class="text-xs uppercase tracking-widest text-spooky-gold font-bold">✨ Hãy chọn 1 viên kẹo ngọt ngào dưới đây 👇</span>
      </div>

      <!-- Lưới 5 loại kẹo sinh động -->
      <div class="grid grid-cols-5 gap-2 sm:gap-3">

        <!-- Kẹo 1: Kẹo mút xoắn Halloween -->
        <button onclick="selectCandyType('lollipop', event)" id="candy-lollipop" class="candy-btn group flex flex-col items-center justify-center p-2 rounded-2xl bg-purple-950/40 hover:bg-purple-900/60 border border-purple-600/30 hover:border-spooky-orange transition-all duration-200 active:scale-95 shadow">
          <div class="w-11 h-11 sm:w-14 sm:h-14 flex items-center justify-center group-hover:scale-110 transition-transform">
            <svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
              <!-- Que kẹo -->
              <rect x="28" y="28" width="4" height="28" rx="2" fill="#E2E8F0"/>
              <!-- Vòng xoắn kẹo -->
              <circle cx="30" cy="22" r="18" fill="#FF7A00"/>
              <path d="M30 4 A18 18 0 0 1 48 22 L30 22 Z" fill="#9333EA"/>
              <path d="M30 40 A18 18 0 0 1 12 22 L30 22 Z" fill="#9333EA"/>
              <circle cx="30" cy="22" r="10" fill="#FFD166"/>
              <circle cx="30" cy="22" r="4" fill="#FF7A00"/>
            </svg>
          </div>
          <span class="text-[11px] sm:text-xs font-semibold text-purple-200 mt-1 truncate w-full text-center group-hover:text-spooky-gold">Kẹo Mút Xoắn</span>
        </button>

        <!-- Kẹo 2: Kẹo Bí Ngô Nhỏ -->
        <button onclick="selectCandyType('pumpkin', event)" id="candy-pumpkin" class="candy-btn group flex flex-col items-center justify-center p-2 rounded-2xl bg-purple-950/40 hover:bg-purple-900/60 border border-purple-600/30 hover:border-spooky-orange transition-all duration-200 active:scale-95 shadow">
          <div class="w-11 h-11 sm:w-14 sm:h-14 flex items-center justify-center group-hover:scale-110 transition-transform">
            <svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
              <!-- Cuống -->
              <rect x="28" y="10" width="4" height="8" rx="2" fill="#22C55E"/>
              <!-- Thân quả kẹo bí -->
              <ellipse cx="30" cy="30" rx="18" ry="14" fill="#EA580C"/>
              <ellipse cx="23" cy="30" rx="12" ry="13" fill="#F97316"/>
              <ellipse cx="37" cy="30" rx="12" ry="13" fill="#F97316"/>
              <ellipse cx="30" cy="30" rx="9" ry="13" fill="#FBBF24"/>
              <!-- Mắt cười cute -->
              <circle cx="26" cy="28" r="2" fill="#3E1404"/>
              <circle cx="34" cy="28" r="2" fill="#3E1404"/>
              <path d="M27 34 Q30 38 33 34" stroke="#3E1404" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
          </div>
          <span class="text-[11px] sm:text-xs font-semibold text-purple-200 mt-1 truncate w-full text-center group-hover:text-spooky-gold">Bí Ngô Nhỏ</span>
        </button>

        <!-- Kẹo 3: Mắt Quỷ Dẻo -->
        <button onclick="selectCandyType('eyeball', event)" id="candy-eyeball" class="candy-btn group flex flex-col items-center justify-center p-2 rounded-2xl bg-purple-950/40 hover:bg-purple-900/60 border border-purple-600/30 hover:border-spooky-orange transition-all duration-200 active:scale-95 shadow">
          <div class="w-11 h-11 sm:w-14 sm:h-14 flex items-center justify-center group-hover:scale-110 transition-transform">
            <svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
              <!-- Cầu mắt trắng dẻo bóng -->
              <circle cx="30" cy="28" r="18" fill="#F8FAFC"/>
              <!-- Mạch máu nhỏ -->
              <path d="M16 28 Q22 24 24 28" stroke="#EF4444" stroke-width="1.2" stroke-linecap="round" fill="none"/>
              <path d="M44 26 Q38 30 36 26" stroke="#EF4444" stroke-width="1.2" stroke-linecap="round" fill="none"/>
              <!-- Tròng mắt xanh neon rực rỡ -->
              <circle cx="30" cy="28" r="9" fill="#06B6D4"/>
              <circle cx="30" cy="28" r="5" fill="#0F172A"/>
              <!-- Đốm sáng tạo độ long lanh dẻo -->
              <circle cx="27" cy="25" r="2" fill="#FFFFFF"/>
            </svg>
          </div>
          <span class="text-[11px] sm:text-xs font-semibold text-purple-200 mt-1 truncate w-full text-center group-hover:text-spooky-gold">Mắt Quỷ Dẻo</span>
        </button>

        <!-- Kẹo 4: Socola Dơi Đêm -->
        <button onclick="selectCandyType('bat', event)" id="candy-bat" class="candy-btn group flex flex-col items-center justify-center p-2 rounded-2xl bg-purple-950/40 hover:bg-purple-900/60 border border-purple-600/30 hover:border-spooky-orange transition-all duration-200 active:scale-95 shadow">
          <div class="w-11 h-11 sm:w-14 sm:h-14 flex items-center justify-center group-hover:scale-110 transition-transform">
            <svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
              <!-- Cánh dơi socola sẫm -->
              <path d="M30 20 C22 10, 8 16, 10 32 C16 30, 24 35, 30 28 C36 35, 44 30, 50 32 C52 16, 38 10, 30 20 Z" fill="#3D180A"/>
              <!-- Bề mặt nổi socola sữa -->
              <path d="M30 22 C24 14, 14 18, 15 29 C20 28, 25 31, 30 26 C35 31, 40 28, 45 29 C46 18, 36 14, 30 22 Z" fill="#5A2814"/>
              <!-- Mắt hạt cườm đỏ -->
              <circle cx="27" cy="22" r="1.5" fill="#EF4444"/>
              <circle cx="33" cy="22" r="1.5" fill="#EF4444"/>
            </svg>
          </div>
          <span class="text-[11px] sm:text-xs font-semibold text-purple-200 mt-1 truncate w-full text-center group-hover:text-spooky-gold">Socola Dơi</span>
        </button>

        <!-- Kẹo 5: Kẹo Gói Sọc Neon -->
        <button onclick="selectCandyType('wrapped', event)" id="candy-wrapped" class="candy-btn group flex flex-col items-center justify-center p-2 rounded-2xl bg-purple-950/40 hover:bg-purple-900/60 border border-purple-600/30 hover:border-spooky-orange transition-all duration-200 active:scale-95 shadow">
          <div class="w-11 h-11 sm:w-14 sm:h-14 flex items-center justify-center group-hover:scale-110 transition-transform">
            <svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
              <!-- Đuôi xoắn 2 bên -->
              <polygon points="12,18 22,28 12,38" fill="#EC4899"/>
              <polygon points="48,18 38,28 48,38" fill="#EC4899"/>
              <!-- Thân kẹo sọc ngộ nghĩnh -->
              <rect x="20" y="17" width="20" height="22" rx="7" fill="#8B5CF6"/>
              <!-- Sọc chéo màu neon -->
              <path d="M22 22 L27 17" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
              <path d="M22 34 L37 19" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
              <path d="M33 37 L39 31" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
            </svg>
          </div>
          <span class="text-[11px] sm:text-xs font-semibold text-purple-200 mt-1 truncate w-full text-center group-hover:text-spooky-gold">Kẹo Gói Sọc</span>
        </button>

      </div>
    </div>
  </footer>

  <!-- ==================== POPUP MODAL 1: GÓI LỜI NHẮN VÀO KẸO ==================== -->
  <div id="writeModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/75 backdrop-blur-sm hidden opacity-0 transition-opacity duration-200">
    <div class="bg-gradient-to-b from-spooky-cardLight to-spooky-card w-full max-w-md rounded-3xl p-5 sm:p-6 border border-spooky-orange/40 shadow-2xl relative transform scale-95 transition-transform duration-200">
      
      <!-- Nút đóng -->
      <button onclick="closeWriteModal()" class="absolute top-4 right-4 text-purple-300 hover:text-white text-xl p-1 leading-none">✕</button>

      <!-- Phần xem trước kẹo đã chọn -->
      <div class="flex items-center gap-3 mb-4 pb-3 border-b border-purple-500/20">
        <div id="modalCandyIcon" class="w-14 h-14 p-1 rounded-2xl bg-spooky-bg/80 border border-purple-400/30 flex items-center justify-center">
          <!-- Icon render động ở đây -->
        </div>
        <div>
          <span class="text-xs uppercase tracking-wider text-spooky-gold font-bold">Gói quà vào kẹo:</span>
          <h3 id="modalCandyTitle" class="font-title text-lg font-bold text-white">Kẹo Mút Xoắn</h3>
        </div>
      </div>

      <!-- Form nhập nội dung -->
      <form id="candyForm" onsubmit="handleSendCandy(event)" class="space-y-3.5">
        <div>
          <label class="block text-xs font-bold text-purple-200 mb-1">TÊN HOẶC BIỆT DANH CỦA BẠN:</label>
          <input type="text" id="senderName" required maxlength="25" placeholder="Ví dụ: Phù thủy nhỏ, Bí mật, An Nhiên..." class="w-full px-3.5 py-2.5 rounded-xl bg-purple-950/60 border border-purple-500/40 text-white placeholder-purple-400/40 focus:outline-none focus:border-spooky-orange text-sm transition">
        </div>

        <div>
          <div class="flex justify-between items-center mb-1">
            <label class="block text-xs font-bold text-purple-200">LỜI NHẮN HALLOWEEN:</label>
            <span id="wordCounter" class="text-xs font-semibold text-spooky-gold">0 / 50 từ</span>
          </div>
          <textarea id="candyMessage" required rows="3" placeholder="Nhập lời chúc, tin nhắn bí mật hoặc câu 'Trick or Treat' ngọt ngào..." class="w-full px-3.5 py-2.5 rounded-xl bg-purple-950/60 border border-purple-500/40 text-white placeholder-purple-400/40 focus:outline-none focus:border-spooky-orange text-sm resize-none transition" oninput="validateWordCount()"></textarea>
          <p id="wordCountError" class="text-[11px] text-red-400 mt-1 hidden">⚠️ Lời nhắn đã vượt quá giới hạn 50 từ. Bạn hãy rút gọn lại một chút nhé!</p>
        </div>

        <!-- Các gợi ý lời chúc nhanh -->
        <div class="pt-1">
          <span class="text-[11px] text-purple-300 font-semibold block mb-1.5">⚡ Gợi ý lời nhắn siêu nhanh:</span>
          <div class="flex flex-wrap gap-1.5 text-xs">
            <button type="button" onclick="fillQuickMessage('Chúc bạn một mùa Halloween ngọt ngào, ấm áp và luôn vui vẻ nhé! 🍬')" class="px-2.5 py-1 rounded-lg bg-purple-900/40 border border-purple-500/30 text-purple-200 hover:text-white hover:bg-purple-800/60 transition text-[11px]">🎃 Ngọt ngào</button>
            <button type="button" onclick="fillQuickMessage('Trick or Treat! Nhớ chia kẹo cho tớ nha, đồ hảo ngọt ơi! 👻')" class="px-2.5 py-1 rounded-lg bg-purple-900/40 border border-purple-500/30 text-purple-200 hover:text-white hover:bg-purple-800/60 transition text-[11px]">👻 Trick or Treat</button>
            <button type="button" onclick="fillQuickMessage('Ai bốc trúng viên kẹo này thì ngày mai sẽ gặp điều may mắn bất ngờ! ✨')" class="px-2.5 py-1 rounded-lg bg-purple-900/40 border border-purple-500/30 text-purple-200 hover:text-white hover:bg-purple-800/60 transition text-[11px]">✨ May mắn</button>
          </div>
        </div>

        <!-- Nút gửi kẹo -->
        <div class="pt-2">
          <button type="submit" id="submitCandyBtn" class="w-full py-3 px-4 rounded-xl bg-gradient-to-r from-spooky-orange to-amber-500 hover:from-orange-600 hover:to-amber-600 text-white font-title font-bold text-base tracking-wide shadow-lg shadow-orange-600/40 hover:shadow-orange-500/60 transition flex items-center justify-center gap-2">
            <span>Thả kẹo vào giỏ ngay 🎃</span>
          </button>
        </div>
      </form>
    </div>
  </div>

  <!-- ==================== POPUP MODAL 2: BỐC KẸO NGẪU NHIÊN (TRICK OR TREAT) ==================== -->
  <div id="revealModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-sm hidden opacity-0 transition-opacity duration-200">
    <div class="bg-gradient-to-b from-spooky-cardLight via-spooky-card to-spooky-bg w-full max-w-sm rounded-3xl p-6 border-2 border-spooky-gold shadow-2xl relative text-center transform scale-95 transition-transform duration-200">
      
      <button onclick="closeRevealModal()" class="absolute top-4 right-4 text-purple-300 hover:text-white text-xl p-1 leading-none">✕</button>

      <div class="w-20 h-20 mx-auto mb-3 p-2 rounded-3xl bg-spooky-card border-2 border-spooky-gold/80 flex items-center justify-center shadow-lg shadow-amber-500/30 animate-pulse">
        <div id="revealIcon" class="w-14 h-14"></div>
      </div>

      <span class="inline-block px-3 py-1 rounded-full bg-orange-500/20 border border-orange-400/40 text-spooky-gold text-xs font-bold uppercase tracking-wider mb-2">
        🍬 Viên kẹo bạn đã rút được!
      </span>

      <h3 id="revealSender" class="font-title text-xl font-bold text-white mb-2">Từ: Bí Mật</h3>

      <div class="bg-purple-950/70 p-4 rounded-2xl border border-purple-500/30 text-purple-100 text-sm italic mb-4 leading-relaxed max-h-44 overflow-y-auto">
        "<span id="revealMessage">Lời nhắn...</span>"
      </div>

      <div class="text-[11px] text-purple-400 mb-4" id="revealTime">Gửi lúc: Vừa xong</div>

      <div class="flex gap-2">
        <button onclick="pickRandomCandy()" class="flex-1 py-2.5 px-3 rounded-xl bg-spooky-orange hover:bg-orange-600 text-white font-bold text-xs font-title shadow transition">
          🎲 Bốc viên khác
        </button>
        <button onclick="closeRevealModal()" class="flex-1 py-2.5 px-3 rounded-xl bg-purple-900/50 hover:bg-purple-800/50 border border-purple-400/40 text-purple-200 text-xs font-semibold transition">
          Đóng lại
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== POPUP MODAL 3: KHÁM PHÁ TOÀN BỘ GIỎ KẸO ==================== -->
  <div id="explorerModal" class="fixed inset-0 z-50 flex items-center justify-center p-3 sm:p-5 bg-black/80 backdrop-blur-sm hidden opacity-0 transition-opacity duration-200">
    <div class="bg-spooky-card w-full max-w-2xl max-h-[85vh] rounded-3xl p-5 sm:p-6 border border-purple-500/40 shadow-2xl flex flex-col relative">
      
      <div class="flex items-center justify-between pb-3 border-b border-purple-500/20 mb-3">
        <div>
          <h3 class="font-title text-xl font-bold text-white flex items-center gap-2">
            <span>📜</span> Giỏ Kẹo Halloween Chung
          </h3>
          <p class="text-xs text-purple-300">Nhấp vào từng viên kẹo để đọc lời nhắn bí mật</p>
        </div>
        <button onclick="closeExplorerModal()" class="text-purple-300 hover:text-white text-xl p-1 leading-none">✕</button>
      </div>

      <!-- Danh sách kẹo cuộn được -->
      <div id="candiesListContainer" class="flex-1 overflow-y-auto pr-1 space-y-2.5">
        <!-- Render động từ JavaScript -->
      </div>
    </div>
  </div>

  <!-- ==================== POPUP MODAL 4: CÀI ĐẶT GOOGLE SHEETS ==================== -->
  <div id="settingsModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-sm hidden opacity-0 transition-opacity duration-200">
    <div class="bg-spooky-card w-full max-w-lg rounded-3xl p-5 sm:p-6 border border-spooky-orange/40 shadow-2xl relative text-left">
      
      <button onclick="closeSettingsModal()" class="absolute top-4 right-4 text-purple-300 hover:text-white text-xl p-1 leading-none">✕</button>

      <h3 class="font-title text-xl font-bold text-white mb-1 flex items-center gap-2">
        <span>⚙️</span> Cài Đặt Liên Kết Google Sheets
      </h3>
      <p class="text-xs text-purple-300 mb-4 leading-relaxed">
        Dán URL <strong>Google Apps Script Web App</strong> của bạn vào đây. Mỗi khi có ai đó thả kẹo, dữ liệu sẽ tự động được ghi thẳng vào bảng tính của bạn!
      </p>

      <div class="space-y-3 mb-4">
        <div>
          <label class="block text-xs font-bold text-purple-200 mb-1">GOOGLE APPS SCRIPT WEB APP URL:</label>
          <input type="url" id="sheetsWebhookInput" placeholder="https://script.google.com/macros/s/.../exec" class="w-full px-3.5 py-2.5 rounded-xl bg-purple-950/80 border border-purple-500/40 text-white placeholder-purple-400/30 text-xs focus:outline-none focus:border-spooky-orange">
        </div>

        <!-- Hướng dẫn cách tạo code Apps Script 2 phút -->
        <details class="text-xs text-purple-200 bg-purple-950/40 p-3 rounded-xl border border-purple-500/20">
          <summary class="font-bold text-spooky-gold cursor-pointer hover:underline">
            👉 Xem code 6 dòng Google Apps Script để copy
          </summary>
          <div class="mt-2 text-[11px] text-purple-300 space-y-2">
            <p>1. Mở Google Sheet > Chọn <strong>Tiện ích mở rộng (Extensions) > Apps Script</strong>.</p>
            <p>2. Xóa hết code cũ và dán đoạn sau:</p>
            <pre class="bg-black/50 p-2 rounded text-emerald-400 overflow-x-auto text-[10px] font-mono select-all">
function doPost(e) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  var data = JSON.parse(e.postData.contents);
  sheet.appendRow([new Date(), data.sender, data.candyName, data.message]);
  return ContentService.createTextOutput("OK");
}</pre>
            <p>3. Bấm <strong>Triển khai (Deploy) > Tùy chọn triển khai mới (New deployment)</strong> > Chọn loại <strong>Web app</strong> > Ai có quyền truy cập: Chọn <strong>Bất kỳ ai (Anyone)</strong> > Copy link kết thúc bằng <code>/exec</code> dán vào ô trên.</p>
          </div>
        </details>
      </div>

      <div class="flex gap-2">
        <button onclick="saveSettings()" class="flex-1 py-2.5 rounded-xl bg-spooky-orange hover:bg-orange-600 font-bold text-xs font-title text-white transition">
          Lưu Cài Đặt
        </button>
        <button onclick="clearAllDataPrompt()" class="py-2.5 px-3 rounded-xl bg-red-950/60 hover:bg-red-900 border border-red-500/40 text-red-300 text-xs transition">
          Xóa Toàn Bộ Kẹo
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== HỘP THÔNG BÁO TOAST ==================== -->
  <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 z-50 px-4 py-2.5 rounded-full bg-spooky-cardLight border border-spooky-gold text-white text-xs font-bold shadow-2xl transition-all duration-300 opacity-0 pointer-events-none translate-y-4">
    Thông báo ở đây
  </div>

  <!-- ==================== JAVASCRIPT TOÀN BỘ LOGIC ==================== -->
  <script>
    // Dữ liệu định nghĩa 5 loại kẹo
    const CANDY_TYPES = {
      lollipop: {
        id: 'lollipop',
        name: 'Kẹo Mút Xoắn',
        color: '#FF7A00',
        svg: `<svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
          <rect x="28" y="28" width="4" height="28" rx="2" fill="#E2E8F0"/>
          <circle cx="30" cy="22" r="18" fill="#FF7A00"/>
          <path d="M30 4 A18 18 0 0 1 48 22 L30 22 Z" fill="#9333EA"/>
          <path d="M30 40 A18 18 0 0 1 12 22 L30 22 Z" fill="#9333EA"/>
          <circle cx="30" cy="22" r="10" fill="#FFD166"/>
          <circle cx="30" cy="22" r="4" fill="#FF7A00"/>
        </svg>`
      },
      pumpkin: {
        id: 'pumpkin',
        name: 'Kẹo Bí Ngô Nhỏ',
        color: '#F97316',
        svg: `<svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
          <rect x="28" y="10" width="4" height="8" rx="2" fill="#22C55E"/>
          <ellipse cx="30" cy="30" rx="18" ry="14" fill="#EA580C"/>
          <ellipse cx="23" cy="30" rx="12" ry="13" fill="#F97316"/>
          <ellipse cx="37" cy="30" rx="12" ry="13" fill="#F97316"/>
          <ellipse cx="30" cy="30" rx="9" ry="13" fill="#FBBF24"/>
          <circle cx="26" cy="28" r="2" fill="#3E1404"/>
          <circle cx="34" cy="28" r="2" fill="#3E1404"/>
          <path d="M27 34 Q30 38 33 34" stroke="#3E1404" stroke-width="1.5" stroke-linecap="round"/>
        </svg>`
      },
      eyeball: {
        id: 'eyeball',
        name: 'Kẹo Mắt Quỷ Dẻo',
        color: '#06B6D4',
        svg: `<svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
          <circle cx="30" cy="28" r="18" fill="#F8FAFC"/>
          <path d="M16 28 Q22 24 24 28" stroke="#EF4444" stroke-width="1.2" stroke-linecap="round" fill="none"/>
          <path d="M44 26 Q38 30 36 26" stroke="#EF4444" stroke-width="1.2" stroke-linecap="round" fill="none"/>
          <circle cx="30" cy="28" r="9" fill="#06B6D4"/>
          <circle cx="30" cy="28" r="5" fill="#0F172A"/>
          <circle cx="27" cy="25" r="2" fill="#FFFFFF"/>
        </svg>`
      },
      bat: {
        id: 'bat',
        name: 'Kẹo Socola Dơi',
        color: '#5A2814',
        svg: `<svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
          <path d="M30 20 C22 10, 8 16, 10 32 C16 30, 24 35, 30 28 C36 35, 44 30, 50 32 C52 16, 38 10, 30 20 Z" fill="#3D180A"/>
          <path d="M30 22 C24 14, 14 18, 15 29 C20 28, 25 31, 30 26 C35 31, 40 28, 45 29 C46 18, 36 14, 30 22 Z" fill="#5A2814"/>
          <circle cx="27" cy="22" r="1.5" fill="#EF4444"/>
          <circle cx="33" cy="22" r="1.5" fill="#EF4444"/>
        </svg>`
      },
      wrapped: {
        id: 'wrapped',
        name: 'Kẹo Gói Sọc Neon',
        color: '#EC4899',
        svg: `<svg class="w-full h-full" viewBox="0 0 60 60" fill="none">
          <polygon points="12,18 22,28 12,38" fill="#EC4899"/>
          <polygon points="48,18 38,28 48,38" fill="#EC4899"/>
          <rect x="20" y="17" width="20" height="22" rx="7" fill="#8B5CF6"/>
          <path d="M22 22 L27 17" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
          <path d="M22 34 L37 19" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
          <path d="M33 37 L39 31" stroke="#38BDF8" stroke-width="3" stroke-linecap="round"/>
        </svg>`
      }
    };

    // Dữ liệu mẫu ban đầu để giỏ không bị trống
    const INITIAL_CANDIES = [
      {
        id: 1,
        type: 'lollipop',
        candyName: 'Kẹo Mút Xoắn',
        sender: 'Bí Ngô Vui Tính',
        message: 'Chúc bạn một mùa lễ hội ma quái thật nhiều niềm vui và luôn nở nụ cười rạng rỡ nha! 🎃✨',
        time: 'Hôm nay'
      },
      {
        id: 2,
        type: 'bat',
        candyName: 'Socola Dơi',
        sender: 'Ma Cà Rồng Dễ Thương',
        message: 'Trick or Treat! Mình không cắn đâu, chỉ để lại một viên kẹo socola siêu ngọt cho bạn thôi!',
        time: 'Hôm nay'
      },
      {
        id: 3,
        type: 'eyeball',
        candyName: 'Kẹo Mắt Quỷ',
        sender: 'Người Bí Ẩn',
        message: 'Ai bốc trúng viên kẹo này thì ngày mai sẽ nhận được một tin nhắn tỏ tình hoặc quà bất ngờ đấy!',
        time: 'Hôm nay'
      }
    ];

    // Trạng thái ứng dụng
    let candies = [];
    let selectedCandyKey = 'lollipop';
    let lastClickedButtonRect = null;
    let audioEnabled = true;
    let audioCtx = null;
    let googleSheetWebhookUrl = '';

    // ==================== KHỞI TẠO HỆ THỐNG ÂM THANH (WEB AUDIO API) ====================
    function initAudio() {
      if (!audioCtx) {
        const AudioContext = window.AudioContext || window.webkitAudioContext;
        if (AudioContext) {
          audioCtx = new AudioContext();
        }
      }
      if (audioCtx && audioCtx.state === 'suspended') {
        audioCtx.resume();
      }
    }

    // Âm thanh 'Pop' vui nhộn khi kẹo rơi
    function playPopSound() {
      if (!audioEnabled) return;
      initAudio();
      if (!audioCtx) return;

      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();

      osc.type = 'sine';
      osc.frequency.setValueAtTime(320, audioCtx.currentTime);
      osc.frequency.exponentialRampToValueAtTime(780, audioCtx.currentTime + 0.12);

      gain.gain.setValueAtTime(0.25, audioCtx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.12);

      osc.connect(gain);
      gain.connect(audioCtx.destination);

      osc.start();
      osc.stop(audioCtx.currentTime + 0.13);
    }

    // Âm thanh chuông ma thuật khi kẹo rơi tọt vào giỏ
    function playMagicChime() {
      if (!audioEnabled) return;
      initAudio();
      if (!audioCtx) return;

      const freqs = [523.25, 659.25, 783.99, 1046.50]; // C5, E5, G5, C6
      freqs.forEach((freq, idx) => {
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();

        osc.type = 'triangle';
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime + (idx * 0.06));

        gain.gain.setValueAtTime(0.2, audioCtx.currentTime + (idx * 0.06));
        gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + (idx * 0.06) + 0.45);

        osc.connect(gain);
        gain.connect(audioCtx.destination);

        osc.start(audioCtx.currentTime + (idx * 0.06));
        osc.stop(audioCtx.currentTime + (idx * 0.06) + 0.5);
      });
    }

    // Âm thanh kỳ bí khi bốc ngẫu nhiên (Trick or Treat)
    function playMysterySound() {
      if (!audioEnabled) return;
      initAudio();
      if (!audioCtx) return;

      const osc = audioCtx.createOscillator();
      const gain = audioCtx.createGain();

      osc.type = 'sawtooth';
      osc.frequency.setValueAtTime(440, audioCtx.currentTime);
      osc.frequency.exponentialRampToValueAtTime(880, audioCtx.currentTime + 0.3);

      gain.gain.setValueAtTime(0.15, audioCtx.currentTime);
      gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.35);

      osc.connect(gain);
      gain.connect(audioCtx.destination);

      osc.start();
      osc.stop(audioCtx.currentTime + 0.36);
    }

    function toggleAudio() {
      audioEnabled = !audioEnabled;
      document.getElementById('audioIcon').textContent = audioEnabled ? '🔊' : '🔇';
      showToast(audioEnabled ? 'Đã bật âm thanh' : 'Đã tắt âm thanh');
    }

    // ==================== KHỞI CHẠY KHI TẢI TRANG ====================
    window.addEventListener('DOMContentLoaded', () => {
      // Đọc từ LocalStorage
      const savedCandies = localStorage.getItem('halloween_candies');
      if (savedCandies) {
        try {
          candies = JSON.parse(savedCandies);
        } catch(e) {
          candies = INITIAL_CANDIES;
        }
      } else {
        candies = [...INITIAL_CANDIES];
        saveCandiesToStorage();
      }

      googleSheetWebhookUrl = localStorage.getItem('halloween_sheet_webhook') || '';
      document.getElementById('sheetsWebhookInput').value = googleSheetWebhookUrl;

      updateCountBadge();
    });

    function saveCandiesToStorage() {
      localStorage.setItem('halloween_candies', JSON.stringify(candies));
      updateCountBadge();
    }

    function updateCountBadge() {
      document.getElementById('candyCountBadge').textContent = candies.length;
    }

    // ==================== BƯỚC 1: BẤM CHỌN KẸO ====================
    function selectCandyType(typeKey, event) {
      initAudio();
      playPopSound();
      selectedCandyKey = typeKey;

      if (event && event.currentTarget) {
        lastClickedButtonRect = event.currentTarget.getBoundingClientRect();
      }

      const candy = CANDY_TYPES[typeKey];
      document.getElementById('modalCandyIcon').innerHTML = candy.svg;
      document.getElementById('modalCandyTitle').textContent = candy.name;

      // Mở modal nhập lời nhắn
      const modal = document.getElementById('writeModal');
      modal.classList.remove('hidden');
      setTimeout(() => {
        modal.classList.remove('opacity-0');
        modal.firstElementChild.classList.remove('scale-95');
      }, 10);
      document.getElementById('senderName').focus();
    }

    function closeWriteModal() {
      const modal = document.getElementById('writeModal');
      modal.classList.add('opacity-0');
      modal.firstElementChild.classList.add('scale-95');
      setTimeout(() => {
        modal.classList.add('hidden');
      }, 200);
    }

    // Đếm số từ và kiểm soát tối đa 50 từ
    function getWordCount(text) {
      const trimmed = text.trim();
      if (!trimmed) return 0;
      return trimmed.split(/\s+/).filter(Boolean).length;
    }

    function validateWordCount() {
      const textarea = document.getElementById('candyMessage');
      const counter = document.getElementById('wordCounter');
      const errorMsg = document.getElementById('wordCountError');
      const submitBtn = document.getElementById('submitCandyBtn');
      const count = getWordCount(textarea.value);

      counter.textContent = `${count} / 50 từ`;

      if (count > 50) {
        counter.classList.remove('text-spooky-gold');
        counter.classList.add('text-red-400', 'font-bold');
        errorMsg.classList.remove('hidden');
        submitBtn.disabled = true;
        submitBtn.classList.add('opacity-50', 'cursor-not-allowed');
      } else {
        counter.classList.add('text-spooky-gold');
        counter.classList.remove('text-red-400', 'font-bold');
        errorMsg.classList.add('hidden');
        submitBtn.disabled = false;
        submitBtn.classList.remove('opacity-50', 'cursor-not-allowed');
      }
    }

    function fillQuickMessage(msg) {
      const textarea = document.getElementById('candyMessage');
      textarea.value = msg;
      validateWordCount();
    }

    // ==================== BƯỚC 2: THẢ KẸO VÀO GIỎ BẰNG HOẠT HỌA ====================
    function handleSendCandy(e) {
      e.preventDefault();
      const sender = document.getElementById('senderName').value.trim();
      const message = document.getElementById('candyMessage').value.trim();

      if (!sender || !message) return;
      if (getWordCount(message) > 50) return;

      const newCandy = {
        id: Date.now(),
        type: selectedCandyKey,
        candyName: CANDY_TYPES[selectedCandyKey].name,
        sender: sender,
        message: message,
        time: 'Vừa xong'
      };

      // Đóng modal
      closeWriteModal();

      // Reset form
      document.getElementById('candyForm').reset();
      document.getElementById('wordCounter').textContent = '0 / 50 từ';

      // Kích hoạt hiệu ứng bay kẹo
      triggerFlyingCandyAnimation(selectedCandyKey, () => {
        // Lưu dữ liệu vào giỏ
        candies.push(newCandy);
        saveCandiesToStorage();

        // Gửi ngầm tới Google Sheets nếu có link cài đặt
        syncToGoogleSheets(newCandy);

        showToast('✨ Viên kẹo đã rơi tọt vào giỏ bí ngô!');
      });
    }

    // Hiệu ứng hoạt họa kẹo bay từ khay/modal thẳng vào miệng giỏ bí ngô
    function triggerFlyingCandyAnimation(candyKey, onComplete) {
      const mouthTarget = document.getElementById('targetMouth');
      const targetRect = mouthTarget.getBoundingClientRect();

      // Tọa độ bắt đầu
      let startX = window.innerWidth / 2;
      let startY = window.innerHeight * 0.75;

      if (lastClickedButtonRect) {
        startX = lastClickedButtonRect.left + (lastClickedButtonRect.width / 2);
        startY = lastClickedButtonRect.top + (lastClickedButtonRect.height / 2);
      }

      // Tọa độ kết thúc (tâm miệng giỏ bí ngô)
      const endX = targetRect.left + (targetRect.width / 2);
      const endY = targetRect.top + (targetRect.height / 2);

      // Tạo phần tử bay tạm thời
      const flyingEl = document.createElement('div');
      flyingEl.className = 'flying-candy-clone w-16 h-16 sm:w-20 sm:h-20';
      flyingEl.innerHTML = CANDY_TYPES[candyKey].svg;
      flyingEl.style.left = `${startX - 35}px`;
      flyingEl.style.top = `${startY - 35}px`;
      flyingEl.style.transform = 'scale(1) rotate(0deg)';
      document.body.appendChild(flyingEl);

      playPopSound();

      // Buộc trình duyệt reflow
      void flyingEl.offsetWidth;

      // Di chuyển theo vòng cung nhẹ
      requestAnimationFrame(() => {
        flyingEl.style.left = `${endX - 25}px`;
        flyingEl.style.top = `${endY - 25}px`;
        flyingEl.style.transform = 'scale(0.3) rotate(360deg)';
        flyingEl.style.opacity = '0.9';
      });

      // Khi kẹo chạm đích
      setTimeout(() => {
        flyingEl.remove();

        // Giỏ bí ngô phản hồi rung lắc
        const basketSvg = document.getElementById('pumpkinBasketSvg');
        basketSvg.classList.remove('bounce-active');
        void basketSvg.offsetWidth;
        basketSvg.classList.add('bounce-active');

        // Âm thanh thần tiên
        playMagicChime();

        // Nảy pháo hoa sao hạt quanh miệng
        spawnSparkles(endX, endY);

        if (onComplete) onComplete();
      }, 850);
    }

    // Hiệu ứng tia sáng bung nở khi đón kẹo
    function spawnSparkles(x, y) {
      const colors = ['#FFD166', '#FF7A00', '#A642F4', '#39FF14', '#FFFFFF'];
      for (let i = 0; i < 16; i++) {
        const star = document.createElement('div');
        star.style.position = 'fixed';
        star.style.left = `${x}px`;
        star.style.top = `${y}px`;
        star.style.width = `${Math.random() * 8 + 4}px`;
        star.style.height = star.style.width;
        star.style.borderRadius = '50%';
        star.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
        star.style.pointerEvents = 'none';
        star.style.zIndex = '9999';
        star.style.boxShadow = `0 0 10px ${star.style.backgroundColor}`;
        document.body.appendChild(star);

        const angle = Math.random() * Math.PI * 2;
        const velocity = Math.random() * 65 + 25;
        const destX = Math.cos(angle) * velocity;
        const destY = Math.sin(angle) * velocity;

        star.animate([
          { transform: 'translate(0, 0) scale(1)', opacity: 1 },
          { transform: `translate(${destX}px, ${destY}px) scale(0)`, opacity: 0 }
        ], {
          duration: 650,
          easing: 'cubic-bezier(0.2, 0.9, 0.3, 1)'
        }).onfinish = () => star.remove();
      }
    }

    function reactToBasketClick() {
      initAudio();
      playPopSound();
      const basketSvg = document.getElementById('pumpkinBasketSvg');
      basketSvg.classList.remove('bounce-active');
      void basketSvg.offsetWidth;
      basketSvg.classList.add('bounce-active');
      showToast('🎃 Ú òa! Hãy chọn 1 viên kẹo bên dưới để thả vào nhé!');
    }

    // ==================== BƯỚC 3: TÍNH NĂNG BỐC KẸO NGẪU NHIÊN ====================
    function pickRandomCandy() {
      if (candies.length === 0) {
        showToast('Giỏ hiện đang trống trơn, hãy là người đầu tiên bỏ kẹo vào nhé!');
        return;
      }

      playMysterySound();

      const randomIndex = Math.floor(Math.random() * candies.length);
      const chosen = candies[randomIndex];

      const candyMeta = CANDY_TYPES[chosen.type] || CANDY_TYPES.lollipop;

      document.getElementById('revealIcon').innerHTML = candyMeta.svg;
      document.getElementById('revealSender').textContent = `Từ: ${chosen.sender}`;
      document.getElementById('revealMessage').textContent = chosen.message;
      document.getElementById('revealTime').textContent = `Loại kẹo: ${chosen.candyName || candyMeta.name} • ${chosen.time || 'Halloween'}`;

      closeExplorerModal();

      const modal = document.getElementById('revealModal');
      modal.classList.remove('hidden');
      setTimeout(() => {
        modal.classList.remove('opacity-0');
        modal.firstElementChild.classList.remove('scale-95');
      }, 10);
    }

    function closeRevealModal() {
      const modal = document.getElementById('revealModal');
      modal.classList.add('opacity-0');
      modal.firstElementChild.classList.add('scale-95');
      setTimeout(() => modal.classList.add('hidden'), 200);
    }

    // ==================== BƯỚC 4: KHÁM PHÁ TOÀN BỘ GIỎ KẸO ====================
    function openBasketExplorer() {
      initAudio();
      const container = document.getElementById('candiesListContainer');
      container.innerHTML = '';

      if (candies.length === 0) {
        container.innerHTML = `
          <div class="text-center py-10 text-purple-300">
            <span class="text-4xl block mb-2">🕷️</span>
            Chưa có viên kẹo nào trong giỏ. Hãy bấm chọn 1 viên kẹo bên dưới để gửi lời nhắn đầu tiên!
          </div>
        `;
      } else {
        // Hiển thị kẹo mới nhất lên đầu
        const reversedCandies = [...candies].reverse();

        reversedCandies.forEach((item) => {
          const meta = CANDY_TYPES[item.type] || CANDY_TYPES.lollipop;
          const card = document.createElement('div');
          card.className = 'p-3 rounded-2xl bg-purple-950/60 border border-purple-500/25 flex items-center justify-between gap-3 hover:border-spooky-orange transition';
          card.innerHTML = `
            <div class="flex items-center gap-3 min-w-0">
              <div class="w-10 h-10 p-1 rounded-xl bg-purple-900/60 flex-shrink-0 flex items-center justify-center">
                ${meta.svg}
              </div>
              <div class="min-w-0">
                <div class="flex items-center gap-2">
                  <h4 class="font-bold text-sm text-spooky-gold truncate">${escapeHtml(item.sender)}</h4>
                  <span class="text-[10px] px-2 py-0.5 rounded-full bg-purple-900 text-purple-300">${meta.name}</span>
                </div>
                <p class="text-xs text-purple-200/90 truncate mt-0.5 max-w-xs sm:max-w-md">${escapeHtml(item.message)}</p>
              </div>
            </div>
            <button onclick='readSpecificCandy(${JSON.stringify(item).replace(/'/g, "&apos;")})' class="px-2.5 py-1 rounded-xl bg-spooky-orange/30 hover:bg-spooky-orange text-orange-200 hover:text-white text-xs font-semibold flex-shrink-0 transition">
              Đọc
            </button>
          `;
          container.appendChild(card);
        });
      }

      const modal = document.getElementById('explorerModal');
      modal.classList.remove('hidden');
      setTimeout(() => {
        modal.classList.remove('opacity-0');
      }, 10);
    }

    function readSpecificCandy(item) {
      closeExplorerModal();
      const meta = CANDY_TYPES[item.type] || CANDY_TYPES.lollipop;
      document.getElementById('revealIcon').innerHTML = meta.svg;
      document.getElementById('revealSender').textContent = `Từ: ${item.sender}`;
      document.getElementById('revealMessage').textContent = item.message;
      document.getElementById('revealTime').textContent = `Loại kẹo: ${item.candyName || meta.name} • ${item.time || 'Halloween'}`;

      const modal = document.getElementById('revealModal');
      modal.classList.remove('hidden');
      setTimeout(() => {
        modal.classList.remove('opacity-0');
        modal.firstElementChild.classList.remove('scale-95');
      }, 10);
    }

    function closeExplorerModal() {
      const modal = document.getElementById('explorerModal');
      modal.classList.add('opacity-0');
      setTimeout(() => modal.classList.add('hidden'), 200);
    }

    // ==================== BƯỚC 5: TÍCH HỢP GOOGLE SHEETS ====================
    function openSettingsModal() {
      const modal = document.getElementById('settingsModal');
      modal.classList.remove('hidden');
      setTimeout(() => modal.classList.remove('opacity-0'), 10);
    }

    function closeSettingsModal() {
      const modal = document.getElementById('settingsModal');
      modal.classList.add('opacity-0');
      setTimeout(() => modal.classList.add('hidden'), 200);
    }

    function saveSettings() {
      const url = document.getElementById('sheetsWebhookInput').value.trim();
      googleSheetWebhookUrl = url;
      localStorage.setItem('halloween_sheet_webhook', url);
      closeSettingsModal();
      showToast(url ? '✅ Đã lưu liên kết Google Sheets!' : 'Đã xóa liên kết Google Sheets');
    }

    function syncToGoogleSheets(candyData) {
      if (!googleSheetWebhookUrl) return;

      try {
        fetch(googleSheetWebhookUrl, {
          method: 'POST',
          mode: 'no-cors',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({
            sender: candyData.sender,
            candyName: candyData.candyName,
            message: candyData.message,
            timestamp: new Date().toLocaleString('vi-VN')
          })
        }).catch(err => {
          console.warn('Lỗi gửi tới Google Sheets (nếu do CORS thì dữ liệu vẫn có thể đã vào):', err);
        });
      } catch (e) {
        console.error('Không thể gửi request Google Sheets:', e);
      }
    }

    function clearAllDataPrompt() {
      candies = [];
      saveCandiesToStorage();
      closeSettingsModal();
      showToast('Đã làm trống giỏ kẹo!');
    }

    // ==================== TIỆN ÍCH HỖ TRỢ ====================
    function showToast(msg) {
      const toast = document.getElementById('toast');
      toast.textContent = msg;
      toast.classList.remove('opacity-0', 'translate-y-4');
      toast.classList.add('opacity-100', 'translate-y-0');

      clearTimeout(window.toastTimer);
      window.toastTimer = setTimeout(() => {
        toast.classList.remove('opacity-100', 'translate-y-0');
        toast.classList.add('opacity-0', 'translate-y-4');
      }, 3000);
    }

    function escapeHtml(string) {
      const div = document.createElement('div');
      div.innerText = string;
      return div.innerHTML;
    }
  </script>
</body>
</html>
