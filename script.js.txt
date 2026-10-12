const display = document.getElementById("display");

document.querySelectorAll("button").forEach(btn => {
  btn.addEventListener("click", () => {
    const v = btn.textContent;
    if (v === "C") display.value = "";
    else if (v === "=") {
      try { display.value = eval(display.value); }
      catch { display.value = "Error"; }
    }
    else display.value += v;
  });
});