<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Raey ♡ — Frontend Developer</title>
    <link
      rel="icon"
      href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🌸</text></svg>"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400&family=Nunito:wght@300;400;600;700&display=swap"
      rel="stylesheet"
    />
    <style>
      *,
      *::before,
      *::after {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      :root {
        --sk: #f8bbd0;
        --sk2: #f48fb1;
        --mn: #e8d5f0;
        --mn2: #ce93d8;
        --bg: #fdf6f9;
        --bg2: #fff0f6;
        --tx: #5c3d52;
        --txm: #9e7b8e;
        --txl: #c5a3b5;
        --ac: #ad7fa8;
        --br: rgba(248, 187, 208, 0.5);
      }
      html {
        scroll-behavior: smooth;
      }
      body {
        background: var(--bg);
        font-family: "Nunito", sans-serif;
        color: var(--tx);
        min-height: 100vh;
      }
      /* ── HEADER ── */
      .hdr {
        position: relative;
        overflow: hidden;
        text-align: center;
        background: linear-gradient(
          160deg,
          #fde8f2 0%,
          #edd6f4 40%,
          #d9ecfa 100%
        );
        border-bottom: 1px solid var(--br);
      }
      .hdr-in {
        position: relative;
        z-index: 2;
        padding: 60px 32px 48px;
        max-width: 700px;
        margin: 0 auto;
      }
      /* floating petals */
      .petal {
        position: absolute;
        border-radius: 50% 0 50% 0;
        animation: fp linear infinite;
        pointer-events: none;
      }
      @keyframes fp {
        0% {
          transform: translateY(0) rotate(0deg);
          opacity: 0.18;
        }
        50% {
          opacity: 0.28;
        }
        100% {
          transform: translateY(-130px) rotate(360deg);
          opacity: 0.06;
        }
      }
      /* Genshin ornament */
      .orn {
        width: 60px;
        height: 60px;
        margin: 0 auto 18px;
      }
      .orn svg {
        width: 60px;
        height: 60px;
      }
      /* avatar */
      .av-ring {
        width: 96px;
        height: 96px;
        border-radius: 50%;
        margin: 0 auto 16px;
        background: linear-gradient(135deg, #f8bbd0, #ce93d8, #9fa8da);
        padding: 3px;
        box-shadow:
          0 0 0 7px rgba(248, 187, 208, 0.18),
          0 10px 36px rgba(173, 127, 168, 0.22);
      }
      .av-in {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        background: linear-gradient(135deg, #fde8f2, #edd6f4);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 36px;
      }
      .hdr h1 {
        font-family: "Cormorant Garamond", serif;
        font-size: 42px;
        font-weight: 500;
        color: #6d3f6a;
        letter-spacing: 2.5px;
        margin-bottom: 8px;
      }
      .hdr .sub {
        font-size: 14px;
        color: var(--txm);
        max-width: 420px;
        margin: 0 auto 18px;
        line-height: 1.8;
      }
      .spill {
        display: inline-flex;
        align-items: center;
        gap: 7px;
        background: rgba(255, 255, 255, 0.65);
        border: 1px solid var(--br);
        border-radius: 100px;
        padding: 6px 16px;
        font-size: 12.5px;
        color: var(--ac);
        font-weight: 600;
        backdrop-filter: blur(6px);
      }
      .sdot {
        width: 7px;
        height: 7px;
        border-radius: 50%;
        background: #a5d6a7;
        box-shadow: 0 0 0 2px rgba(165, 214, 167, 0.3);
        animation: pulse 2s ease-in-out infinite;
      }
      @keyframes pulse {
        0%,
        100% {
          box-shadow: 0 0 0 2px rgba(165, 214, 167, 0.3);
        }
        50% {
          box-shadow: 0 0 0 6px rgba(165, 214, 167, 0.12);
        }
      }
      /* element orbs */
      .erow {
        display: flex;
        justify-content: center;
        gap: 14px;
        flex-wrap: wrap;
        padding: 18px 0 4px;
      }
      .eorb {
        width: 38px;
        height: 38px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 17px;
        transition:
          transform 0.22s ease,
          box-shadow 0.22s ease;
        cursor: default;
      }
      .eorb:hover {
        transform: scale(1.18) rotate(-8deg);
      }
      .o-cry {
        background: radial-gradient(circle at 38% 38%, #e8f4fd, #90c8e8);
        box-shadow: 0 3px 12px rgba(144, 200, 232, 0.4);
      }
      .o-ane {
        background: radial-gradient(circle at 38% 38%, #e8faf2, #73c7aa);
        box-shadow: 0 3px 12px rgba(115, 199, 170, 0.4);
      }
      .o-hyd {
        background: radial-gradient(circle at 38% 38%, #e8effe, #7a9fe0);
        box-shadow: 0 3px 12px rgba(122, 159, 224, 0.4);
      }
      .o-pyr {
        background: radial-gradient(circle at 38% 38%, #fde8e8, #e07a7a);
        box-shadow: 0 3px 12px rgba(224, 122, 122, 0.4);
      }
      .o-ele {
        background: radial-gradient(circle at 38% 38%, #f0e8fd, #b07ae0);
        box-shadow: 0 3px 12px rgba(176, 122, 224, 0.4);
      }
      .o-geo {
        background: radial-gradient(circle at 38% 38%, #fdf3e8, #e0b87a);
        box-shadow: 0 3px 12px rgba(224, 184, 122, 0.4);
      }
      .o-den {
        background: radial-gradient(circle at 38% 38%, #eef9e8, #9ec87a);
        box-shadow: 0 3px 12px rgba(158, 200, 122, 0.4);
      }
      /* ── MAIN ── */
      .main {
        max-width: 720px;
        margin: 0 auto;
        padding: 36px 20px 56px;
        display: flex;
        flex-direction: column;
        gap: 26px;
      }
      /* ── CARD ── */
      .card {
        background: #fff;
        border-radius: 20px;
        border: 1px solid var(--br);
        overflow: hidden;
        box-shadow: 0 6px 28px rgba(173, 127, 168, 0.08);
        position: relative;
        transition:
          transform 0.2s ease,
          box-shadow 0.2s ease;
      }
      .card:hover {
        transform: translateY(-3px);
        box-shadow: 0 12px 36px rgba(173, 127, 168, 0.14);
      }
      .card::before,
      .card::after {
        content: "✦";
        position: absolute;
        font-size: 10px;
        color: rgba(248, 187, 208, 0.55);
        z-index: 1;
      }
      .card::before {
        top: 9px;
        left: 13px;
      }
      .card::after {
        top: 9px;
        right: 13px;
      }
      .ch {
        display: flex;
        align-items: center;
        gap: 11px;
        padding: 16px 22px 12px;
        border-bottom: 1px solid rgba(248, 187, 208, 0.22);
      }
      .ci {
        width: 30px;
        height: 30px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 15px;
        flex-shrink: 0;
      }
      .ct {
        font-family: "Cormorant Garamond", serif;
        font-size: 18px;
        font-weight: 500;
        color: #6d3f6a;
        letter-spacing: 0.5px;
      }
      .cb {
        padding: 18px 22px;
      }
      /* about list */
      .alist {
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 11px;
      }
      .alist li {
        display: flex;
        align-items: flex-start;
        gap: 10px;
        font-size: 14px;
        color: var(--tx);
        line-height: 1.55;
      }
      .ab {
        flex-shrink: 0;
        font-size: 15px;
        width: 26px;
        text-align: center;
      }
      /* tech chips */
      .tgrid {
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
      }
      .chip {
        display: flex;
        align-items: center;
        gap: 6px;
        padding: 6px 14px;
        border-radius: 100px;
        font-size: 12px;
        font-weight: 600;
        border: 1px solid;
        transition:
          transform 0.18s,
          box-shadow 0.18s;
        cursor: default;
        white-space: nowrap;
      }
      .chip:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 12px rgba(173, 127, 168, 0.2);
      }
      .cp {
        background: #fff0f6;
        border-color: #f8bbd0;
        color: #a0527a;
      }
      .cl {
        background: #f3eef9;
        border-color: #ce93d8;
        color: #7b5ea7;
      }
      .cs {
        background: #eef4fd;
        border-color: #90caf9;
        color: #5574a6;
      }
      .cm {
        background: #f0faf5;
        border-color: #a5d6a7;
        color: #3e7d54;
      }
      .cpe {
        background: #fff6ee;
        border-color: #ffcc80;
        color: #9e6b20;
      }
      /* stats */
      .sgrid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }
      .sc {
        background: linear-gradient(135deg, #fff0f6, #f5eef9);
        border: 1px solid rgba(248, 187, 208, 0.38);
        border-radius: 14px;
        padding: 14px 16px;
        position: relative;
        overflow: hidden;
      }
      .sc::before {
        content: "";
        position: absolute;
        top: -16px;
        right: -16px;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        background: rgba(248, 187, 208, 0.18);
      }
      .slb {
        font-size: 11px;
        color: var(--txm);
        font-weight: 600;
        letter-spacing: 0.7px;
        text-transform: uppercase;
        margin-bottom: 6px;
      }
      .sval {
        font-family: "Cormorant Garamond", serif;
        font-size: 28px;
        color: #7b4f72;
        font-weight: 500;
        line-height: 1;
      }
      .ssub {
        font-size: 11px;
        color: var(--txl);
        margin-top: 3px;
      }
      .sico {
        font-size: 20px;
        position: absolute;
        right: 14px;
        top: 13px;
        opacity: 0.45;
      }
      /* streak bar */
      .stbx {
        background: linear-gradient(
          135deg,
          #2d1b45 0%,
          #1a2a50 50%,
          #1f3040 100%
        );
        border-radius: 14px;
        padding: 18px 20px;
        color: #fff;
        position: relative;
        overflow: hidden;
      }
      .stbx::before {
        content: "";
        position: absolute;
        inset: 0;
        background: url("data:image/svg+xml,%3Csvg width='40' height='40' xmlns='http://www.w3.org/2000/svg'%3E%3Ccircle cx='2' cy='2' r='1' fill='rgba(255,255,255,0.035)'/%3E%3C/svg%3E");
      }
      .sti {
        display: flex;
        justify-content: space-around;
        position: relative;
        z-index: 1;
      }
      .sst {
        text-align: center;
      }
      .snum {
        font-family: "Cormorant Garamond", serif;
        font-size: 28px;
        color: #f8bbd0;
        line-height: 1;
      }
      .slbl {
        font-size: 10px;
        color: rgba(255, 255, 255, 0.45);
        margin-top: 4px;
        font-weight: 600;
        letter-spacing: 0.4px;
        text-transform: uppercase;
      }
      .sdiv {
        width: 1px;
        background: rgba(255, 255, 255, 0.1);
        margin: 4px 0;
      }
      /* contribution grid */
      .cgrid {
        display: grid;
        grid-template-columns: repeat(52, 1fr);
        gap: 2px;
      }
      .cc {
        aspect-ratio: 1;
        border-radius: 2px;
        background: rgba(248, 187, 208, 0.1);
      }
      .cc.l1 {
        background: rgba(248, 187, 208, 0.3);
      }
      .cc.l2 {
        background: rgba(248, 187, 208, 0.55);
      }
      .cc.l3 {
        background: rgba(244, 143, 177, 0.7);
      }
      .cc.l4 {
        background: #f48fb1;
      }
      /* now playing */
      .np {
        display: flex;
        align-items: center;
        gap: 16px;
      }
      .aa {
        width: 74px;
        height: 74px;
        border-radius: 13px;
        flex-shrink: 0;
        background: linear-gradient(135deg, #2a1b3d, #4a2560, #1b2d5c);
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        overflow: hidden;
        box-shadow: 0 6px 18px rgba(42, 27, 61, 0.35);
      }
      .aam {
        position: absolute;
        width: 28px;
        height: 28px;
        border-radius: 50%;
        background: radial-gradient(
          circle at 35% 35%,
          #ffe8b0,
          #e8c85a 60%,
          #b8943a
        );
        top: 10px;
        right: 10px;
        box-shadow: 0 0 10px rgba(255, 230, 100, 0.5);
      }
      .aas {
        position: absolute;
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background: #2a1b3d;
        top: 10px;
        right: 19px;
        opacity: 0.84;
      }
      .aav {
        position: absolute;
        bottom: 4px;
        left: 50%;
        transform: translateX(-50%);
        font-size: 22px;
        filter: brightness(0) invert(0.9);
        opacity: 0.68;
      }
      .ti2 {
        flex: 1;
        min-width: 0;
      }
      .ttl {
        font-family: "Cormorant Garamond", serif;
        font-size: 18px;
        font-weight: 500;
        color: #4a2560;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
      .tar {
        font-size: 12px;
        color: var(--txm);
        margin: 3px 0 9px;
      }
      .tbw {
        height: 4px;
        background: rgba(248, 187, 208, 0.28);
        border-radius: 100px;
        overflow: hidden;
      }
      .tbf {
        height: 100%;
        width: 62%;
        background: linear-gradient(90deg, #f48fb1, #ce93d8);
        border-radius: 100px;
        position: relative;
        animation: pp 60s linear forwards;
      }
      @keyframes pp {
        from {
          width: 62%;
        }
        to {
          width: 100%;
        }
      }
      .tbf::after {
        content: "";
        position: absolute;
        right: 0;
        top: 50%;
        transform: translateY(-50%);
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: #ce93d8;
        box-shadow: 0 0 5px rgba(206, 147, 216, 0.6);
      }
      .ttm {
        display: flex;
        justify-content: space-between;
        font-size: 10.5px;
        color: var(--txl);
        margin-top: 5px;
      }
      /* playing indicator */
      .ptag {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: 11.5px;
        color: var(--ac);
        font-weight: 600;
      }
      .pbars {
        display: flex;
        gap: 2px;
        align-items: flex-end;
        height: 12px;
      }
      .pbars span {
        display: block;
        width: 3px;
        background: var(--ac);
        border-radius: 1px;
        animation: eq 0.7s ease-in-out infinite alternate;
      }
      .pbars span:nth-child(1) {
        height: 5px;
        animation-delay: 0s;
      }
      .pbars span:nth-child(2) {
        height: 10px;
        animation-delay: 0.2s;
      }
      .pbars span:nth-child(3) {
        height: 7px;
        animation-delay: 0.1s;
      }
      .pbars span:nth-child(4) {
        height: 12px;
        animation-delay: 0.3s;
      }
      @keyframes eq {
        from {
          transform: scaleY(0.4);
        }
        to {
          transform: scaleY(1);
        }
      }
      /* divider */
      .dvd {
        display: flex;
        align-items: center;
        gap: 10px;
        color: var(--txl);
        font-size: 18px;
      }
      .dvd::before,
      .dvd::after {
        content: "";
        flex: 1;
        height: 1px;
        background: linear-gradient(
          90deg,
          transparent,
          rgba(248, 187, 208, 0.5),
          transparent
        );
      }
      /* socials */
      .srow {
        display: flex;
        justify-content: center;
        gap: 10px;
        flex-wrap: wrap;
      }
      .sbtn {
        display: inline-flex;
        align-items: center;
        gap: 7px;
        padding: 9px 18px;
        border-radius: 100px;
        font-size: 13px;
        font-weight: 700;
        border: 1px solid;
        text-decoration: none;
        transition:
          transform 0.18s,
          box-shadow 0.18s;
        font-family: "Nunito", sans-serif;
      }
      .sbtn:hover {
        transform: translateY(-3px);
        box-shadow: 0 6px 18px rgba(173, 127, 168, 0.24);
      }
      .bg {
        background: #fff0f6;
        border-color: #f8bbd0;
        color: #a0527a;
      }
      .bi {
        background: #f3eef9;
        border-color: #ce93d8;
        color: #7b5ea7;
      }
      /* footer */
      .ftr {
        text-align: center;
        padding: 26px 24px 36px;
        border-top: 1px solid var(--br);
        color: var(--txl);
        font-size: 12.5px;
        background: linear-gradient(
          180deg,
          transparent,
          rgba(248, 187, 208, 0.07)
        );
      }
      .fq {
        font-family: "Cormorant Garamond", serif;
        font-style: italic;
        font-size: 16px;
        color: var(--ac);
        margin-bottom: 8px;
        opacity: 0.88;
      }
      /* responsive */
      @media (max-width: 520px) {
        .hdr h1 {
          font-size: 30px;
        }
        .sgrid {
          grid-template-columns: 1fr;
        }
        .erow {
          gap: 9px;
        }
        .eorb {
          width: 32px;
          height: 32px;
          font-size: 14px;
        }
        .cgrid {
          grid-template-columns: repeat(26, 1fr);
        }
      }
    </style>
  </head>
  <body>
    <!-- HEADER -->
    <header class="hdr">
      <!-- petals -->
      <div
        class="petal"
        style="
          width: 14px;
          height: 14px;
          background: #f8bbd0;
          left: 7%;
          top: 35%;
          animation-duration: 6s;
          animation-delay: -2s;
          opacity: 0.22;
        "
      ></div>
      <div
        class="petal"
        style="
          width: 10px;
          height: 10px;
          background: #ce93d8;
          left: 23%;
          top: 55%;
          animation-duration: 8s;
          animation-delay: -4s;
          opacity: 0.2;
        "
      ></div>
      <div
        class="petal"
        style="
          width: 16px;
          height: 16px;
          background: #f8bbd0;
          left: 67%;
          top: 20%;
          animation-duration: 7s;
          animation-delay: -1s;
          opacity: 0.22;
        "
      ></div>
      <div
        class="petal"
        style="
          width: 9px;
          height: 9px;
          background: #b0c4f0;
          right: 10%;
          top: 60%;
          animation-duration: 9s;
          animation-delay: -3s;
          opacity: 0.2;
        "
      ></div>
      <div
        class="petal"
        style="
          width: 12px;
          height: 12px;
          background: #ce93d8;
          right: 27%;
          top: 10%;
          animation-duration: 5.5s;
          animation-delay: -5s;
          opacity: 0.2;
        "
      ></div>
      <div
        class="petal"
        style="
          width: 8px;
          height: 8px;
          background: #f8bbd0;
          left: 44%;
          top: 8%;
          animation-duration: 7.5s;
          animation-delay: -2.5s;
          opacity: 0.18;
        "
      ></div>
      <div class="hdr-in">
        <!-- Genshin ornament -->
        <div class="orn">
          <svg
            viewBox="0 0 60 60"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="30" cy="30" r="12" stroke="#F8BBD0" stroke-width="1" />
            <circle
              cx="30"
              cy="30"
              r="18"
              stroke="#CE93D8"
              stroke-width="0.5"
              stroke-dasharray="3 4"
            />
            <circle cx="30" cy="30" r="5" fill="#F8BBD0" opacity=".7" />
            <line
              x1="30"
              y1="8"
              x2="30"
              y2="14"
              stroke="#F8BBD0"
              stroke-width="1.5"
              stroke-linecap="round"
            />
            <line
              x1="30"
              y1="46"
              x2="30"
              y2="52"
              stroke="#F8BBD0"
              stroke-width="1.5"
              stroke-linecap="round"
            />
            <line
              x1="8"
              y1="30"
              x2="14"
              y2="30"
              stroke="#F8BBD0"
              stroke-width="1.5"
              stroke-linecap="round"
            />
            <line
              x1="46"
              y1="30"
              x2="52"
              y2="30"
              stroke="#F8BBD0"
              stroke-width="1.5"
              stroke-linecap="round"
            />
            <circle cx="30" cy="8" r="2" fill="#CE93D8" />
            <circle cx="30" cy="52" r="2" fill="#CE93D8" />
            <circle cx="8" cy="30" r="2" fill="#CE93D8" />
            <circle cx="52" cy="30" r="2" fill="#CE93D8" />
            <circle cx="16.5" cy="16.5" r="1.5" fill="#F8BBD0" opacity=".6" />
            <circle cx="43.5" cy="16.5" r="1.5" fill="#F8BBD0" opacity=".6" />
            <circle cx="16.5" cy="43.5" r="1.5" fill="#F8BBD0" opacity=".6" />
            <circle cx="43.5" cy="43.5" r="1.5" fill="#F8BBD0" opacity=".6" />
          </svg>
        </div>
        <div class="av-ring"><div class="av-in">🌸</div></div>
        <h1>Raey ₊˚⊹♡</h1>
        <p class="sub">
          Frontend developer crafting interfaces that feel soft, clean, and
          alive<br />
          Currently exploring the backend realm one API endpoint at a time ✨
        </p>
        <span class="spill">
          <span class="sdot"></span>
          Open to collab &amp; new adventures
        </span>
        <div class="erow">
          <div class="eorb o-cry" title="Cryo">❄</div>
          <div class="eorb o-ane" title="Anemo">🌿</div>
          <div class="eorb o-hyd" title="Hydro">💧</div>
          <div class="eorb o-pyr" title="Pyro">🔥</div>
          <div class="eorb o-ele" title="Electro">⚡</div>
          <div class="eorb o-geo" title="Geo">🪨</div>
          <div class="eorb o-den" title="Dendro">🍃</div>
        </div>
      </div>
    </header>
    <!-- MAIN -->
    <main class="main">
      <!-- ABOUT -->
      <div class="card">
        <div class="ch">
          <div class="ci" style="background: #fff0f6">🌷</div>
          <span class="ct">About Me</span>
        </div>
        <div class="cb">
          <ul class="alist">
            <li>
              <span class="ab">🎀</span
              ><span
                >Frontend Developer focusing on
                <strong style="color: #a0527a; font-weight: 700">UI/UX</strong>
                — crafting soft, interactive experiences</span
              >
            </li>
            <li>
              <span class="ab">🌸</span
              ><span
                >Love when code meets aesthetics — every pixel should feel
                intentional</span
              >
            </li>
            <li>
              <span class="ab">💻</span
              ><span
                >Currently venturing into backend development — learning one
                endpoint at a time</span
              >
            </li>
            <li>
              <span class="ab">🎮</span
              ><span
                >Genshin Impact traveler and Persona series enjoyer 🌙</span
              >
            </li>
            <li>
              <span class="ab">🎨</span
              ><span
                >Art &amp; projects on Instagram:
                <strong style="color: #7b5ea7; font-weight: 700"
                  >@areuraey</strong
                ></span
              >
            </li>
          </ul>
        </div>
      </div>
      <!-- TECH STACK -->
      <div class="card">
        <div class="ch">
          <div class="ci" style="background: #f3eef9">💫</div>
          <span class="ct">Tech Stack</span>
        </div>
        <div class="cb">
          <div class="tgrid">
            <span class="chip cp">🌐 HTML</span>
            <span class="chip cl">🎨 CSS</span>
            <span class="chip cpe">⚡ JavaScript</span>
            <span class="chip cs">⚛ React</span>
            <span class="chip cm">⚡ Vite</span>
            <span class="chip cs">🌊 Tailwind CSS</span>
            <span class="chip cm">🟢 Node.js</span>
            <span class="chip cl">🖌 Figma</span>
          </div>
        </div>
      </div>
      <!-- GITHUB STATS -->
      <div class="card">
        <div class="ch">
          <div class="ci" style="background: #fff6ee">🍓</div>
          <span class="ct">GitHub Stats</span>
        </div>
        <div
          class="cb"
          style="display: flex; flex-direction: column; gap: 14px"
        >
          <div class="stbx">
            <div class="sti">
              <div class="sst">
                <div class="snum" id="total-commits">127</div>
                <div class="slbl">Total Commits</div>
              </div>
              <div class="sdiv"></div>
              <div class="sst">
                <div class="snum">14</div>
                <div class="slbl">Day Streak 🔥</div>
              </div>
              <div class="sdiv"></div>
              <div class="sst">
                <div class="snum">21</div>
                <div class="slbl">Longest Streak</div>
              </div>
            </div>
          </div>
          <div class="sgrid">
            <div class="sc">
              <div class="slb">Public Repos</div>
              <div class="sval">18</div>
              <div class="ssub">Active projects</div>
              <div class="sico">📁</div>
            </div>
            <div class="sc">
              <div class="slb">Stars Earned</div>
              <div class="sval">42</div>
              <div class="ssub">Across all repos</div>
              <div class="sico">⭐</div>
            </div>
          </div>
          <div>
            <div
              style="
                font-size: 11px;
                color: var(--txm);
                font-weight: 600;
                letter-spacing: 0.5px;
                text-transform: uppercase;
                margin-bottom: 8px;
              "
            >
              Contribution activity — 2024
            </div>
            <div class="cgrid" id="cg"></div>
            <div
              style="
                display: flex;
                align-items: center;
                gap: 5px;
                margin-top: 6px;
                justify-content: flex-end;
              "
            >
              <span style="font-size: 10px; color: var(--txl)">Less</span>
              <div
                style="
                  width: 9px;
                  height: 9px;
                  border-radius: 2px;
                  background: rgba(248, 187, 208, 0.1);
                  border: 1px solid rgba(248, 187, 208, 0.25);
                "
              ></div>
              <div
                style="
                  width: 9px;
                  height: 9px;
                  border-radius: 2px;
                  background: rgba(248, 187, 208, 0.3);
                "
              ></div>
              <div
                style="
                  width: 9px;
                  height: 9px;
                  border-radius: 2px;
                  background: rgba(248, 187, 208, 0.55);
                "
              ></div>
              <div
                style="
                  width: 9px;
                  height: 9px;
                  border-radius: 2px;
                  background: #f48fb1;
                "
              ></div>
              <span style="font-size: 10px; color: var(--txl)">More</span>
            </div>
          </div>
        </div>
      </div>
      <!-- NOW PLAYING -->
      <div class="card">
        <div class="ch">
          <div class="ci" style="background: #2a1b3d; font-size: 14px">🎧</div>
          <span class="ct">Now Playing</span>
          <div class="ptag" style="margin-left: auto">
            <div class="pbars">
              <span></span><span></span><span></span><span></span>
            </div>
            playing
          </div>
        </div>
        <div class="cb">
          <div class="np">
            <div class="aa">
              <div class="aas"></div>
              <div class="aam"></div>
              <div class="aav">🔫</div>
            </div>
            <div class="ti2">
              <div class="ttl">Color Your Night</div>
              <div class="tar">Persona 3 Reload OST · Lyn Inaizumi</div>
              <div class="tbw"><div class="tbf"></div></div>
              <div class="ttm"><span>2:14</span><span>3:36</span></div>
            </div>
          </div>
        </div>
      </div>
      <!-- DIVIDER -->
      <div class="dvd">✦</div>
      <!-- SOCIALS -->
      <div class="srow">
        <a
          class="sbtn bg"
          href="https://github.com/demoonlightt"
          target="_blank"
          rel="noopener"
          >🐙 demoonlightt</a
        >
        <a
          class="sbtn bi"
          href="https://instagram.com/areuraey"
          target="_blank"
          rel="noopener"
          >🌸 @areuraey</a
        >
      </div>
    </main>
    <!-- FOOTER -->
    <footer class="ftr">
      <div class="fq">"Crafting little worlds, one commit at a time ✨"</div>
      <div>made with lots of ♡ · raey · 2025</div>
    </footer>
    <script>
      // contribution heatmap
      const g = document.getElementById("cg");
      const lv = ["", "l1", "l2", "l3", "l4"];
      const wt = [0.45, 0.25, 0.15, 0.1, 0.05];
      for (let i = 0; i < 52 * 7; i++) {
        const r = Math.random();
        let acc = 0,
          l = 0;
        for (let w = 0; w < wt.length; w++) {
          acc += wt[w];
          if (r < acc) {
            l = w;
            break;
          }
        }
        const c = document.createElement("div");
        c.className = "cc " + (lv[l] || "");
        g.appendChild(c);
      }
    </script>
  </body>
</html>
