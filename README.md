<svg viewBox="0 0 900 260" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="textFace" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#ffffff"/>
      <stop offset="45%" stop-color="#00C9A7"/>
      <stop offset="100%" stop-color="#6C63FF"/>
    </linearGradient>
    <radialGradient id="bg" cx="50%" cy="50%" r="75%">
      <stop offset="0%" stop-color="#161b22"/>
      <stop offset="100%" stop-color="#0d1117"/>
    </radialGradient>
    <filter id="soft" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="2.2"/>
    </filter>
  </defs>

  <rect width="900" height="260" rx="18" fill="url(#bg)"/>

  <!-- ===== 3D extruded text: stacked offset copies build the "depth" ===== -->
  <g font-family="Verdana, 'Segoe UI', sans-serif" font-weight="900" font-size="58" text-anchor="middle">
    <g id="extrude">
      <!-- 14 stepped layers, darkening toward the back, offset down-right to fake depth -->
      <text x="452" y="146" fill="#050608">PRINCE BHANDARI</text>
      <text x="451" y="145" fill="#0a0c10">PRINCE BHANDARI</text>
      <text x="450" y="144" fill="#12151c">PRINCE BHANDARI</text>
      <text x="449" y="143" fill="#1a1f29">PRINCE BHANDARI</text>
      <text x="448" y="142" fill="#232a36">PRINCE BHANDARI</text>
      <text x="447" y="141" fill="#2c3444">PRINCE BHANDARI</text>
      <text x="446" y="140" fill="#354152">PRINCE BHANDARI</text>
      <text x="445" y="139" fill="#3f4d60">PRINCE BHANDARI</text>
      <text x="444" y="138" fill="#485a6e">PRINCE BHANDARI</text>
      <text x="443" y="137" fill="#52677d">PRINCE BHANDARI</text>
      <text x="442" y="136" fill="#5c748c">PRINCE BHANDARI</text>
      <text x="441" y="135" fill="#66819b">PRINCE BHANDARI</text>
    </g>

    <!-- subtle drop shadow under the face layer -->
    <text x="440" y="134" fill="#000000" opacity="0.35" filter="url(#soft)">PRINCE BHANDARI</text>

    <!-- front face -->
    <text x="438" y="132" fill="url(#textFace)" stroke="#0d1117" stroke-width="1.5">PRINCE BHANDARI</text>

    <!-- gentle rocking to sell the 3D illusion -->
    <animateTransform attributeName="transform" type="rotate"
      values="0 450 132; 1.2 450 132; 0 450 132; -1.2 450 132; 0 450 132"
      dur="6s" repeatCount="indefinite"/>
  </g>

  <text x="450" y="185" text-anchor="middle" font-family="'Fira Code', monospace" font-size="16"
        fill="#8b949e">Associate Engineer Candidate · Full-Stack (MERN) · DSA · ML</text>

  <!-- ===== reusable spider ===== -->
  <g id="spider">
    <ellipse cx="0" cy="2" rx="6" ry="8" fill="#0d1117" stroke="#00C9A7" stroke-width="0.8"/>
    <circle cx="0" cy="-6" r="4" fill="#0d1117" stroke="#00C9A7" stroke-width="0.8"/>
    <g stroke="#00C9A7" stroke-width="1.3" fill="none" stroke-linecap="round">
      <path d="M-4,-2 Q-16,-8 -22,-2"/>
      <path d="M-4,1 Q-17,3 -23,9"/>
      <path d="M-4,4 Q-15,10 -19,17"/>
      <path d="M-4,7 Q-12,14 -13,22"/>
      <path d="M4,-2 Q16,-8 22,-2"/>
      <path d="M4,1 Q17,3 23,9"/>
      <path d="M4,4 Q15,10 19,17"/>
      <path d="M4,7 Q12,14 13,22"/>
    </g>
  </g>

  <!-- Spider 1: wide loop — right, up, left, down -->
  <use href="#spider">
    <animateMotion dur="7s" repeatCount="indefinite" rotate="auto"
      path="M60,225 L840,225 L840,25 L60,25 Z"/>
  </use>

  <!-- Spider 2: inner loop, opposite direction, offset start -->
  <use href="#spider">
    <animateMotion dur="9s" repeatCount="indefinite" rotate="auto" begin="-2s"
      path="M120,205 L120,45 L780,45 L780,205 Z"/>
  </use>

  <!-- Spider 3: smaller, faster diagonal-ish loop for variety -->
  <use href="#spider" transform="scale(0.8)">
    <animateMotion dur="5s" repeatCount="indefinite" rotate="auto" begin="-1s"
      path="M100,235 L500,235 L500,15 L100,15 Z"/>
  </use>
</svg>
