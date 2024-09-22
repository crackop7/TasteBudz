<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Taste Budz - Home</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      overflow-x: hidden;
      color: #333;
      background-color: #fff8e1;
      background-image: url('https://www.example.com/food-doodle-background.jpg'); /* Replace with a doodle image URL */
      background-repeat: no-repeat;
      background-position: center;
      background-size: cover;
    }

    .background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #ff9800, #ffc107, #ff5722);
      background-size: 300% 300%;
      animation: gradientAnimation 20s ease infinite;
      z-index: -1;
    }

    @keyframes gradientAnimation {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    header {
      background: rgba(255, 152, 0, 0.9);
      color: #fff;
      padding: 20px 0;
      text-align: center;
      position: relative;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    }

    header h1 {
      margin: 0;
      font-size: 2.5em;
    }

    header nav {
      position: absolute;
      top: 20px;
      right: 20px;
    }

    header nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-size: 1.2em;
      padding: 5px 10px;
      border-radius: 5px;
      transition: background 0.3s ease;
    }

    header nav a:hover {
      background: rgba(255, 255, 255, 0.2);
    }

    .hero {
      background: url('https://www.example.com/hero-image.jpg') no-repeat center center/cover;
      height: 350px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      text-align: center;
      position: relative;
    }

    .hero h2 {
      font-size: 3.5em;
      margin: 0;
    }

    .cta-button {
      background: #ffeb3b;
      color: #ff9800;
      border: none;
      padding: 15px 40px;
      font-size: 1.3em;
      cursor: pointer;
      border-radius: 30px;
      margin-top: 20px;
      transition: background 0.3s ease;
    }

    .cta-button:hover {
      background: #ffc107;
    }

    .section {
      padding: 50px 20px;
      text-align: center;
      background: #fff;
    }

    .section h2 {
      font-size: 2.5em;
      margin-bottom: 5px;
      color: #ff5722;
    }

    .section p {
      font-size: 1.2em;
      margin: 0 auto;
      max-width: 800px;
      margin-bottom: 20px;
      color: #666;
      position: relative;
    }

    .tiffin-menu {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }

    .tiffin-item {
      background: #fff;
      border: 2px solid #ff9800;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
      max-width: 300px;
      text-align: center;
      transition: transform 0.3s ease;
    }

    .tiffin-item img {
      width: 100%;
      height: auto;
      display: block;
    }

    .tiffin-item h3 {
      margin: 10px 0;
      font-size: 1.7em;
      color: #ff5722;
    }

    .tiffin-item p {
      margin: 0;
      font-size: 1.2em;
      padding: 0 10px;
      color: #666;
    }

    .tiffin-item:hover {
      transform: scale(1.05);
    }

    footer {
      background: rgba(255, 152, 0, 0.9);
      color: #fff;
      padding: 20px;
      text-align: center;
      position: relative;
    }

    footer p {
      margin: 0;
      font-size: 1em;
    }

    footer a {
      color: #fff;
      text-decoration: underline;
    }

    .scroll-to-top {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #ff5722;
      color: #fff;
      border: none;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.5em;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      transition: background 0.3s ease;
    }

    .scroll-to-top:hover {
      background: #e64a19;
    }

    /* Chatbox Styles */
    .chatbox {
      position: fixed;
      bottom: 100px;
      right: 20px;
      width: 300px;
      height: 400px;
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      overflow: hidden;
      display: none;
      flex-direction: column;
      z-index: 1000;
    }

    .chatbox-header {
      background: #ff5722;
      color: #fff;
      padding: 15px;
      text-align: center;
      font-size: 1.3em;
      cursor: pointer;
    }

    .chatbox-messages {
      flex: 1;
      padding: 10px;
      overflow-y: auto;
      border-bottom: 1px solid #ddd;
    }

    .chatbox-input {
      padding: 10px;
      display: flex;
      border-top: 1px solid #ddd;
    }

    .chatbox-input input {
      flex: 1;
      padding: 10px;
      border: none;
      border-radius: 5px;
      margin-right: 10px;
      outline: none;
    }

    .chatbox-input button {
      background: #ff5722;
      color: #fff;
      border: none;
      padding: 10px;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .chatbox-input button:hover {
      background: #e64a19;
    }

    /* Chatbox Toggle Button */
    .chatbox-toggle {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #ff5722;
      color: #fff;
      border: none;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2em;
      cursor: pointer;
      z-index: 999;
    }

    .chatbox-toggle:hover {
      background: #e64a19;
    }

    /* Message styles */
    .chatbox-messages .message {
      display: flex;
      margin-bottom: 10px;
    }

    .chatbox-messages .user-message {
      justify-content: flex-end;
    }

    .chatbox-messages .bot-message {
      justify-content: flex-start;
    }

    .chatbox-messages .message div {
      max-width: 70%;
      padding: 10px;
      border-radius: 15px;
      color: #fff;
      font-size: 1em;
    }

    .chatbox-messages .user-message div {
      background-color: #ff9800;
      border-top-right-radius: 0;
    }

    .chatbox-messages .bot-message div {
      background-color: #e64a19;
      border-top-left-radius: 0;
    }
  </style>
</head>
<body>

<div class="background"></div>

<header>
  <h1>Taste Budz</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#menu">Menu</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero">
  <div>
    <h2>Delicious Tiffins Delivered To Your Door</h2>
    <button class="cta-button">Order Now</button>
  </div>
</section>

<section class="section" id="menu">
  <h2>Our Menu</h2>
  <p>Discover a variety of delicious, homemade tiffins delivered with love.</p>

  <div class="tiffin-menu">
    <div class="tiffin-item">
      <img src="file:///D:/swayam/swayam/ZHFLWK75OZB4TJM45XR627PU5I.avif" alt="Regular Tiffin">
      <h3>Regular Tiffin</h3>
      <p>Freshly cooked with love, just like home.</p>
    </div>

    <div class="tiffin-item">
      <img src="file:///D:/swayam/swayam/Leonardo_Phoenix_Create_a_vibrant_stilllife_image_featuring_a_2.jpg" alt="Jain Tiffin">
      <h3>Jain Tiffin</h3>
      <p>Pure, simple, and absolutely delicious.</p>
    </div>

    <div class="tiffin-item">
      <img src="file:///D:/swayam/swayam/Leonardo_Phoenix_A_vibrant_and_mouthwatering_Americanstyle_veg_3.jpg" alt="Special Tiffin">
      <h3>Healthy Tiffin</h3>
      <p>For those days when you need something extra.</p>
    </div>
  </div>
</section>

<footer>
  <p>&copy; 2024 Taste Budz. All rights reserved.</p>
  <p>Contact us: +91 8888994994 | <a href="mailto:swayamsancheti45@gmail.com">swayamsancheti45@gmail.com</a> </p>
</footer>

<button class="scroll-to-top" onclick="scrollToTop()">&#8679;</button>

<!-- Chatbox -->
<div class="chatbox" id="chatbox">
  <div class="chatbox-header" onclick="toggleChatbox()">Chat with us!</div>
  <div class="chatbox-messages" id="chatbox-messages"></div>
  <div class="chatbox-input">
    <input type="text" id="chat-input" placeholder="Type your message...">
    <button onclick="sendMessage()">Send</button>
  </div>
</div>

<!-- Chatbox Toggle Button -->
<button class="chatbox-toggle" onclick="toggleChatbox()">&#9993;</button>

<script>
  function toggleChatbox() {
    const chatbox = document.getElementById('chatbox');
    chatbox.style.display = chatbox.style.display === 'none' || chatbox.style.display === '' ? 'flex' : 'none';
  }

  function scrollToTop() {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  function sendMessage() {
    const chatInput = document.getElementById('chat-input');
    const chatMessages = document.getElementById('chatbox-messages');
    const message = chatInput.value;

    if (message.trim() !== '') {
      // Create user message
      const userMessage = document.createElement('div');
      userMessage.classList.add('message', 'user-message');
      const userMessageContent = document.createElement('div');
      userMessageContent.textContent = `You: ${message}`;
      userMessage.appendChild(userMessageContent);
      chatMessages.appendChild(userMessage);

      chatInput.value = '';

      // Auto-scroll to the bottom of the chatbox
      chatMessages.scrollTop = chatMessages.scrollHeight;

      // Simulate bot reply after 1 second
      setTimeout(() => {
        const botMessage = document.createElement('div');
        botMessage.classList.add('message', 'bot-message');
        const botMessageContent = document.createElement('div');
        botMessageContent.textContent = 'Bot: Thank you for your message! We will get back to you soon.';
        botMessage.appendChild(botMessageContent);
        chatMessages.appendChild(botMessage);

        // Auto-scroll to the bottom of the chatbox after bot message
        chatMessages.scrollTop = chatMessages.scrollHeight;
      }, 1000);
    }
  }
</script>

</body>
</html>
