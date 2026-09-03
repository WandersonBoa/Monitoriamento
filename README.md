<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>WMB Correlação — WINFUT × WDOFUT</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="app">
    <header class="topbar">
      <div>
        <strong>WMB_CORRELACAO</strong>
        <span class="version">v1.0</span>
        <span class="pair">WINFUT × WDOFUT</span>
      </div>
      <div class="live"><span class="dot"></span> AO VIVO — DEMONSTRAÇÃO</div>
    </header>

    <main class="dashboard">
      <section class="card gauge-card">
        <h2>VELOCÍMETRO DE CORRELAÇÃO</h2>
        <div class="gauge-wrap">
          <canvas id="gauge" width="420" height="260"></canvas>
        </div>
        <div id="corrValue" class="big-value">0,00</div>
        <div id="corrClass" class="corr-class">NEUTRA</div>
      </section>

      <section class="card summary-card">
        <h2>RESUMO</h2>
        <div class="metric"><span>Correlação atual</span><b id="currentCorr">0,00</b></div>
        <div class="metric"><span>Correlação média</span><b id="avgCorr">0,00</b></div>
        <div class="metric"><span>Força</span><b id="strength">—</b></div>
        <div class="metric"><span>Direção</span><b id="direction">—</b></div>
        <div class="metric"><span>WINFUT</span><b id="winPrice">—</b></div>
        <div class="metric"><span>WDOFUT</span><b id="wdoPrice">—</b></div>
      </section>

      <section class="card chart-card">
        <h2>LINHAS DE CORRELAÇÃO</h2>
        <canvas id="corrChart"></canvas>
        <div class="legend">
          <span><i class="positive"></i> positiva</span>
          <span><i class="negative"></i> negativa</span>
          <span><i class="zero"></i> zero</span>
        </div>
      </section>

      <section class="card signals-card">
        <h2>SINAIS</h2>
        <div id="signal" class="signal neutral">NEUTRO</div>
        <div class="signal-box">
          <span>TENDÊNCIA</span>
          <b id="trend">NEUTRA</b>
        </div>
        <div class="signal-box">
          <span>FILTRO (ADX)</span>
          <b id="adx">—</b>
          <small id="adxStatus">AGUARDANDO</small>
        </div>
        <div class="di-row">
          <div><span>DI+</span><b id="diPlus">—</b></div>
          <div><span>DI-</span><b id="diMinus">—</b></div>
        </div>
      </section>

      <section class="card bottom-card">
        <div class="strength-title">FORÇA DA CORRELAÇÃO</div>
        <div class="strength-bar">
          <div class="ticks"></div>
          <div id="strengthMarker" class="marker"></div>
        </div>
        <label>Período: <input id="period" type="range" min="5" max="50" value="21"> <b id="periodValue">21</b></label>
        <div class="update">Atualização: <b id="clock">--:--:--</b> <span class="live"><span class="dot"></span> Ao vivo</span></div>
      </section>
    </main>
  </div>
  <script src="app.js"></script>
</body>
</html>
