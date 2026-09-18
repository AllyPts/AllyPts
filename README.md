<div align="center">

```xml
<svg xmlns="[http://www.w3.org/2000/svg](http://www.w3.org/2000/svg)" viewBox="0 0 850 340" width="100%" height="340">
  <defs>
    <!-- Filtro de Brilho Neon (Glow) -->
    <filter id="matrix-glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="box-glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <style>
      @keyframes fall {
        0% { transform: translateY(-120px); opacity: 0; }
        20% { opacity: 0.8; }
        80% { opacity: 0.8; }
        100% { transform: translateY(320px); opacity: 0; }
      }
      @keyframes blink {
        0%, 100% { opacity: 1; }
        50% { opacity: 0; }
      }
      .stream {
        font-family: 'Courier New', monospace;
        font-size: 13px;
        fill: #00FF41;
        writing-mode: vertical-rl;
        text-orientation: upright;
        letter-spacing: 3px;
      }
      .s1 { animation: fall 3.5s linear infinite; }
      .s2 { animation: fall 4.2s linear infinite 0.8s; }
      .s3 { animation: fall 3.0s linear infinite 1.5s; }
      .s4 { animation: fall 4.8s linear infinite 0.3s; }
      .s5 { animation: fall 3.7s linear infinite 2.0s; }
      .s6 { animation: fall 4.0s linear infinite 1.1s; }
      .s7 { animation: fall 3.3s linear infinite 2.5s; }
      .s8 { animation: fall 4.5s linear infinite 0.6s; }

      .term-title {
        font-family: 'Consolas', 'Fira Code', monospace;
        font-size: 26px;
        font-weight: bold;
        fill: #00FF41;
        letter-spacing: 2px;
      }
      .cursor {
        animation: blink 0.9s infinite;
        fill: #00FF41;
      }
      .sub-title {
        font-family: 'Consolas', 'Fira Code', monospace;
        font-size: 16px;
        font-weight: bold;
        fill: #e6edf3;
        letter-spacing: 1px;
      }
      .badge-label {
        font-family: 'Consolas', monospace;
        font-size: 12px;
        font-weight: 900;
        fill: #ffffff;
        letter-spacing: 1.5px;
      }
      .badge-val {
        font-family: 'Consolas', monospace;
        font-size: 12px;
        font-weight: 900;
        fill: #000000;
        letter-spacing: 1.5px;
      }
    </style>
  </defs>

  <!-- Fundo Escuro com Borda Verde Neon Glow -->
  <rect x="5" y="5" width="840" height="330" rx="10" fill="#020d04" stroke="#00FF41" stroke-width="2" filter="url(#box-glow)" />

  <!-- Chuva de Código Matrix (Colunas Laterais) -->
  <g opacity="0.35">
    <text x="35" y="0" class="stream s1">01101001010110</text>
    <text x="75" y="0" class="stream s2">10011101001010</text>
    <text x="120" y="0" class="stream s3">01010100110011</text>
    <text x="165" y="0" class="stream s4">11001010101100</text>
    <text x="680" y="0" class="stream s5">00110101101001</text>
    <text x="725" y="0" class="stream s6">10101001011010</text>
    <text x="770" y="0" class="stream s7">01110010110100</text>
    <text x="815" y="0" class="stream s8">11010101001011</text>
  </g>

  <!-- Ícone de Terminal Topo -->
  <g transform="translate(413, 30)" opacity="0.7">
    <rect x="-16" y="-12" width="32" height="24" rx="4" fill="none" stroke="#00FF41" stroke-width="1.8" />
    <path d="M-8 -3 L-3 0 L-8 3 M0 3 L6 3" stroke="#00FF41" stroke-width="1.8" fill="none" stroke-linecap="round" />
  </g>

  <!-- Texto Central Neon -->
  <g filter="url(#matrix-glow)">
    <text x="425" y="105" text-anchor="middle" class="term-title">Conectado na Matrix.</text>
  </g>
  <rect x="585" y="87" width="12" height="22" class="cursor" />

  <!-- Linha Divisória com Efeito Fosforescente -->
  <line x1="80" y1="140" x2="770" y2="140" stroke="#003B00" stroke-width="1.5" />
  <line x1="260" y1="140" x2="590" y2="140" stroke="#00FF41" stroke-width="2" filter="url(#matrix-glow)" />

  <!-- Subtítulo -->
  <text x="425" y="185" text-anchor="middle" class="sub-title">Terminal // System Status: Online</text>

  <!-- ================= BADGES DE STATUS (ESTILO MATRIX) ================= -->
  
  <!-- BADGE 1: STATUS / OPERACIONAL -->
  <g transform="translate(145, 230)">
    <rect x="0" y="0" width="80" height="34" rx="5" fill="#000000" stroke="#00FF41" stroke-width="1.5" />
    <text x="40" y="21" text-anchor="middle" class="badge-label">STATUS</text>
    <rect x="80" y="0" width="115" height="34" rx="5" fill="#00FF41" filter="url(#matrix-glow)" />
    <text x="137" y="21" text-anchor="middle" class="badge-val">OPERACIONAL</text>
  </g>

  <!-- BADGE 2: SECURITY / BYPASSED -->
  <g transform="translate(360, 230)">
    <rect x="0" y="0" width="90" height="34" rx="5" fill="#000000" stroke="#00FF41" stroke-width="1.5" />
    <text x="45" y="21" text-anchor="middle" class="badge-label">SECURITY</text>
    <rect x="90" y="0" width="95" height="34" rx="5" fill="#00FF41" filter="url(#matrix-glow)" />
    <text x="137" y="21" text-anchor="middle" class="badge-val">BYPASSED</text>
  </g>

  <!-- BADGE 3: USER / ALLYSON PONTES -->
  <g transform="translate(565, 230)">
    <rect x="0" y="0" width="65" height="34" rx="5" fill="#000000" stroke="#00FF41" stroke-width="1.5" />
    <text x="32" y="21" text-anchor="middle" class="badge-label">USER</text>
    <rect x="65" y="0" width="140" height="34" rx="5" fill="#00FF41" filter="url(#matrix-glow)" />
    <text x="135" y="21" text-anchor="middle" class="badge-val">ALLYSON PONTES</text>
  </g>

</svg>
