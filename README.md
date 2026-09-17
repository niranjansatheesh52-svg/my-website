<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Just Vanda Thingz!!</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      min-height: 100vh;
      background: #yellow;
      color: red;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    .box {
      text-align: center;
      padding: 40px;
    }

    h1 {
      font-size: 42px;
      margin-bottom: 15px;
    }

    p {
      color: #bbb;
      margin-bottom: 30px;
    }

    button {
      border: none;
      padding: 16px 35px;
      border-radius: 12px;
      background: red;
      color: yellow;
      font-size: 18px;
      font-weight: italic;
      cursor: pointer;
    }

    button:hover {
      transform: scale(1.08);
    }

    #prank {
      position: fixed;
      inset: 0;
      background: #111;
      display: none;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    #prank.show {
      display: flex;
    }

    .message {
      padding: 30px;
    }

    .emoji {
      font-size: 100px;
      animation: bounce 0.8s infinite alternate;
    }

    .message h2 {
      font-size: 48px;
      margin: 20px 0;
    }

    .message p {
      font-size: 20px;
    }

    .back {
      margin-top: 20px;
    }

    @keyframes bounce {
      from {
        transform: translateY(0);
      }

      to {
        transform: translateY(-20px);
      }
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>Vanda Leaked 👀</h1>

    <p>Rare items only...</p>

    <button onclick="prank()">EXPLORE</button>
  </div>


  <div id="prank">

    <div class="message">

      <div class="emoji">VANDAxHUB</div>

      <h2>COMING SOON!</h2>

      <p>
        <br>
        If you need now contact on<br>
         7558874227, 9744045641<br>
        VC Available ait 9:00 - 12:30<br>
        DM for Pre-booking <br>
        <a href ="https://www.instagram.com/unfav.adhyee?utm_source=ig_web_button_share_sheet&stkn=ZDNlZDc0MzIxNw=="> PRE-BOOK HERE</a>
      </p>

      <button class="back" onclick="goBack()">
        Go Back
      </button>

    </div>

  </div>


  <script>

    function playSound() {

      const audio = new (
        window.AudioContext ||
        window.webkitAudioContext
      )();

      const oscillator = audio.createOscillator();

      const gain = audio.createGain();

      oscillator.type = "sawtooth";

      oscillator.frequency.setValueAtTime(
        500,
        audio.currentTime
      );

      oscillator.frequency.exponentialRampToValueAtTime(
        100,
        audio.currentTime + 0.5
      );

      gain.gain.setValueAtTime(
        0.3,
        audio.currentTime
      );

      gain.gain.exponentialRampToValueAtTime(
        0.01,
        audio.currentTime + 0.5
      );

      oscillator.connect(gain);

      gain.connect(audio.destination);

      oscillator.start();

      oscillator.stop(
        audio.currentTime + 0.5
      );
    }


    function prank() {

      playSound();

      document
        .getElementById("prank")
        .classList.add("show");

    }


    function goBack() {

      document
        .getElementById("prank")
        .classList.remove("show");

    }

  </script>

</body>
</html>
