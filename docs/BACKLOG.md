
## 29-sep-2026 — Botón "🕓 LATER": compartir la liga en vivo por LaterWhats

- Ya existía todo lo demás: la liga `?v=<código>` abre el visor **sin login**
  (modo `viewer-mode`), con el mapa y el marcador moviéndose por MQTT.
- `index.html` (`shareLater`): abre `latherwhats.vercel.app/?body=…&source=livetrack`
  con el mensaje y la liga ya escritos; el contacto se elige en LaterWhats y se
  manda al momento o se programa.
- **Pendiente / límites:** (1) el código de 6 caracteres viaja por brokers MQTT
  públicos, sin caducidad: quien tenga la liga ve la ubicación mientras se
  comparta; conviene un código más largo y tiempo límite. (2) En iOS el GPS de
  una PWA solo actualiza con la pantalla encendida (hoy usa Wake Lock).
