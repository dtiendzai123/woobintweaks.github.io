border-radius: 20px;
    }

    .slider:before {
      content: "";
      position: absolute;
      height: 12px;
      width: 12px;
      left: 3px;
      bottom: 3px;
      background-color: white;
      border-radius: 50%;
      transition: .4s;
    }

    input:checked + .slider {
      background-color: #2196F3;
    }

    input:checked + .slider:before {
      transform: translateX(18px);
    }

    .alert-box {
      position: fixed;
      top: 30%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 80%;
      max-width: 260px;
      background: white;
      border-radius: 10px;
      padding: 16px;
      text-align: center;
      z-index: 999;
      display: none;
    }

    .alert-box p {
      margin-bottom: 12px;
      color: #333;
      font-weight: bold;
    }

    .alert-box button {
      padding: 8px 16px;
      border: none;
      background: #444;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <!-- LED quanh màn hình -->
  <div class="led-border"></div>
  <div class="led-right"></div>
  <div class="led-bottom"></div>
  <!-- Ẩn panel -->
<div class="toggle-button" onclick="toggleMenu()">
  <img src="undefined - Imgur.jpg" alt="toggle" class="toggle-icon">
</div>

  <!-- Menu bên trái -->
  <div class="menu">
    <div class="menu-item">
      <span>Speed</span>
      <label class="switch">
        <input type="checkbox" onchange="handleToggle(this)">
        <span class="slider"></span>
      </label>
    </div>
    <div class="menu-item">
      <span>Boost Game</span>
      <label class="switch">
        <input type="checkbox" onchange="handleToggle(this)">
        <span class="slider"></span>
      </label>
    </div>
    <div class="menu-item">
      <span>Fix Lag</span>
      <label class="switch">
        <input type="checkbox" onchange="handleToggle(this)">
        <span class="slider"></span>
      </label>
    </div>
      <div class="menu-item">
      <span>dzai s1tg</span>
      <label class="switch">
        <input type="checkbox" onchange="handleToggle(this)">
        <span class="slider"></span>
      </label>
    </div>
    <div class="menu-item">
      <a href="freefireth://">Mở Free Fire</a>
    </div>
    <div class="menu-item">
      <a href="freefiremax://">Mở Free Fire MAX</a>
    </div>
  </div>

  <!-- Cảnh báo -->
  <div id="alertBox" class="alert-box">
    <p id="alertText">Kích hoạt thành công</p>
    <button onclick="closeAlert()">OK</button>
  </div>

  <!-- Âm thanh -->
 <audio autoplay>
        <source src="st.mp3" type="audio/mp3">

  <script>
    function handleToggle(checkbox) {
      const alertText = document.getElementById("alertText");
      const alertBox = document.getElementById("alertBox");
      const audio = document.getElementById("sound");

      if (checkbox.checked) {
        alertText.innerHTML = `Kích hoạt thành công<br>Mua đồ LH:0378813029 `;
      } else {alertText.innerText = "Tắt thành công";
      }

      alertBox.style.display = "block";
      audio.play();
    }

    function closeAlert() {
      document.getElementById("alertBox").style.display = "none";
    }
    function toggleMenu() {
  const menu = document.querySelector('.menu');
  if (menu.style.display === 'none' || !menu.style.display) {
    menu.style.display = 'block';
  } else {
    menu.style.display = 'none';
  }
}
  </script>
</body>
</html>
