# Cuestionario-ucl<!DOCTYPE html>

<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cuestionario UCL – Béisbol Dominicano</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:ital@1&display=swap" rel="stylesheet">
<style>
  :root {
    --red: #C8102E;
    --navy: #002D62;
    --cream: #F5F0E8;
    --gold: #D4A017;
    --dark: #0D0D0D;
    --mid: #2A2A2A;
    --light: #F9F6F0;
    --border: #D6CEBC;
    --success: #1A7A4A;
    --radius: 4px;
  }

- { box-sizing: border-box; margin: 0; padding: 0; }

body {
background-color: var(–cream);
font-family: ‘DM Sans’, sans-serif;
color: var(–dark);
min-height: 100vh;
}

/* HEADER */
.header {
background: var(–navy);
padding: 0;
position: relative;
overflow: hidden;
}

.header-stripe {
height: 6px;
background: repeating-linear-gradient(90deg, var(–red) 0, var(–red) 33%, var(–navy) 33%, var(–navy) 34%, var(–gold) 34%, var(–gold) 67%, var(–navy) 67%, var(–navy) 68%, var(–cream) 68%, var(–cream) 100%);
}

.header-inner {
padding: 36px 48px 32px;
display: flex;
align-items: flex-start;
gap: 32px;
}

.header-badge {
background: var(–red);
color: white;
font-family: ‘Bebas Neue’, sans-serif;
font-size: 11px;
letter-spacing: 3px;
padding: 6px 14px;
border-radius: 2px;
white-space: nowrap;
margin-top: 6px;
flex-shrink: 0;
writing-mode: vertical-rl;
transform: rotate(180deg);
height: fit-content;
}

.header-text h1 {
font-family: ‘Bebas Neue’, sans-serif;
font-size: clamp(28px, 5vw, 52px);
color: white;
line-height: 1;
letter-spacing: 1px;
}

.header-text h1 span { color: var(–gold); }

.header-text p {
color: rgba(255,255,255,0.6);
font-size: 13px;
font-weight: 300;
margin-top: 10px;
letter-spacing: 0.3px;
max-width: 520px;
line-height: 1.6;
}

.unibe-tag {
font-family: ‘Bebas Neue’, sans-serif;
font-size: 10px;
letter-spacing: 4px;
color: var(–gold);
margin-bottom: 10px;
display: block;
}

/* PROGRESS */
.progress-bar-wrap {
background: var(–navy);
padding: 0 48px 28px;
}

.progress-meta {
display: flex;
justify-content: space-between;
font-size: 11px;
color: rgba(255,255,255,0.45);
letter-spacing: 1px;
text-transform: uppercase;
margin-bottom: 8px;
}

.progress-track {
height: 3px;
background: rgba(255,255,255,0.12);
border-radius: 99px;
overflow: hidden;
}

.progress-fill {
height: 100%;
background: linear-gradient(90deg, var(–red), var(–gold));
border-radius: 99px;
transition: width 0.5s cubic-bezier(0.4, 0, 0.2, 1);
width: 0%;
}

/* MAIN */
.main {
max-width: 780px;
margin: 0 auto;
padding: 48px 24px 80px;
}

/* SECTION */
.section {
margin-bottom: 56px;
animation: fadeUp 0.4s ease both;
}

@keyframes fadeUp {
from { opacity: 0; transform: translateY(16px); }
to { opacity: 1; transform: translateY(0); }
}

.section-header {
display: flex;
align-items: center;
gap: 16px;
margin-bottom: 28px;
}

.section-num {
font-family: ‘Bebas Neue’, sans-serif;
font-size: 42px;
color: var(–border);
line-height: 1;
}

.section-label {
border-left: 3px solid var(–red);
padding-left: 14px;
}

.section-label h2 {
font-family: ‘Bebas Neue’, sans-serif;
font-size: 20px;
letter-spacing: 1.5px;
color: var(–navy);
}

.section-label p {
font-size: 12px;
color: #888;
margin-top: 2px;
font-weight: 300;
}

/* FIELD */
.field {
margin-bottom: 24px;
}

.field label {
display: block;
font-size: 13px;
font-weight: 600;
color: var(–mid);
margin-bottom: 8px;
letter-spacing: 0.2px;
}

.field label .req { color: var(–red); margin-left: 3px; }

.field-hint {
font-size: 11px;
color: #999;
font-weight: 300;
margin-top: -4px;
margin-bottom: 8px;
font-style: italic;
}

.field input[type=“number”],
.field input[type=“text”],
.field select,
.field textarea {
width: 100%;
background: white;
border: 1.5px solid var(–border);
border-radius: var(–radius);
padding: 12px 14px;
font-family: ‘DM Sans’, sans-serif;
font-size: 14px;
color: var(–dark);
transition: border-color 0.2s, box-shadow 0.2s;
appearance: none;
-webkit-appearance: none;
}

