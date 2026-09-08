<div align="center">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1300 280" width="100%" height="100%">
  <defs>
    <!-- Background Gradient -->
    <linearGradient id="bgGradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#020f0c" />
      <stop offset="20%" stop-color="#031613" />
      <stop offset="50%" stop-color="#072b26" />
      <stop offset="80%" stop-color="#031613" />
      <stop offset="100%" stop-color="#020f0c" />
    </linearGradient>

    <!-- Speed Lines Fade Gradients Starting from Edges -->
    <linearGradient id="laserFadeLeft" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#2de370" stop-opacity="0.9" />
      <stop offset="70%" stop-color="#39ff14" stop-opacity="0.6" />
      <stop offset="100%" stop-color="#80ffb4" stop-opacity="0" />
    </linearGradient>

    <linearGradient id="laserFadeRight" x1="100%" y1="0%" x2="0%" y2="0%">
      <stop offset="0%" stop-color="#2de370" stop-opacity="0.9" />
      <stop offset="70%" stop-color="#39ff14" stop-opacity="0.6" />
      <stop offset="100%" stop-color="#80ffb4" stop-opacity="0" />
    </linearGradient>

    <!-- Glow Filters -->
    <filter id="glow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="5" result="blur" />
      <feMerge>
        <feMergeNode in="blur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <filter id="superGlow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="8" result="blur1" />
      <feGaussianBlur stdDeviation="3" result="blur2" />
      <feMerge>
        <feMergeNode in="blur1" />
        <feMergeNode in="blur2" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <!-- Tech Badge Style -->
    <linearGradient id="badgeBg" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.12" />
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0.04" />
    </linearGradient>

    <style>
      @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800;900&amp;family=Fira+Code:wght@700&amp;display=swap');

      /* Center Header Typography */
      .main-title {
        font-family: 'Inter', system-ui, -apple-system, sans-serif;
        font-weight: 900;
        font-size: 52px;
        fill: #ffffff;
        letter-spacing: 2.5px;
        filter: drop-shadow(0 0 10px rgba(78, 255, 172, 0.55));
        animation: pulseTitleGlow 4s ease-in-out infinite alternate;
      }

      .subtitle {
        font-family: 'Inter', system-ui, -apple-system, sans-serif;
        font-weight: 700;
        font-size: 19px;
        fill: #b5e8dc;
        letter-spacing: 7px;
      }

      .code-tag {
        font-family: 'Fira Code', monospace;
        font-weight: 700;
        font-size: 26px;
        fill: #61f7a1;
        filter: drop-shadow(0 0 6px rgba(97, 247, 161, 0.8));
      }

      .tag-text {
        font-family: 'Inter', system-ui, -apple-system, sans-serif;
        font-weight: 600;
        font-size: 13px;
        fill: #d8f5ee;
      }

      /* Edge Circuits */
      .circuit-base {
        fill: none;
        stroke: #123e32;
        stroke-width: 2.2;
        stroke-linecap: round;
        stroke-linejoin: round;
      }

      .circuit-terminal {
        fill: #041a17;
        stroke: #257d66;
        stroke-width: 2.2;
      }

      /* Animated Electric Currents */
      .electric-stream {
        fill: none;
        stroke: #52ff9e;
        stroke-width: 2.6;
        stroke-linecap: round;
        stroke-linejoin: round;
        stroke-dasharray: 80 500;
        filter: url(#glow);
        animation: electricFlow 3.6s linear infinite;
      }

      .stream-delay-1 { animation-delay: 0s; }
      .stream-delay-2 { animation-delay: -1.2s; }
      .stream-delay-3 { animation-delay: -2.4s; }

      /* Neon Pulsing Dots */
      .glowing-node {
        fill: #b3ffd4;
        filter: url(#superGlow);
        animation: nodePulse 2.4s ease-in-out infinite alternate;
      }
      .node-d1 { animation-delay: -0.4s; }
      .node-d2 { animation-delay: -1.2s; }
      .node-d3 { animation-delay: -1.8s; }

      /* Speed / Laser Lashes */
      .speed-line-left {
        stroke: url(#laserFadeLeft);
        stroke-linecap: round;
        animation: laserRush 2.8s ease-in-out infinite alternate;
      }

      .speed-line-right {
        stroke: url(#laserFadeRight);
        stroke-linecap: round;
        animation: laserRush 2.8s ease-in-out infinite alternate;
      }

      /* Twinkling Stars */
      .star {
        fill: #85fbd2;
        animation: starTwinkle 2.5s infinite ease-in-out alternate;
      }

      /* Keyframes */
      @keyframes electricFlow {
        0% { stroke-dashoffset: 580; }
        100% { stroke-dashoffset: 0; }
      }

      @keyframes nodePulse {
        0% { r: 5.5; opacity: 0.6; }
        100% { r: 9; opacity: 1; filter: drop-shadow(0 0 12px #39ff94); }
      }

      @keyframes laserRush {
        0% { stroke-width: 2.5; opacity: 0.7; }
        100% { stroke-width: 4.5; opacity: 1; }
      }

      @keyframes pulseTitleGlow {
        0% { filter: drop-shadow(0 0 6px rgba(78, 255, 172, 0.35)); }
        100% { filter: drop-shadow(0 0 16px rgba(78, 255, 172, 0.75)); }
      }

      @keyframes starTwinkle {
        0% { opacity: 0.15; transform: scale(0.8); }
        100% { opacity: 0.85; transform: scale(1.3); }
      }
    </style>
  </defs>

  <!-- Background Canvas -->
  <rect width="1300" height="280" fill="url(#bgGradient)" />

  <!-- Stars across entire canvas (filling outer edge space) -->
  <g>
    <circle class="star" cx="40" cy="35" r="1.5" style="animation-delay: 0.3s;" />
    <circle class="star" cx="80" cy="115" r="1.2" style="animation-delay: 1.2s;" />
    <circle class="star" cx="130" cy="45" r="1.8" style="animation-delay: 0.6s;" />
    <circle class="star" cx="60" cy="245" r="1.4" style="animation-delay: 1.8s;" />
    <circle class="star" cx="190" cy="160" r="1.3" style="animation-delay: 0.9s;" />
    <circle class="star" cx="260" cy="260" r="1.5" style="animation-delay: 1.4s;" />
    <circle class="star" cx="320" cy="30" r="1.6" style="animation-delay: 0.2s;" />

    <circle class="star" cx="1260" cy="35" r="1.5" style="animation-delay: 0.5s;" />
    <circle class="star" cx="1220" cy="115" r="1.2" style="animation-delay: 1.6s;" />
    <circle class="star" cx="1170" cy="45" r="1.8" style="animation-delay: 0.1s;" />
    <circle class="star" cx="1240" cy="245" r="1.4" style="animation-delay: 1.1s;" />
    <circle class="star" cx="1110" cy="160" r="1.3" style="animation-delay: 0.7s;" />
    <circle class="star" cx="1040" cy="260" r="1.5" style="animation-delay: 1.9s;" />
    <circle class="star" cx="980" cy="30" r="1.6" style="animation-delay: 0.4s;" />
  </g>

  <!-- ==================== LEFT WING (Full Edge Extension: x=0 to x=430) ==================== -->
  <g id="left-wing">
    <!-- Edge Lasers -->
    <line class="speed-line-left" x1="0" y1="42" x2="220" y2="42" stroke-width="3" style="animation-delay: 0.1s;" />
    <line class="speed-line-left" x1="0" y1="88" x2="310" y2="88" stroke-width="3.5" style="animation-delay: 0.5s;" />
    <line class="speed-line-left" x1="0" y1="125" x2="260" y2="125" stroke-width="4.2" style="animation-delay: 1.1s;" />
    <line class="speed-line-left" x1="0" y1="168" x2="350" y2="168" stroke-width="4" style="animation-delay: 0.3s;" />
    <line class="speed-line-left" x1="0" y1="210" x2="240" y2="210" stroke-width="3.2" style="animation-delay: 0.8s;" />
    <line class="speed-line-left" x1="0" y1="248" x2="330" y2="248" stroke-width="2.8" style="animation-delay: 1.4s;" />

    <!-- Static Extended Tracks -->
    <!-- Edge Outer Track 1 -->
    <path class="circuit-base" d="M0 55 L70 55 L105 30 L220 30 L250 55 L360 55" />
    <circle class="circuit-terminal" cx="364" cy="55" r="4.5" />

    <!-- Edge Outer Track 2 -->
    <path class="circuit-base" d="M0 95 L95 95 L135 65 L260 65 L290 85 L395 85" />
    <circle class="circuit-terminal" cx="399" cy="85" r="4.5" />

    <!-- Edge Track 3 -->
    <path class="circuit-base" d="M0 135 L120 135 L165 95 L275 95 L305 60 L380 60" />
    <circle class="circuit-terminal" cx="384" cy="60" r="4.5" />

    <!-- Main Inflow Track 4 -->
    <path class="circuit-base" d="M0 155 L145 155 L190 115 L320 115 L350 78 L420 78" />
    <circle class="circuit-terminal" cx="424" cy="78" r="4.5" />

    <!-- Deep Loop Track 5 -->
    <path class="circuit-base" d="M0 180 L110 180 L160 220 L270 220 L310 160 L410 160" />
    <circle class="circuit-terminal" cx="414" cy="160" r="4.5" />

    <!-- Bottom Outer Track 6 -->
    <path class="circuit-base" d="M0 225 L85 225 L125 185 L230 185 L265 240 L385 240" />
    <circle class="circuit-terminal" cx="389" cy="240" r="4.5" />

    <!-- Extra Edge Filler Track 7 -->
    <path class="circuit-base" d="M30 260 L140 260 L180 215 L250 215" />
    <circle class="circuit-terminal" cx="254" cy="215" r="4.5" />

    <!-- Electric Pulses Traversing Full Length -->
    <path class="electric-stream stream-delay-1" d="M0 55 L70 55 L105 30 L220 30 L250 55 L360 55" />
    <path class="electric-stream stream-delay-2" d="M0 95 L95 95 L135 65 L260 65 L290 85 L395 85" />
    <path class="electric-stream stream-delay-3" d="M0 135 L120 135 L165 95 L275 95 L305 60 L380 60" />
    <path class="electric-stream stream-delay-1" d="M0 155 L145 155 L190 115 L320 115 L350 78 L420 78" />
    <path class="electric-stream stream-delay-2" d="M0 180 L110 180 L160 220 L270 220 L310 160 L410 160" />
    <path class="electric-stream stream-delay-3" d="M0 225 L85 225 L125 185 L230 185 L265 240 L385 240" />

    <!-- Distributed Glowing Nodes (from edge to center) -->
    <circle class="glowing-node node-d1" cx="70" cy="55" r="6" />
    <circle class="glowing-node node-d3" cx="120" cy="135" r="7" />
    <circle class="glowing-node node-d2" cx="220" cy="30" r="6.5" />
    <circle class="glowing-node node-d1" cx="270" cy="220" r="7.5" />
    <circle class="glowing-node node-d2" cx="320" cy="115" r="8" />
    <circle class="glowing-node node-d3" cx="160" cy="220" r="6" />
  </g>

  <!-- ==================== RIGHT WING (Full Edge Extension: Mirrored x=1300 to x=870) ==================== -->
  <g id="right-wing" transform="translate(1300, 0) scale(-1, 1)">
    <!-- Edge Lasers -->
    <line class="speed-line-right" x1="0" y1="42" x2="220" y2="42" stroke-width="3" style="animation-delay: 0.3s;" />
    <line class="speed-line-right" x1="0" y1="88" x2="310" y2="88" stroke-width="3.5" style="animation-delay: 0.8s;" />
    <line class="speed-line-right" x1="0" y1="125" x2="260" y2="125" stroke-width="4.2" style="animation-delay: 0.2s;" />
    <line class="speed-line-right" x1="0" y1="168" x2="350" y2="168" stroke-width="4" style="animation-delay: 1.4s;" />
    <line class="speed-line-right" x1="0" y1="210" x2="240" y2="210" stroke-width="3.2" style="animation-delay: 0.6s;" />
    <line class="speed-line-right" x1="0" y1="248" x2="330" y2="248" stroke-width="2.8" style="animation-delay: 1.1s;" />

    <!-- Static Extended Tracks -->
    <path class="circuit-base" d="M0 55 L70 55 L105 30 L220 30 L250 55 L360 55" />
    <circle class="circuit-terminal" cx="364" cy="55" r="4.5" />

    <path class="circuit-base" d="M0 95 L95 95 L135 65 L260 65 L290 85 L395 85" />
    <circle class="circuit-terminal" cx="399" cy="85" r="4.5" />

    <path class="circuit-base" d="M0 135 L120 135 L165 95 L275 95 L305 60 L380 60" />
    <circle class="circuit-terminal" cx="384" cy="60" r="4.5" />

    <path class="circuit-base" d="M0 155 L145 155 L190 115 L320 115 L350 78 L420 78" />
    <circle class="circuit-terminal" cx="424" cy="78" r="4.5" />

    <path class="circuit-base" d="M0 180 L110 180 L160 220 L270 220 L310 160 L410 160" />
    <circle class="circuit-terminal" cx="414" cy="160" r="4.5" />

    <path class="circuit-base" d="M0 225 L85 225 L125 185 L230 185 L265 240 L385 240" />
    <circle class="circuit-terminal" cx="389" cy="240" r="4.5" />

    <path class="circuit-base" d="M30 260 L140 260 L180 215 L250 215" />
    <circle class="circuit-terminal" cx="254" cy="215" r="4.5" />

    <!-- Electric Pulses -->
    <path class="electric-stream stream-delay-2" d="M0 55 L70 55 L105 30 L220 30 L250 55 L360 55" />
    <path class="electric-stream stream-delay-3" d="M0 95 L95 95 L135 65 L260 65 L290 85 L395 85" />
    <path class="electric-stream stream-delay-1" d="M0 135 L120 135 L165 95 L275 95 L305 60 L380 60" />
    <path class="electric-stream stream-delay-2" d="M0 155 L145 155 L190 115 L320 115 L350 78 L420 78" />
    <path class="electric-stream stream-delay-3" d="M0 180 L110 180 L160 220 L270 220 L310 160 L410 160" />
    <path class="electric-stream stream-delay-1" d="M0 225 L85 225 L125 185 L230 185 L265 240 L385 240" />

    <!-- Glowing Nodes -->
    <circle class="glowing-node node-d2" cx="70" cy="55" r="6" />
    <circle class="glowing-node node-d1" cx="120" cy="135" r="7" />
    <circle class="glowing-node node-d3" cx="220" cy="30" r="6.5" />
    <circle class="glowing-node node-d2" cx="270" cy="220" r="7.5" />
    <circle class="glowing-node node-d1" cx="320" cy="115" r="8" />
    <circle class="glowing-node node-d3" cx="160" cy="220" r="6" />
  </g>

  <!-- ==================== CENTER HERO CONTENT ==================== -->
  <g id="center-content">
    
    <!-- Code Bracket Icon with Accent Lines -->
    <g transform="translate(650, 48)">
      <line x1="-120" y1="-8" x2="-40" y2="-8" stroke="#1c6b54" stroke-width="2" stroke-linecap="round" />
      <text x="0" y="0" class="code-tag" text-anchor="middle">&lt; / &gt;</text>
      <line x1="40" y1="-8" x2="120" y2="-8" stroke="#1c6b54" stroke-width="2" stroke-linecap="round" />
    </g>

    <!-- Main Title -->
    <text x="650" y="118" class="main-title" text-anchor="middle">SIAM AL RABBI</text>

    <!-- Subtitle -->
    <text x="650" y="156" class="subtitle" text-anchor="middle">FULL-STACK DEVELOPER</text>

    <!-- Tech Stack Pill Badges (Centered) -->
    <g transform="translate(367.5, 185)">
      
      <!-- Next.js (Authentic Black 'N' Icon inside White Circle) -->
      <g transform="translate(0, 0)">
        <rect width="98" height="34" rx="17" fill="url(#badgeBg)" stroke="#2f6354" stroke-width="1.2" />
        <circle cx="21" cy="17" r="10.5" fill="#ffffff" />
        
        <g id="nextjs-n">
          <rect x="16.5" y="11.2" width="2" height="11.2" rx="0.5" fill="#000000" />
          <rect x="23.5" y="11.2" width="2" height="8.2" rx="0.5" fill="#000000" />
          <polygon points="16.5,11.2 18.5,11.2 27.2,24.2 25.2,24.2" fill="#000000" />
        </g>

        <text x="60" y="22" class="tag-text" text-anchor="middle">Next.js</text>
      </g>

      <!-- React -->
      <g transform="translate(108, 0)">
        <rect width="96" height="34" rx="17" fill="url(#badgeBg)" stroke="#2f6354" stroke-width="1.2" />
        <ellipse cx="21" cy="17" rx="9" ry="3.5" fill="none" stroke="#58c4dc" stroke-width="1.2" transform="rotate(30 21 17)" />
        <ellipse cx="21" cy="17" rx="9" ry="3.5" fill="none" stroke="#58c4dc" stroke-width="1.2" transform="rotate(90 21 17)" />
        <ellipse cx="21" cy="17" rx="9" ry="3.5" fill="none" stroke="#58c4dc" stroke-width="1.2" transform="rotate(150 21 17)" />
        <circle cx="21" cy="17" r="1.5" fill="#58c4dc" />
        <text x="56" y="22" class="tag-text" text-anchor="middle">React</text>
      </g>

      <!-- TypeScript -->
      <g transform="translate(214, 0)">
        <rect width="118" height="34" rx="17" fill="url(#badgeBg)" stroke="#2f6354" stroke-width="1.2" />
        <rect x="12" y="9" width="16" height="16" rx="3" fill="#3178c6" />
        <text x="20" y="21" font-family="'Inter', sans-serif" font-weight="800" font-size="9" fill="#ffffff" text-anchor="middle">TS</text>
        <text x="69" y="22" class="tag-text" text-anchor="middle">TypeScript</text>
      </g>

      <!-- Node.js -->
      <g transform="translate(342, 0)">
        <rect width="105" height="34" rx="17" fill="url(#badgeBg)" stroke="#2f6354" stroke-width="1.2" />
        <rect x="12" y="9" width="16" height="16" rx="3" fill="#215732" />
        <text x="20" y="21" font-family="'Inter', sans-serif" font-weight="800" font-size="9" fill="#83cd29" text-anchor="middle">JS</text>
        <text x="63" y="22" class="tag-text" text-anchor="middle">Node.js</text>
      </g>

      <!-- MongoDB -->
      <g transform="translate(457, 0)">
        <rect width="112" height="34" rx="17" fill="url(#badgeBg)" stroke="#2f6354" stroke-width="1.2" />
        <path d="M19 9 C19 9 14 14 14 18 C14 21.5 17 24 19 25 C21 24 24 21.5 24 18 C24 14 19 9 19 9 Z" fill="#47a248" />
        <path d="M19 9 L19 25" stroke="#ffffff" stroke-width="0.8" opacity="0.6" />
        <text x="68" y="22" class="tag-text" text-anchor="middle">MongoDB</text>
      </g>

    </g>
  </g>
</svg>

<img width="900" height="160" alt="Github-Welcome" src="https://github.com/user-attachments/assets/65610cf5-1b90-46bf-bb5a-f3801d22825f" />
<svg fill="none" viewBox="0 0 900 160" width="900" height="160" xmlns="http://www.w3.org/2000/svg">
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:ital,wght@1,800;1,900&amp;display=swap');

        * {
          box-sizing: border-box;
          margin: 0;
          padding: 0;
        }

        .banner-container {
          position: relative;
          width: 880px;
          height: 145px;
          background: #ffffff;
          border-radius: 14px;
          border: 6px solid #1f1f1f;
          display: flex;
          align-items: center;
          justify-content: center;
          overflow: hidden;
          margin: 6px auto;
        }

        .phrase-group {
          position: absolute;
          inset: 0;
          display: flex;
          align-items: center;
          justify-content: center;
          pointer-events: none;
          opacity: 0;
          animation-duration: 14.73s;
          animation-timing-function: linear;
          animation-iteration-count: infinite;
        }

        .group-one { --travel-dist: 180px; animation-name: groupOneSeq; }
        .group-two { --travel-dist: 380px; animation-name: groupTwoSeq; }
        .group-three { --travel-dist: 225px; animation-name: groupThreeSeq; }

        .text-phrase {
          position: absolute;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
          white-space: nowrap;
          color: #0a0a0a;
          font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
          font-size: 40px;
          font-weight: 800;
          font-style: italic;
          letter-spacing: -0.8px;
          clip-path: inset(0 50% 0 50%);
          animation: textReveal 14.73s linear infinite;
        }

        .line {
          position: absolute;
          left: 50%;
          top: 50%;
          width: 135px;
          height: 6px;
          background: #1f7bfa;
          transform-origin: center center;
          border-radius: 2px;
          animation-duration: 14.73s;
          animation-timing-function: linear;
          animation-iteration-count: infinite;
        }

        .line-left  { animation-name: leftLineTravel; }
        .line-right { animation-name: rightLineTravel; }

        @keyframes groupOneSeq {
          0%, 33.32%   { opacity: 1; }
          33.33%, 100% { opacity: 0; }
        }
        @keyframes groupTwoSeq {
          0%, 33.32%   { opacity: 0; }
          33.33%, 66.65% { opacity: 1; }
          66.66%, 100% { opacity: 0; }
        }
        @keyframes groupThreeSeq {
          0%, 66.65%   { opacity: 0; }
          66.66%, 100% { opacity: 1; }
        }

        @keyframes leftLineTravel {
          0.00%, 33.33%, 66.66% { transform: translate(-50%, -50%) rotate(90deg) scaleX(0.02); }
          2.03%, 35.36%, 68.69% { transform: translate(-50%, -50%) rotate(90deg) scaleX(1); }
          3.80%, 37.13%, 70.46% { transform: translate(-50%, -50%) rotate(-45deg) scaleX(1); }
          6.77%, 40.10%, 73.43% { transform: translate(-59%, -50%) rotate(-45deg) scaleX(1); }
          12.40%, 45.73%, 79.06% { transform: translate(calc(-50% - var(--travel-dist)), -50%) rotate(-45deg) scaleX(1); }
          20.73%, 54.06%, 87.39% { transform: translate(calc(-50% - var(--travel-dist)), -50%) rotate(-45deg) scaleX(1); }
          26.77%, 60.10%, 93.43% { transform: translate(-50%, -50%) rotate(-45deg) scaleX(1); }
          28.40%, 61.73%, 95.06% { transform: translate(-50%, -50%) rotate(90deg) scaleX(1); }
          33.32%, 66.65%, 100.0% { transform: translate(-50%, -50%) rotate(90deg) scaleX(0.02); }
        }

        @keyframes rightLineTravel {
          0.00%, 33.33%, 66.66% { transform: translate(-50%, -50%) rotate(90deg) scaleX(0.02); }
          2.03%, 35.36%, 68.69% { transform: translate(-50%, -50%) rotate(90deg) scaleX(1); }
          3.80%, 37.13%, 70.46% { transform: translate(-50%, -50%) rotate(-45deg) scaleX(1); }
          6.77%, 40.10%, 73.43% { transform: translate(-41%, -50%) rotate(-45deg) scaleX(1); }
          12.40%, 45.73%, 79.06% { transform: translate(calc(-50% + var(--travel-dist)), -50%) rotate(-45deg) scaleX(1); }
          20.73%, 54.06%, 87.39% { transform: translate(calc(-50% + var(--travel-dist)), -50%) rotate(-45deg) scaleX(1); }
          26.77%, 60.10%, 93.43% { transform: translate(-50%, -50%) rotate(-45deg) scaleX(1); }
          28.40%, 61.73%, 95.06% { transform: translate(-50%, -50%) rotate(90deg) scaleX(1); }
          33.32%, 66.65%, 100.0% { transform: translate(-50%, -50%) rotate(90deg) scaleX(0.02); }
        }

        @keyframes textReveal {
          0.0%, 6.6%, 33.33%, 39.9%, 66.66%, 73.2% { clip-path: inset(0 50% 0 50%); }
          9.0%, 42.3%, 75.6% { clip-path: inset(0 32% 0 32%); }
          11.3%, 44.6%, 77.9% { clip-path: inset(0 15% 0 15%); }
          12.6%, 20.6%, 45.9%, 53.9%, 79.2%, 87.2% { clip-path: inset(0 0% 0 0%); }
          23.3%, 56.6%, 89.9% { clip-path: inset(0 12% 0 12%); }
          25.6%, 58.9%, 92.2% { clip-path: inset(0 30% 0 30%); }
          26.8%, 33.32%, 60.1%, 66.65%, 93.4%, 100% { clip-path: inset(0 50% 0 50%); }
        }
      </style>

      <div class="banner-container">
        <div class="phrase-group group-one">
          <h1 class="text-phrase">Hello there!</h1>
          <div class="line line-left"></div>
          <div class="line line-right"></div>
        </div>
        <div class="phrase-group group-two">
          <h1 class="text-phrase">I'm Siam, a Full-Stack Developer.</h1>
          <div class="line line-left"></div>
          <div class="line line-right"></div>
        </div>
        <div class="phrase-group group-three">
          <h1 class="text-phrase">Nice to meet you!</h1>
          <div class="line line-left"></div>
          <div class="line line-right"></div>
        </div>
      </div>
    </div>
  </foreignObject>
</svg>


<img width="300" height="65" alt="Github-Cover" src="https://github.com/user-attachments/assets/654939be-dcbf-4dea-860b-1f648c193037" />


<p>
<img src="https://komarev.com/ghpvc/?username=Siam-AR&label=Profile+Views&color=6C63FF&style=for-the-badge"/>
<img src="https://img.shields.io/github/followers/Siam-AR?style=for-the-badge"/>
</p>

</div>

---

# <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="35"> About Me

<table>
<tr>

<td width="60%">

### 👨‍💻 Who Am I?

I'm **Siam Al Rabbi**, a **Computer Science & Engineering** student passionate about creating scalable, responsive, and user-friendly web applications.

I enjoy transforming ideas into real-world products using the **MERN Stack** while continuously learning modern technologies and software engineering principles.

### 🚀 Current Activities

- 🔭 Building **SkillSwap** — A Full-Stack Skill Exchange Platform
- 🌱 Learning **Next.js** & **TypeScript**
- 💡 Exploring Software Architecture & System Design
- ⚡ Passionate about writing clean, maintainable code

</td>

<td width="40%" align="center">
<div>
  <p align="center">
  <img src="https://github.com/demartini/demartini/blob/master/code.gif">
</p>
  </a>
</p>
</div>
</td>

</tr>
</table>

---

# <img src="https://media.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif" width="35"> Tech Stack

<div align="center">

## 🎨 Frontend

<img src="https://skillicons.dev/icons?i=html,css,js,ts,react,nextjs,tailwind" />

<br><br>

## ⚙️ Backend

<img src="https://techstack-generator.vercel.app/nodejs-icon.svg" width="65"/>
<img src="https://user-images.githubusercontent.com/74038190/212257460-738ff738-247f-4445-a718-cdd0ca76e2db.gif" width="65"/>
<img src="https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/assets/74038190/1a797f46-efe4-41e6-9e75-5303e1bbcbfa" width="65"/>

<br><br>

## 🗄️ Database

<img src="https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/assets/74038190/398b19b1-9aae-4c1f-8bc0-d172a2c08d68" width="65"/>
<img src="https://techstack-generator.vercel.app/mysql-icon.svg" width="65"/>
<img src="https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub/assets/74038190/3c16d4f2-b757-4c70-8f42-43d5dddd2c36" width="65"/>

<br><br>

## 🛠️ Tools

<img src="https://user-images.githubusercontent.com/74038190/212281775-b468df30-4edc-4bf8-a4ee-f52e1aaddc86.gif" width="65"/>
<img src="https://user-images.githubusercontent.com/74038190/212257468-1e9a91f1-b626-4baa-b15d-5c385dfa7ed2.gif" width="65"/>
<img src="https://user-images.githubusercontent.com/74038190/212257465-7ce8d493-cac5-494e-982a-5a9deb852c4b.gif" width="65"/>

<br><br>

<img src="https://skillicons.dev/icons?i=github,git,vscode,linux,figma,postman,vercel,firebase" />

</div>

---

# 🚀 Featured Project

<div align="center">

## 🌟 SkillSwap

*A Modern Full-Stack Skill Exchange Platform*

<img src="https://img.shields.io/badge/Status-In%20Development-success?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Type-Full--Stack-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/License-MIT-orange?style=for-the-badge"/>

</div>

SkillSwap is a modern web application where users can exchange skills, discover learning partners, send swap requests, and collaborate with others through a clean, responsive, and user-friendly interface.

### ✨ Key Features

- 🔐 Secure Firebase Authentication
- 👤 User Profiles & Skill Management
- 🔄 Skill Swap Requests
- ❤️ Like & Save Skills
- 🌙 Dark Mode
- 📱 Fully Responsive Design
- ⚡ Fast Performance with Next.js
- 🎯 Clean & Modern UI

### 🛠 Built With

<div align="center">

<img src="https://skillicons.dev/icons?i=nextjs,react,ts,nodejs,express,mongodb,firebase,tailwind"/>

</div>

---

# <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="32"> GitHub Statistics

<div align="center">

<img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Siam-AR&theme=github_dark" width="100%" />

<br><br>

<img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Siam-AR&theme=github_dark" width="32%" />

<img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Siam-AR&theme=github_dark" width="32%" />

<img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Siam-AR&theme=github_dark" width="32%" />

<br><br>

<!-- <img src="https://streak-stats.demolab.com?user=Siam-AR&theme=github-dark&hide_border=true" width="75%" /> -->

<!-- <br><br> -->

<!-- <img src="https://github-readme-activity-graph.vercel.app/graph?username=Siam-AR&theme=github-dark&hide_border=true" width="100%" /> -->

</div>

---

# 🤝 Connect With Me

<div align="center">

<a href="https://github.com/Siam-AR">
<img src="https://skillicons.dev/icons?i=github" width="50"/>
</a>

&nbsp;&nbsp;&nbsp;

<a href="https://linkedin.com/in/siam-ar">
<img src="https://skillicons.dev/icons?i=linkedin" width="50"/>
</a>

&nbsp;&nbsp;&nbsp;

<a href="mailto:siam.ar.nexus@gmail.com">
<img src="https://skillicons.dev/icons?i=gmail" width="50"/>
</a>

</div>

<br>

<div align="center">

### 📫 Reach Me

📍 **Location:** Dhaka, Bangladesh 🇧🇩

📧 **Email:** siam.ar.nexus@gmail.com

📱 **Phone:** +880 1612890989

</div>

---

<div align="center">

### 💙 Thanks for visiting my profile!

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&duration=3500&pause=1200&center=true&vCenter=true&width=500&lines=Thanks+for+visiting!;Happy+Coding!+🚀;See+you+again!+👋" />

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=6C63FF&height=120&section=footer"/>

</div>

