# Canvas graphic extra content

### 💡 Note on expectations

> ⚠️ *Important note: todo esto es **extra**. NO es obligatorio, y de hecho **no es temario de Ironhack** 
ni está en las learning units, es algo que os doy por si mi experiencia os ayuda en estos temas a aquellos 
que os hace ilu aplicarlo, pero la parte de los estilos, gráficos y flipaduras es siempre algo autodidacta 
y cada estudiante va tan lejos como quiera ir (a mi no me explicaron nada de esto por ejemplo, lo tuve que 
investigar por mi cuenta).  Lo digo porque las horas de ayuda con Marina, Guillem y conmigo deberían ir enfocadas 
a lógica del juego y dudas de programación en sí, pero NO de todo esto que no es un requisito a nivel de proyecto.*


# Adding sound to Canvas 🎶

- Paso 1: guardarse los sonidos .mp3 o .wav en una carpeta del proyecto

> Se pueden encontrar sonidos en webs como [https://mixkit.co/free-sound-effects/game/](https://mixkit.co/free-sound-effects/game/) y se pueden cortar con [https://mp3cut.net/es/](https://mp3cut.net/es/)

- Paso 2: crear una función que se encargue de crear un elemento de HTML que pueda reproducir sonido

```jsx
// file: sound.js

function sound(src) { // Esto es lo mismo que haciendo una clase pero con una función, si queréis podeis copiar directamente esto en un archivo y usarlo
  this.sound = document.createElement("audio");
  this.sound.src = src;
  this.sound.setAttribute("preload", "auto");
  this.sound.setAttribute("controls", "none");
  this.sound.style.display = "none";
  document.body.appendChild(this.sound);
  this.play = function() { // Aquí no podemos poner arrow function porque perdemos el this
    this.sound.play();
  };
  this.stop = function() {
    this.sound.pause();
  };
}
```

- crear un new sound (game.js)

```jsx
this.collisionSound = new sound('./sounds/grow.wav');
```

- Paso 3: aplicar el play donde toque ese efecto

```jsx
this.collisionSound.play();
```

- Link video [10 minutos] ( *acabo de ver que como estoy con los airpods el sonido que hace el juego no se ha grabado, pero bueno, lo hace* ): [https://ironhack.zoom.us/rec/share/5VzXwyQODo8ChTzh6MNMyLiOMzfwQBDvPuzkICrCVgj87E-zdvmndDx-kTBO4wwh.j4nQAIRL_BtbV8cr?startTime=1652350051000](https://ironhack.zoom.us/rec/share/5VzXwyQODo8ChTzh6MNMyLiOMzfwQBDvPuzkICrCVgj87E-zdvmndDx-kTBO4wwh.j4nQAIRL_BtbV8cr?startTime=1652350051000)
- Web de donde me bajo yo el sonido: [https://mixkit.co/free-sound-effects/game/](https://mixkit.co/free-sound-effects/game/)
- Web que uso para cortar el sonido: [https://mp3cut.net/](https://mp3cut.net/)

---

# Using sprite animations

- Link video parte 1 [22 minutos]: [https://ironhack.zoom.us/rec/share/AqvoeFHfpaam8nn_SNAHtO1sf8EISxmXW1qgM1GId4QeM7NdRPw9MfN4rNe_Gvue.B5gwecAC7c2MFzHQ?startTime=1652356418000](https://ironhack.zoom.us/rec/share/AqvoeFHfpaam8nn_SNAHtO1sf8EISxmXW1qgM1GId4QeM7NdRPw9MfN4rNe_Gvue.B5gwecAC7c2MFzHQ?startTime=1652356418000)
- Link video parte 2 [10 minutos]: [https://ironhack.zoom.us/rec/share/83czZFSNwWybFPY79HXxY8BDfDCeHxNlLCffn4m1LcDitKR-3p2p6rDxiuO1YyWo.rQSxvVU5hSslNlkp?startTime=1652357863000](https://ironhack.zoom.us/rec/share/83czZFSNwWybFPY79HXxY8BDfDCeHxNlLCffn4m1LcDitKR-3p2p6rDxiuO1YyWo.rQSxvVU5hSslNlkp?startTime=1652357863000)
- Web donde me descargo los sprites: [https://craftpix.net/freebies/](https://craftpix.net/freebies/)
- Yo compruebo las medidas con Sketch pero es de pago, podéis hacerlo con cualquier programa gratis

---

# Parallax effect

- Link video [35 minutos]: [https://ironhack.zoom.us/rec/share/1JSwnWm7Ama84sjRGByQ81xOT0G7p5DrPQEbFtc0y8WWYnbLMo-7MJzKhDZbupWc.LjdphVX0ocaoQK_k?startTime=1652359742000](https://ironhack.zoom.us/rec/share/1JSwnWm7Ama84sjRGByQ81xOT0G7p5DrPQEbFtc0y8WWYnbLMo-7MJzKhDZbupWc.LjdphVX0ocaoQK_k?startTime=1652359742000)
- Web donde me descargo el fondo: [https://itch.io/game-assets/free/tag-parallax](https://itch.io/game-assets/free/tag-parallax)

---

Repositorio con todo aplicado: https://github.com/alebausa/meatball-dev