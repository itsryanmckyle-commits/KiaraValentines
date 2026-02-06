<script>
  let taskCompleted = false;
  let noClickedOnce = false;

  function sayYes() {
    if (!taskCompleted) {
      document.querySelector(".card").innerHTML = `
        <h1>ryanmn</h1>
        <h2>Task Time 😏</h2>
        <p>Before you can say YES...</p>
        <p><strong>Task:</strong> Send me a kiss emoji 😘 on WhatsApp 💬</p>
        <button class="yes" onclick="completeTask()">I did it 😘</button>
      `;
    } else {
      showSuccess();
    }
  }

  function completeTask() {
    taskCompleted = true;
    showSuccess();
  }

  function showSuccess() {
    document.querySelector(".card").innerHTML = `
      <h1>ryanmn</h1>
      <h2>Yay!!! 🥰💖</h2>
      <img src="https://media.tenor.com/gUiu1zyxfzYAAAAi/bear-kiss-bear-kisses.gif" />
      <p>You’re officially my Valentine 💝</p>
    `;
  }

  function handleNoClick() {
    const msg = document.getElementById("noMessage");
    if (!noClickedOnce) {
      noClickedOnce = true;
      msg.textContent = "Kiara, are you sure? 🥺💔";
    }
    moveNo();
  }

  function moveNo() {
    const noBtn = document.getElementById("noBtn");
    if (!noBtn) return;

    const x = Math.random() * 250 - 125;
    const y = Math.random() * 250 - 125;

    noBtn.style.position = "relative";
    noBtn.style.transform = translate(${x}px, ${y}px);
  }
</script>
