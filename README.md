<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>이차경 개인 웹페이지</title>
  <!-- 나눔고딕 폰트 -->
  <link href="https://fonts.googleapis.com/css2?family=Nanum+Gothic&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Nanum Gothic', sans-serif;
      color: #333;
      background: linear-gradient(to top, #ff9966, #ff5e62); /* 가을 노을 느낌 */
    }
    header {
      text-align: center;
      padding: 2rem;
      color: white;
    }
    header h1 {
      font-size: 2.5rem;
      margin-bottom: 0.5rem;
    }
    header p {
      font-size: 1.2rem;
    }
    nav {
      text-align: center;
      background: rgba(255,255,255,0.2);
      padding: 1rem;
    }
    nav a {
      margin: 0 1rem;
      text-decoration: none;
      color: white;
      font-weight: bold;
    }
    section {
      max-width: 900px;
      margin: auto;
      background: rgba(255, 200, 150, 0.7); /* 따뜻한 오렌지톤 반투명 */
      border-radius: 10px;
      padding: 2rem;
      margin-top: 2rem;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }
    section h2 {
      color: #2e8b57; /* 초록색 포인트 */
      margin-bottom: 1rem;
    }
    .leaf {
      position: absolute;
      width: 40px;
      height: 40px;
      background: url('https://cdn-icons-png.flaticon.com/512/765/765539.png') no-repeat center/contain;
      animation: fall 10s linear infinite;
    }
    @keyframes fall {
      0% { transform: translateY(-100px) rotate(0deg); opacity: 1; }
      100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
    }
    footer {
      text-align: center;
      padding: 1rem;
      color: white;
      margin-top: 2rem;
    }
    /* 반응형 */
    @media (max-width: 600px) {
      header h1 { font-size: 1.8rem; }
      section { padding: 1rem; }
    }
  </style>
</head>
<body>
  <header>
    <h1>👋 안녕하세요, 이차경입니다</h1>
    <p>한신대학교 AI·SW대학 소속 · 웹프로그래밍 수업용 개인 페이지</p>
  </header>

  <nav>
    <a href="#edu">학력</a>
    <a href="#career">경력</a>
    <a href="#cert">자격</a>
    <a href="#personality">성격</a>
  </nav>

  <section id="edu">
    <h2>🎓 학력</h2>
    <ul>
      <li>한신대학교 AI·SW대학 재학</li>
      <li>웹프로그래밍 및 인공지능 관련 전공</li>
    </ul>
  </section>

  <section id="career">
    <h2>💼 경력</h2>
    <ul>
      <li>웹프로그래밍 프로젝트 참여</li>
      <li>AI 관련 학부 연구 활동</li>
    </ul>
  </section>

  <section id="cert">
    <h2>📜 자격</h2>
    <ul>
      <li>정보처리기사 준비 중</li>
      <li>AI·SW 관련 교내 인증 프로그램 수료</li>
    </ul>
  </section>

  <section id="personality">
    <h2>🌟 성격</h2>
    <p>호기심 많고 성실하며, 새로운 기술을 배우는 것을 즐깁니다. 팀워크를 중시하고 긍정적인 에너지를 전달하는 것을 좋아합니다 😊</p>
  </section>

  <footer>
    <p>© 2026 이차경 · 모든 권리 보유</p>
  </footer>

  <!-- JS로 초록색 나뭇잎 떨어지는 효과 -->
  <script>
    function createLeaf() {
      const leaf = document.createElement('div');
      leaf.className = 'leaf';
      leaf.style.left = Math.random() * window.innerWidth + 'px';
      document.body.appendChild(leaf);
      setTimeout(() => leaf.remove(), 10000);
    }
    setInterval(createLeaf, 1500);
  </script>
</body>
</html>