.field select {
background-image: url(“data:image/svg+xml,%3Csvg xmlns=‘http://www.w3.org/2000/svg’ width=‘12’ height=‘8’%3E%3Cpath d=‘M1 1l5 5 5-5’ stroke=’%23999’ stroke-width=‘1.5’ fill=‘none’ stroke-linecap=‘round’/%3E%3C/svg%3E”);
background-repeat: no-repeat;
background-position: right 14px center;
padding-right: 38px;
}

.field input:focus,
.field select:focus,
.field textarea:focus {
outline: none;
border-color: var(–navy);
box-shadow: 0 0 0 3px rgba(0,45,98,0.08);
}

.field textarea { resize: vertical; min-height: 90px; }

/* RADIO / CHECK GRID */
.options-grid {
display: grid;
gap: 10px;
}

.options-grid.cols-2 { grid-template-columns: 1fr 1fr; }
.options-grid.cols-3 { grid-template-columns: 1fr 1fr 1fr; }

@media (max-width: 540px) {
.options-grid.cols-2,
.options-grid.cols-3 { grid-template-columns: 1fr; }
}

.opt {
position: relative;
}

.opt input { position: absolute; opacity: 0; width: 0; height: 0; }

.opt label {
display: flex;
align-items: center;
gap: 10px;
background: white;
border: 1.5px solid var(–border);
border-radius: var(–radius);
padding: 12px 16px;
cursor: pointer;
font-size: 13.5px;
font-weight: 400;
color: var(–mid);
transition: border-color 0.15s, background 0.15s, color 0.15s;
margin-bottom: 0;
letter-spacing: 0;
}

.opt label::before {
content: ‘’;
width: 16px;
height: 16px;
border: 2px solid var(–border);
border-radius: 50%;
flex-shrink: 0;
transition: border-color 0.15s, background 0.15s;
}

.opt.check label::before { border-radius: 3px; }

.opt input:checked + label {
border-color: var(–navy);
background: #F0F4FA;
color: var(–navy);
font-weight: 600;
}

.opt input:checked + label::before {
background: var(–navy);
border-color: var(–navy);
box-shadow: inset 0 0 0 3px white;
}

/* SCALE */
.scale-wrap { display: flex; gap: 8px; }

.scale-item { flex: 1; text-align: center; }

.scale-item input { position: absolute; opacity: 0; }

.scale-item label {
display: flex;
flex-direction: column;
align-items: center;
gap: 6px;
cursor: pointer;
padding: 10px 4px;
border-radius: var(–radius);
border: 1.5px solid var(–border);
background: white;
font-size: 13px;
font-weight: 500;
color: #888;
transition: all 0.15s;
margin-bottom: 0;
letter-spacing: 0;
}

.scale-item label span {
font-family: ‘Bebas Neue’, sans-serif;
font-size: 20px;
color: var(–mid);
}

.scale-item input:checked + label {
border-color: var(–red);
background: #FDF0F2;
color: var(–red);
}

.scale-item input:checked + label span { color: var(–red); }

.scale-labels {
display: flex;
justify-content: space-between;
font-size: 10px;
color: #bbb;
letter-spacing: 0.5px;
margin-top: 6px;
text-transform: uppercase;
}

/* DIVIDER */
.divider {
height: 1px;
background: var(–border);
margin: 48px 0;
position: relative;
}

.divider::after {
content: ‘◆’;
position: absolute;
left: 50%;
top: 50%;
transform: translate(-50%, -50%);
background: var(–cream);
padding: 0 12px;
color: var(–border);
font-size: 10px;
}

/* ROW */
.field-row {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 16px;
}

@media (max-width: 540px) { .field-row { grid-template-columns: 1fr; } }

/* ALERT BOX */
.alert-box {
background: #FFF8E1;
border: 1.5px solid var(–gold);
border-radius: var(–radius);
padding: 14px 18px;
font-size: 12.5px;
color: #7A5C00;
margin-bottom: 24px;
line-height: 1.6;
}

.alert-box strong { font-weight: 600; }

/* CONDITIONAL */
.conditional {
display: none;
border-left: 3px solid var(–gold);
padding-left: 20px;
margin-top: 16px;
}

.conditional.visible { display: block; }

/* SUBMIT */
.submit-zone {
margin-top: 56px;
text-align: center;
padding: 40px;
background: white;
border: 1.5px solid var(–border);
border-radius: var(–radius);
}

.submit-zone p {
font-size: 12px;
color: #999;
margin-bottom: 24px;
line-height: 1.7;
}

.btn-submit {
background: var(–navy);
color: white;
border: none;
padding: 16px 56px;
font-family: ‘Bebas Neue’, sans-serif;
font-size: 18px;
letter-spacing: 3px;
border-radius: var(–radius);
cursor: pointer;
transition: background 0.2s, transform 0.1s;
}

.btn-submit:hover { background: var(–red); }
.btn-submit:active { transform: scale(0.98); }

/* SUCCESS */
.success-screen {
display: none;
text-align: center;
padding: 80px 40px;
}

.success-screen.visible { display: block; }

.success-icon {
width: 72px;
height: 72px;
background: var(–success);
border-radius: 50%;
display: flex;
align-items: center;
justify-content: center;
margin: 0 auto 24px;
font-size: 32px;
}

.success-screen h2 {
font-family: ‘Bebas Neue’, sans-serif;
font-size: 36px;
letter-spacing: 2px;
color: var(–navy);
margin-bottom: 12px;
}

.success-screen p { color: #888; font-size: 14px; }

.form-content {}

/* FOOTER */
.footer {
background: var(–navy);
padding: 20px 48px;
display: flex;
justify-content: space-between;
align-items: center;
}

.footer p {
font-size: 11px;
color: rgba(255,255,255,0.35);
letter-spacing: 0.5px;
}

.footer-dots {
display: flex;
gap: 6px;
}

.footer-dots span {
width: 8px;
height: 8px;
border-radius: 50%;
}

.dot-red { background: var(–red); }
.dot-gold { background: var(–gold); }
.dot-light { background: rgba(255,255,255,0.2); }

/* VALIDATION */
.field.error input,
.field.error select,
.field.error textarea {
border-color: var(–red);
}

.field .error-msg {
display: none;
font-size: 11px;
color: var(–red);
margin-top: 5px;
}

.field.error .error-msg { display: block; }
</style>

</head>
<body>

<div class="header">
  <div class="header-stripe"></div>
  <div class="header-inner">
    <div class="header-badge">UNIBE</div>
    <div class="header-text">
      <span class="unibe-tag">Universidad Iberoamericana · Medicina Deportiva</span>
      <h1>PREVALENCIA DE <span>CIRUGÍA TOMMY JOHN</span><br>Y FACTORES DE RIESGO</h1>
      <p>Cuestionario para jugadores dominicanos de béisbol entre 17–21 años. La información es confidencial y de uso académico exclusivo.</p>
    </div>
  </div>
</div>

<div class="progress-bar-wrap">
  <div class="progress-meta">
    <span id="progressLabel">Sección 1 de 5</span>
    <span id="progressPct">0%</span>
  </div>
  <div class="progress-track">
    <div class="progress-fill" id="progressFill"></div>
  </div>
</div>

<div class="main">

  <div class="form-content" id="formContent">
  <form id="mainForm" novalidate>

  <!-- ═══════════════════════════════════════════
       SECCIÓN 1 · DATOS SOCIODEMOGRÁFICOS
  ═══════════════════════════════════════════ -->

  <div class="section" id="sec1">
    <div class="section-header">
      <div class="section-num">01</div>
      <div class="section-label">
        <h2>Datos Sociodemográficos</h2>
        <p>Información básica del participante</p>
      </div>
    </div>

```
<div class="field-row">
  <div class="field" id="f-edad">
    <label>Edad <span class="req">*</span></label>
    <input type="number" name="edad" min="17" max="21" placeholder="17–21 años" required>
    <span class="error-msg">Ingresa una edad entre 17 y 21 años.</span>
  </div>

  <div class="field" id="f-provincia">
    <label>Provincia de origen <span class="req">*</span></label>
    <select name="provincia" required>
      <option value="">Seleccionar…</option>
      <option>Santo Domingo</option>
      <option>San Cristóbal</option>
      <option>San Pedro de Macorís</option>
      <option>La Romana</option>
      <option>Santiago</option>
      <option>La Vega</option>
      <option>Azua</option>
      <option>Barahona</option>
      <option>Otra</option>
    </select>
    <span class="error-msg">Selecciona una provincia.</span>
  </div>
</div>

<div class="field" id="f-lateralidad">
  <label>Lateralidad dominante <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="lateralidad" id="lat-d" value="Derecho" required>
      <label for="lat-d">⚾ Derecho</label>
    </div>
    <div class="opt">
      <input type="radio" name="lateralidad" id="lat-i" value="Izquierdo">
      <label for="lat-i">⚾ Izquierdo</label>
    </div>
    <div class="opt">
      <input type="radio" name="lateralidad" id="lat-a" value="Ambidiestro">
      <label for="lat-a">⚾ Ambidiestro</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>
```

  </div><!-- /sec1 -->

  <div class="divider"></div>

  <!-- ═══════════════════════════════════════════
       SECCIÓN 2 · CARACTERÍSTICAS DEPORTIVAS
  ═══════════════════════════════════════════ -->

  <div class="section" id="sec2">
    <div class="section-header">
      <div class="section-num">02</div>
      <div class="section-label">
        <h2>Características Deportivas</h2>
        <p>Posición, experiencia y nivel competitivo</p>
      </div>
    </div>

```
<div class="field" id="f-posicion">
  <label>Posición principal de juego <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="posicion" id="pos-lanz" value="Lanzador" required>
      <label for="pos-lanz">🏟️ Lanzador (Pitcher)</label>
    </div>
    <div class="opt">
      <input type="radio" name="posicion" id="pos-cat" value="Receptor">
      <label for="pos-cat">🎯 Receptor (Catcher)</label>
    </div>
    <div class="opt">
      <input type="radio" name="posicion" id="pos-inf" value="Infielder">
      <label for="pos-inf">⚡ Infielder</label>
    </div>
    <div class="opt">
      <input type="radio" name="posicion" id="pos-out" value="Outfielder">
      <label for="pos-out">🌿 Outfielder</label>
    </div>
    <div class="opt">
      <input type="radio" name="posicion" id="pos-dh" value="Designated Hitter">
      <label for="pos-dh">🪄 Designated Hitter</label>
    </div>
    <div class="opt">
      <input type="radio" name="posicion" id="pos-multi" value="Multiple posiciones">
      <label for="pos-multi">🔄 Múltiples posiciones</label>
    </div>
  </div>
  <span class="error-msg">Selecciona tu posición.</span>
</div>

<!-- Subtipo lanzador (condicional) -->
<div class="conditional" id="cond-lanzador">
  <div class="field">
    <label>¿Cuál es tu rol como lanzador?</label>
    <div class="options-grid cols-3">
      <div class="opt">
        <input type="radio" name="rol_lanzador" id="rol-abre" value="Abridor">
        <label for="rol-abre">Abridor</label>
      </div>
      <div class="opt">
        <input type="radio" name="rol_lanzador" id="rol-rel" value="Relevista">
        <label for="rol-rel">Relevista</label>
      </div>
      <div class="opt">
        <input type="radio" name="rol_lanzador" id="rol-cer" value="Cerrador">
        <label for="rol-cer">Cerrador</label>
      </div>
    </div>
  </div>
</div>

<div class="field-row">
  <div class="field" id="f-años">
    <label>Años de práctica intensiva del béisbol <span class="req">*</span></label>
    <select name="años_practica" required>
      <option value="">Seleccionar…</option>
      <option value="1-2">1–2 años</option>
      <option value="3-4">3–4 años</option>
      <option value="5-6">5–6 años</option>
      <option value="7-8">7–8 años</option>
      <option value="9+">9 o más años</option>
    </select>
    <span class="error-msg">Selecciona los años de práctica.</span>
  </div>

  <div class="field" id="f-inicio">
    <label>Edad de inicio en béisbol competitivo <span class="req">*</span></label>
    <input type="number" name="edad_inicio" min="5" max="21" placeholder="Ej: 10" required>
    <span class="error-msg">Ingresa una edad válida.</span>
  </div>
</div>

<div class="field" id="f-nivel">
  <label>Nivel competitivo actual <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="nivel" id="niv-acad" value="Academia profesional" required>
      <label for="niv-acad">🏆 Academia profesional (MLB)</label>
    </div>
    <div class="opt">
      <input type="radio" name="nivel" id="niv-liga-d" value="Liga dominicana">
      <label for="niv-liga-d">⭐ Liga dominicana (nacional)</label>
    </div>
    <div class="opt">
      <input type="radio" name="nivel" id="niv-liga-a" value="Liga amateur">
      <label for="niv-liga-a">🌟 Liga amateur / regional</label>
    </div>
    <div class="opt">
      <input type="radio" name="nivel" id="niv-uni" value="Universitario">
      <label for="niv-uni">🎓 Universitario</label>
    </div>
  </div>
  <span class="error-msg">Selecciona un nivel.</span>
</div>

<div class="field" id="f-ligas-sim">
  <label>¿Participas en múltiples ligas o equipos simultáneamente? <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="ligas_sim" id="lsim-s" value="Sí" required>
      <label for="lsim-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="ligas_sim" id="lsim-n" value="No">
      <label for="lsim-n">No</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>
```

  </div><!-- /sec2 -->

  <div class="divider"></div>

  <!-- ═══════════════════════════════════════════
       SECCIÓN 3 · CARGA DE LANZAMIENTOS
  ═══════════════════════════════════════════ -->

  <div class="section" id="sec3">
    <div class="section-header">
      <div class="section-num">03</div>
      <div class="section-label">
        <h2>Carga de Lanzamientos y Entrenamiento</h2>
        <p>Frecuencia, volumen e intensidad</p>
      </div>
    </div>

```
<div class="field-row">
  <div class="field" id="f-dias-sem">
    <label>Días de entrenamiento por semana <span class="req">*</span></label>
    <select name="dias_entrenamiento" required>
      <option value="">Seleccionar…</option>
      <option value="1-2">1–2 días</option>
      <option value="3-4">3–4 días</option>
      <option value="5-6">5–6 días</option>
      <option value="7">Todos los días</option>
    </select>
    <span class="error-msg">Selecciona los días.</span>
  </div>

  <div class="field" id="f-horas-dia">
    <label>Horas de entrenamiento por día <span class="req">*</span></label>
    <select name="horas_entrenamiento" required>
      <option value="">Seleccionar…</option>
      <option value="<1">&lt;1 hora</option>
      <option value="1-2">1–2 horas</option>
      <option value="2-3">2–3 horas</option>
      <option value="3-4">3–4 horas</option>
      <option value=">4">Más de 4 horas</option>
    </select>
    <span class="error-msg">Selecciona las horas.</span>
  </div>
</div>

<div class="field" id="f-lanzamientos-dia">
  <label>Número aproximado de lanzamientos por sesión de entrenamiento <span class="req">*</span></label>
  <p class="field-hint">Incluye bullpen, práctica de bateo y ejercicios</p>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-0" value="<25" required>
      <label for="ls-0">Menos de 25</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-1" value="25-50">
      <label for="ls-1">25–50</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-2" value="51-75">
      <label for="ls-2">51–75</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-3" value="76-100">
      <label for="ls-3">76–100</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-4" value="101-125">
      <label for="ls-4">101–125</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_sesion" id="ls-5" value=">125">
      <label for="ls-5">Más de 125</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-lanz-juego">
  <label>Número de lanzamientos en partido / juego <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-0" value="<25" required>
      <label for="lj-0">Menos de 25</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-1" value="25-50">
      <label for="lj-1">25–50</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-2" value="51-75">
      <label for="lj-2">51–75</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-3" value="76-100">
      <label for="lj-3">76–100</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-4" value=">100">
      <label for="lj-4">Más de 100</label>
    </div>
    <div class="opt">
      <input type="radio" name="lanzamientos_juego" id="lj-na" value="N/A">
      <label for="lj-na">No aplica</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-juegos-sem">
  <label>Partidos / juegos por semana (en temporada) <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="juegos_sem" id="js-0" value="0" required>
      <label for="js-0">0 (fuera de temporada)</label>
    </div>
    <div class="opt">
      <input type="radio" name="juegos_sem" id="js-1" value="1">
      <label for="js-1">1</label>
    </div>
    <div class="opt">
      <input type="radio" name="juegos_sem" id="js-2" value="2-3">
      <label for="js-2">2–3</label>
    </div>
    <div class="opt">
      <input type="radio" name="juegos_sem" id="js-3" value="4-5">
      <label for="js-3">4–5</label>
    </div>
    <div class="opt">
      <input type="radio" name="juegos_sem" id="js-4" value=">5">
      <label for="js-4">Más de 5</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<!-- VELOCIDAD -->
<div class="field" id="f-velocidad">
  <label>Velocidad máxima de lanzamiento estimada (mph) <span class="req">*</span></label>
  <p class="field-hint">Si no conoces el dato exacto, indica el rango aproximado</p>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="velocidad" id="v-0" value="<70 mph" required>
      <label for="v-0">Menos de 70 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-1" value="70-74 mph">
      <label for="v-1">70–74 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-2" value="75-79 mph">
      <label for="v-2">75–79 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-3" value="80-84 mph">
      <label for="v-3">80–84 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-4" value="85-89 mph">
      <label for="v-4">85–89 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-5" value="90-94 mph">
      <label for="v-5">90–94 mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-6" value="95+ mph">
      <label for="v-6">95+ mph</label>
    </div>
    <div class="opt">
      <input type="radio" name="velocidad" id="v-na" value="No sé / No aplica">
      <label for="v-na">No sé / No aplica</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<!-- TIPOS DE LANZAMIENTO -->
<div class="field">
  <label>Tipos de lanzamiento que realizas regularmente <span class="req">*</span></label>
  <p class="field-hint">Puedes marcar más de uno</p>
  <div class="options-grid cols-2">
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-fb" value="Fastball (recta)">
      <label for="tl-fb">Fastball (recta)</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-cb" value="Curveball (curva)">
      <label for="tl-cb">Curveball (curva)</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-sl" value="Slider">
      <label for="tl-sl">Slider</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-ch" value="Changeup">
      <label for="tl-ch">Changeup</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-si" value="Sinker">
      <label for="tl-si">Sinker / Two-seam</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-cu" value="Cutter">
      <label for="tl-cu">Cutter</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-kn" value="Knuckleball">
      <label for="tl-kn">Knuckleball</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="tipo_lanzamiento" id="tl-sp" value="Splitter">
      <label for="tl-sp">Splitter</label>
    </div>
  </div>
</div>

<!-- EDAD CURVA -->
<div class="field" id="f-edad-curva">
  <label>¿A qué edad comenzaste a lanzar curveball o slider regularmente?</label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-0" value="Antes de los 12 años">
      <label for="ec-0">Antes de los 12</label>
    </div>
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-1" value="12-13 años">
      <label for="ec-1">12–13 años</label>
    </div>
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-2" value="14-15 años">
      <label for="ec-2">14–15 años</label>
    </div>
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-3" value="16-17 años">
      <label for="ec-3">16–17 años</label>
    </div>
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-4" value="18+ años">
      <label for="ec-4">18 o más</label>
    </div>
    <div class="opt">
      <input type="radio" name="edad_curva" id="ec-na" value="No lanzo estos pitches">
      <label for="ec-na">No lanzo estos pitches</label>
    </div>
  </div>
</div>

<div class="field" id="f-descanso">
  <label>Días de descanso completo entre apariciones como lanzador <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-0" value="0-1 día" required>
      <label for="dd-0">0–1 día</label>
    </div>
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-1" value="2-3 días">
      <label for="dd-1">2–3 días</label>
    </div>
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-2" value="4-5 días">
      <label for="dd-2">4–5 días</label>
    </div>
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-3" value="6-7 días">
      <label for="dd-3">6–7 días</label>
    </div>
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-4" value=">7 días">
      <label for="dd-4">Más de 7 días</label>
    </div>
    <div class="opt">
      <input type="radio" name="dias_descanso" id="dd-na" value="No soy lanzador">
      <label for="dd-na">No soy lanzador</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-intensidad">
  <label>Intensidad percibida del entrenamiento habitual</label>
  <div class="scale-wrap">
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-1" value="1">
      <label for="int-1"><span>1</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-2" value="2">
      <label for="int-2"><span>2</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-3" value="3">
      <label for="int-3"><span>3</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-4" value="4">
      <label for="int-4"><span>4</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-5" value="5">
      <label for="int-5"><span>5</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-6" value="6">
      <label for="int-6"><span>6</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-7" value="7">
      <label for="int-7"><span>7</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-8" value="8">
      <label for="int-8"><span>8</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-9" value="9">
      <label for="int-9"><span>9</span></label>
    </div>
    <div class="scale-item">
      <input type="radio" name="intensidad" id="int-10" value="10">
      <label for="int-10"><span>10</span></label>
    </div>
  </div>
  <div class="scale-labels">
    <span>Muy suave</span>
    <span>Máximo esfuerzo</span>
  </div>
</div>
```

  </div><!-- /sec3 -->

  <div class="divider"></div>

  <!-- ═══════════════════════════════════════════
       SECCIÓN 4 · ANTECEDENTES CLÍNICOS
  ═══════════════════════════════════════════ -->

  <div class="section" id="sec4">
    <div class="section-header">
      <div class="section-num">04</div>
      <div class="section-label">
        <h2>Antecedentes Clínicos del Codo</h2>
        <p>Historia de dolor, lesiones y tratamientos</p>
      </div>
    </div>

```
<div class="alert-box">
  <strong>Confidencialidad garantizada.</strong> La información médica que proveas es completamente confidencial y solo se usará con fines estadísticos. No se compartirá tu identidad.
</div>

<div class="field" id="f-dolor-codo">
  <label>¿Has experimentado dolor en el codo (brazo de lanzar) durante o después de lanzar? <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="dolor_codo" id="dc-s" value="Sí" required>
      <label for="dc-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="dolor_codo" id="dc-n" value="No">
      <label for="dc-n">No</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<!-- CONDICIONAL: si hay dolor -->
<div class="conditional" id="cond-dolor">

  <div class="field">
    <label>Localización del dolor</label>
    <div class="options-grid cols-2">
      <div class="opt check">
        <input type="checkbox" name="loc_dolor" id="ld-med" value="Cara medial (interna)">
        <label for="ld-med">Cara medial (interna)</label>
      </div>
      <div class="opt check">
        <input type="checkbox" name="loc_dolor" id="ld-lat" value="Cara lateral (externa)">
        <label for="ld-lat">Cara lateral (externa)</label>
      </div>
      <div class="opt check">
        <input type="checkbox" name="loc_dolor" id="ld-post" value="Posterior">
        <label for="ld-post">Posterior</label>
      </div>
      <div class="opt check">
        <input type="checkbox" name="loc_dolor" id="ld-gen" value="General / difuso">
        <label for="ld-gen">General / difuso</label>
      </div>
    </div>
  </div>

  <div class="field">
    <label>Intensidad del dolor (EVA)</label>
    <div class="scale-wrap">
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-1" value="1">
        <label for="evd-1"><span>1</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-2" value="2">
        <label for="evd-2"><span>2</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-3" value="3">
        <label for="evd-3"><span>3</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-4" value="4">
        <label for="evd-4"><span>4</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-5" value="5">
        <label for="evd-5"><span>5</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-6" value="6">
        <label for="evd-6"><span>6</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-7" value="7">
        <label for="evd-7"><span>7</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-8" value="8">
        <label for="evd-8"><span>8</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-9" value="9">
        <label for="evd-9"><span>9</span></label>
      </div>
      <div class="scale-item">
        <input type="radio" name="intensidad_dolor" id="evd-10" value="10">
        <label for="evd-10"><span>10</span></label>
      </div>
    </div>
    <div class="scale-labels"><span>Sin dolor</span><span>Dolor insoportable</span></div>
  </div>

  <div class="field">
    <label>¿El dolor te obligó a dejar de lanzar o reducir tu actividad?</label>
    <div class="options-grid cols-3">
      <div class="opt">
        <input type="radio" name="dolor_limita" id="dl-s" value="Sí, dejé de lanzar">
        <label for="dl-s">Sí, dejé de lanzar</label>
      </div>
      <div class="opt">
        <input type="radio" name="dolor_limita" id="dl-r" value="Sí, reduje actividad">
        <label for="dl-r">Reduje actividad</label>
      </div>
      <div class="opt">
        <input type="radio" name="dolor_limita" id="dl-n" value="No, seguí lanzando">
        <label for="dl-n">No, seguí igual</label>
      </div>
    </div>
  </div>

  <div class="field">
    <label>¿Buscaste atención médica por ese dolor?</label>
    <div class="options-grid cols-2">
      <div class="opt">
        <input type="radio" name="atencion_medica" id="am-s" value="Sí">
        <label for="am-s">Sí</label>
      </div>
      <div class="opt">
        <input type="radio" name="atencion_medica" id="am-n" value="No">
        <label for="am-n">No</label>
      </div>
    </div>
  </div>

</div><!-- /cond-dolor -->

<div class="field" id="f-lesion-ucl">
  <label>¿Has sido diagnosticado con alguna lesión del ligamento colateral cubital (UCL)? <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="lesion_ucl" id="lu-s" value="Sí" required>
      <label for="lu-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="lesion_ucl" id="lu-n" value="No">
      <label for="lu-n">No</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<!-- CONDICIONAL: lesión UCL -->
<div class="conditional" id="cond-ucl">
  <div class="field">
    <label>Grado de la lesión según diagnóstico médico</label>
    <div class="options-grid cols-2">
      <div class="opt">
        <input type="radio" name="grado_lesion" id="gl-1" value="Grado 1 (esguince leve)">
        <label for="gl-1">Grado 1 – Esguince leve</label>
      </div>
      <div class="opt">
        <input type="radio" name="grado_lesion" id="gl-2" value="Grado 2 (desgarro parcial)">
        <label for="gl-2">Grado 2 – Desgarro parcial</label>
      </div>
      <div class="opt">
        <input type="radio" name="grado_lesion" id="gl-3" value="Grado 3 (ruptura completa)">
        <label for="gl-3">Grado 3 – Ruptura completa</label>
      </div>
      <div class="opt">
        <input type="radio" name="grado_lesion" id="gl-nd" value="No sé el grado">
        <label for="gl-nd">No sé el grado exacto</label>
      </div>
    </div>
  </div>
</div>

<!-- CIRUGÍA TOMMY JOHN — PREGUNTA CENTRAL -->
<div class="field" id="f-tommy">
  <label>¿Te has realizado la cirugía de reconstrucción del UCL (Cirugía Tommy John)? <span class="req">*</span></label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="cirugia_tommy" id="tj-s" value="Sí" required>
      <label for="tj-s">✅ Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="cirugia_tommy" id="tj-n" value="No">
      <label for="tj-n">❌ No</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<!-- CONDICIONAL: cirugía Tommy John SÍ -->
<div class="conditional" id="cond-tommy">

  <div class="field-row">
    <div class="field">
      <label>Edad al momento de la cirugía</label>
      <input type="number" name="edad_cirugia" min="10" max="21" placeholder="Ej: 18">
    </div>
    <div class="field">
      <label>¿Dónde se realizó la cirugía?</label>
      <select name="lugar_cirugia">
        <option value="">Seleccionar…</option>
        <option>República Dominicana</option>
        <option>Estados Unidos</option>
        <option>Otro país</option>
      </select>
    </div>
  </div>

  <div class="field">
    <label>¿Fue tu primera cirugía Tommy John o una revisión?</label>
    <div class="options-grid cols-2">
      <div class="opt">
        <input type="radio" name="primera_cirugia" id="pc-1" value="Primera vez">
        <label for="pc-1">Primera vez</label>
      </div>
      <div class="opt">
        <input type="radio" name="primera_cirugia" id="pc-2" value="Revisión (segunda o más)">
        <label for="pc-2">Revisión (segunda o más)</label>
      </div>
    </div>
  </div>

  <div class="field">
    <label>¿Completaste el proceso de rehabilitación postoperatoria?</label>
    <div class="options-grid cols-3">
      <div class="opt">
        <input type="radio" name="rehab_completa" id="rc-s" value="Sí, completamente">
        <label for="rc-s">Sí, completamente</label>
      </div>
      <div class="opt">
        <input type="radio" name="rehab_completa" id="rc-p" value="Parcialmente">
        <label for="rc-p">Parcialmente</label>
      </div>
      <div class="opt">
        <input type="radio" name="rehab_completa" id="rc-n" value="No">
        <label for="rc-n">No</label>
      </div>
    </div>
  </div>

  <div class="field">
    <label>¿Retornaste a la práctica del béisbol competitivo tras la cirugía?</label>
    <div class="options-grid cols-3">
      <div class="opt">
        <input type="radio" name="retorno" id="ret-s" value="Sí">
        <label for="ret-s">Sí</label>
      </div>
      <div class="opt">
        <input type="radio" name="retorno" id="ret-p" value="En proceso">
        <label for="ret-p">En proceso</label>
      </div>
      <div class="opt">
        <input type="radio" name="retorno" id="ret-n" value="No">
        <label for="ret-n">No</label>
      </div>
    </div>
  </div>

</div><!-- /cond-tommy -->

<!-- CONDICIONAL: cirugía Tommy John NO -->
<div class="conditional" id="cond-no-tommy">
  <div class="field">
    <label>¿Te han indicado o recomendado la cirugía Tommy John pero aún no te la has realizado?</label>
    <div class="options-grid cols-2">
      <div class="opt">
        <input type="radio" name="indicacion_tj" id="itj-s" value="Sí">
        <label for="itj-s">Sí, me la recomendaron</label>
      </div>
      <div class="opt">
        <input type="radio" name="indicacion_tj" id="itj-n" value="No">
        <label for="itj-n">No, nunca me la indicaron</label>
      </div>
    </div>
  </div>
</div>

<div class="field" id="f-otras-lesiones">
  <label>¿Has tenido otras lesiones del brazo de lanzar? (puedes marcar varias)</label>
  <div class="options-grid cols-2">
    <div class="opt check">
      <input type="checkbox" name="otras_lesiones" id="ol-manguito" value="Lesión del manguito rotador">
      <label for="ol-manguito">Lesión del manguito rotador</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="otras_lesiones" id="ol-epicond" value="Epicondilitis">
      <label for="ol-epicond">Epicondilitis medial/lateral</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="otras_lesiones" id="ol-stress" value="Fractura por estrés">
      <label for="ol-stress">Fractura por estrés</label>
    </div>
    <div class="opt check">
      <input type="checkbox" name="otras_lesiones" id="ol-none" value="Ninguna">
      <label for="ol-none">Ninguna</label>
    </div>
  </div>
</div>
```

  </div><!-- /sec4 -->

  <div class="divider"></div>

  <!-- ═══════════════════════════════════════════
       SECCIÓN 5 · PREVENCIÓN Y SUPERVISIÓN
  ═══════════════════════════════════════════ -->

  <div class="section" id="sec5">
    <div class="section-header">
      <div class="section-num">05</div>
      <div class="section-label">
        <h2>Prevención y Supervisión Médica</h2>
        <p>Acceso a atención y prácticas preventivas</p>
      </div>
    </div>

```
<div class="field" id="f-sup-med">
  <label>¿Tu academia o equipo cuenta con supervisión médica o fisioterapéutica? <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="supervision_medica" id="sm-s" value="Sí, regularmente" required>
      <label for="sm-s">Sí, regularmente</label>
    </div>
    <div class="opt">
      <input type="radio" name="supervision_medica" id="sm-a" value="Sí, ocasionalmente">
      <label for="sm-a">Ocasionalmente</label>
    </div>
    <div class="opt">
      <input type="radio" name="supervision_medica" id="sm-n" value="No">
      <label for="sm-n">No</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-control-carga">
  <label>¿Existe un protocolo o control de la carga de lanzamientos en tu academia? <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="control_carga" id="cc-s" value="Sí" required>
      <label for="cc-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="control_carga" id="cc-n" value="No">
      <label for="cc-s-n">No</label>
    </div>
    <div class="opt">
      <input type="radio" name="control_carga" id="cc-ns" value="No sé">
      <label for="cc-ns">No sé</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-calentamiento">
  <label>¿Realizas calentamiento específico del brazo antes de lanzar? <span class="req">*</span></label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="calentamiento" id="cal-siem" value="Siempre" required>
      <label for="cal-siem">Siempre</label>
    </div>
    <div class="opt">
      <input type="radio" name="calentamiento" id="cal-frec" value="Frecuentemente">
      <label for="cal-frec">Frecuentemente</label>
    </div>
    <div class="opt">
      <input type="radio" name="calentamiento" id="cal-av" value="A veces">
      <label for="cal-av">A veces</label>
    </div>
    <div class="opt">
      <input type="radio" name="calentamiento" id="cal-rara" value="Raramente">
      <label for="cal-rara">Raramente</label>
    </div>
    <div class="opt">
      <input type="radio" name="calentamiento" id="cal-nun" value="Nunca">
      <label for="cal-nun">Nunca</label>
    </div>
  </div>
  <span class="error-msg">Selecciona una opción.</span>
</div>

<div class="field" id="f-temporada-descanso">
  <label>¿Tienes un período de descanso activo (off-season) donde no lanzas?</label>
  <div class="options-grid cols-3">
    <div class="opt">
      <input type="radio" name="off_season" id="os-s" value="Sí">
      <label for="os-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="off_season" id="os-n" value="No">
      <label for="os-n">No, lanzo todo el año</label>
    </div>
    <div class="opt">
      <input type="radio" name="off_season" id="os-p" value="Parcialmente">
      <label for="os-p">Parcialmente</label>
    </div>
  </div>
</div>

<div class="field">
  <label>¿Has recibido educación sobre prevención de lesiones del codo?</label>
  <div class="options-grid cols-2">
    <div class="opt">
      <input type="radio" name="educacion_prev" id="ep-s" value="Sí">
      <label for="ep-s">Sí</label>
    </div>
    <div class="opt">
      <input type="radio" name="educacion_prev" id="ep-n" value="No">
      <label for="ep-n">No</label>
    </div>
  </div>
</div>

<div class="field">
  <label>Comentarios adicionales o información relevante que quieras agregar</label>
  <textarea name="comentarios" placeholder="Escribe aquí cualquier información adicional sobre lesiones, tratamientos, contexto deportivo u otro aspecto que consideres importante…"></textarea>
</div>
```

  </div><!-- /sec5 -->

  <!-- SUBMIT -->

  <div class="submit-zone">
    <p>
      Al enviar este cuestionario confirmas que la información es verídica y que participas de forma voluntaria.<br>
      Tu información es confidencial y solo será usada con fines académicos en el marco del estudio de UNIBE.
    </p>
    <button type="submit" class="btn-submit">ENVIAR CUESTIONARIO</button>
  </div>

  </form>
  </div><!-- /form-content -->

  <!-- PANTALLA ÉXITO -->

  <div class="success-screen" id="successScreen">
    <div class="success-icon">✓</div>
    <h2>¡CUESTIONARIO COMPLETADO!</h2>
    <p>Gracias por tu participación. Tu información ha sido registrada correctamente.<br>Este estudio contribuirá a mejorar la salud de los jugadores de béisbol dominicanos.</p>
  </div>

</div><!-- /main -->

<div class="footer">
  <p>UNIBE · Facultad de Ciencias de la Salud · Escuela de Medicina · 2026</p>
  <div class="footer-dots">
    <span class="dot-red"></span>
    <span class="dot-gold"></span>
    <span class="dot-light"></span>
  </div>
</div>

<script>
// ── PROGRESS ──────────────────────────────────────────────────────────
const sections = ['sec1','sec2','sec3','sec4','sec5'];
const totalSections = sections.length;

function updateProgress() {
  const inputs = document.querySelectorAll('#mainForm input, #mainForm select, #mainForm textarea');
  let filled = 0, total = 0;

  inputs.forEach(inp => {
    if (inp.type === 'radio' || inp.type === 'checkbox') {
      const name = inp.name;
      if (!document.querySelector(`[name="${name}"][data-counted]`)) {
        const group = document.querySelectorAll(`[name="${name}"]`);
        const checked = document.querySelector(`[name="${name}"]:checked`);
        group.forEach(el => el.dataset.counted = '1');
        total++;
        if (checked) filled++;
      }
      return;
    }
    if (inp.type === 'hidden') return;
    total++;
    if (inp.value.trim()) filled++;
  });

  // reset counted flags
  document.querySelectorAll('[data-counted]').forEach(el => delete el.dataset.counted);

  const pct = total > 0 ? Math.round((filled / total) * 100) : 0;
  document.getElementById('progressFill').style.width = pct + '%';
  document.getElementById('progressPct').textContent = pct + '%';
}

// ── CONDITIONALS ─────────────────────────────────────────────────────
function setupConditional(triggerName, triggerValue, condId) {
  const inputs = document.querySelectorAll(`[name="${triggerName}"]`);
  const cond = document.getElementById(condId);
  if (!cond) return;

  function check() {
    const sel = document.querySelector(`[name="${triggerName}"]:checked`);
    const show = sel && sel.value === triggerValue;
    cond.classList.toggle('visible', show);
    if (!show) {
      cond.querySelectorAll('input, select, textarea').forEach(el => {
        if (el.type === 'radio' || el.type === 'checkbox') el.checked = false;
        else el.value = '';
      });
    }
  }

  inputs.forEach(inp => inp.addEventListener('change', () => { check(); updateProgress(); }));
  check();
}

setupConditional('posicion', 'Lanzador', 'cond-lanzador');
setupConditional('dolor_codo', 'Sí', 'cond-dolor');
setupConditional('lesion_ucl', 'Sí', 'cond-ucl');
setupConditional('cirugia_tommy', 'Sí', 'cond-tommy');
setupConditional('cirugia_tommy', 'No', 'cond-no-tommy');

// Handle the "No Tommy" conditional separately (both yes/no exclusion)
document.querySelectorAll('[name="cirugia_tommy"]').forEach(inp => {
  inp.addEventListener('change', () => {
    const sel = document.querySelector('[name="cirugia_tommy"]:checked');
    document.getElementById('cond-tommy').classList.toggle('visible', sel && sel.value === 'Sí');
    document.getElementById('cond-no-tommy').classList.toggle('visible', sel && sel.value === 'No');
  });
});

// ── PROGRESS UPDATE ON ALL CHANGES ───────────────────────────────────
document.getElementById('mainForm').addEventListener('change', updateProgress);
document.getElementById('mainForm').addEventListener('input', updateProgress);

// ── VALIDATION ────────────────────────────────────────────────────────
function validateForm() {
  const requiredFields = [
    { id: 'f-edad', check: () => { const v = parseInt(document.querySelector('[name="edad"]')?.value); return v >= 17 && v <= 21; }},
    { id: 'f-provincia', check: () => document.querySelector('[name="provincia"]')?.value },
    { id: 'f-lateralidad', check: () => document.querySelector('[name="lateralidad"]:checked') },
    { id: 'f-posicion', check: () => document.querySelector('[name="posicion"]:checked') },
    { id: 'f-años', check: () => document.querySelector('[name="años_practica"]')?.value },
    { id: 'f-inicio', check: () => document.querySelector('[name="edad_inicio"]')?.value },
    { id: 'f-nivel', check: () => document.querySelector('[name="nivel"]:checked') },
    { id: 'f-ligas-sim', check: () => document.querySelector('[name="ligas_sim"]:checked') },
    { id: 'f-dias-sem', check: () => document.querySelector('[name="dias_entrenamiento"]')?.value },
    { id: 'f-horas-dia', check: () => document.querySelector('[name="horas_entrenamiento"]')?.value },
    { id: 'f-lanzamientos-dia', check: () => document.querySelector('[name="lanzamientos_sesion"]:checked') },
    { id: 'f-lanz-juego', check: () => document.querySelector('[name="lanzamientos_juego"]:checked') },
    { id: 'f-juegos-sem', check: () => document.querySelector('[name="juegos_sem"]:checked') },
    { id: 'f-velocidad', check: () => document.querySelector('[name="velocidad"]:checked') },
    { id: 'f-descanso', check: () => document.querySelector('[name="dias_descanso"]:checked') },
    { id: 'f-dolor-codo', check: () => document.querySelector('[name="dolor_codo"]:checked') },
    { id: 'f-lesion-ucl', check: () => document.querySelector('[name="lesion_ucl"]:checked') },
    { id: 'f-tommy', check: () => document.querySelector('[name="cirugia_tommy"]:checked') },
    { id: 'f-sup-med', check: () => document.querySelector('[name="supervision_medica"]:checked') },
    { id: 'f-control-carga', check: () => document.querySelector('[name="control_carga"]:checked') },
    { id: 'f-calentamiento', check: () => document.querySelector('[name="calentamiento"]:checked') },
  ];

  let valid = true;

  requiredFields.forEach(({ id, check }) => {
    const el = document.getElementById(id);
    if (!el) return;
    const ok = check();
    el.classList.toggle('error', !ok);
    if (!ok) valid = false;
  });

  return valid;
}

// ── FORM SUBMIT ──────────────────────────────────────────────────────
document.getElementById('mainForm').addEventListener('submit', function(e) {
  e.preventDefault();

  if (!validateForm()) {
    // Scroll to first error
    const firstError = document.querySelector('.field.error');
    if (firstError) firstError.scrollIntoView({ behavior: 'smooth', block: 'center' });
    return;
  }

  // Collect data
  const formData = new FormData(this);
  const data = {};
  for (let [key, val] of formData.entries()) {
    if (data[key]) {
      data[key] = Array.isArray(data[key]) ? [...data[key], val] : [data[key], val];
    } else {
      data[key] = val;
    }
  }

  console.log('Datos del cuestionario:', JSON.stringify(data, null, 2));

  // Show success
  document.getElementById('formContent').style.display = 'none';
  document.getElementById('successScreen').classList.add('visible');
  document.getElementById('progressFill').style.width = '100%';
  document.getElementById('progressPct').textContent = '100%';
  document.getElementById('progressLabel').textContent = 'Completado';
  window.scrollTo({ top: 0, behavior: 'smooth' });
});

// Clear error on change
document.getElementById('mainForm').addEventListener('change', (e) => {
  const field = e.target.closest('.field');
  if (field) field.classList.remove('error');
});

updateProgress();
</script>

</body>
</html>
