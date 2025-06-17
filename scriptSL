(function() {
  function digitarTextoGradualmente(el, texto, delay = 100) {
    let i = 0;
    const intervalo = setInterval(() => {
      if (i < texto.length) {
        el.value += texto[i];
        el.dispatchEvent(new Event("input"));
        i++;
      } else {
        clearInterval(intervalo);
        console.log("✅ Texto preenchido.");
      }
    }, delay + Math.random() * 50);
  }

  const campo = document.querySelector("textarea, input[type='text']");
  const resposta = "Minha resposta automática.";

  if (campo) {
    digitarTextoGradualmente(campo, resposta, 120);

    setTimeout(() => {
      const botao = [...document.querySelectorAll("button")]
        .find(b => b.innerText.includes("Próxima") || b.innerText.includes("Enviar"));
      if (botao) {
        botao.click();
        console.log("✅ Botão clicado.");
      }
    }, 4000 + Math.random() * 3000);
  } else {
    console.log("❌ Campo de resposta não encontrado.");
  }
})();
