# 🤖 Robot Trajectory Simulator

Simulatore di traiettorie per robot industriali ABB con cinematica avanzata e esportazione codice RAPID.

## Panoramica

Tool Python per la simulazione offline di movimenti robotici, sviluppato per ottimizzare cicli di saldatura senza fermare la produzione. Calcola profili di moto realistici, genera codice RAPID e visualizza traiettorie con heatmap di velocità.

## Caratteristiche Tecniche

- **Profili di moto trapezoidali**: Accelerazione costante, velocità di crociera, decelerazione 
- **Gestione zone ABB**: z0, z1, z5, z10, z20, z50, fine con calcolo deviazione pre-punto
- **Cinematica 2D**: Interpolazione cartesiana con step temporale configurabile (default 20ms)
- **Esportazione RAPID**: Codice sintatticamente corretto per controller IRC5
- **Visualizzazione**: Heatmap velocità, zone di precisione, vettori direzione

  
## Funzionalità

## 🔍 Analisi Descrittiva
- OEE calcolato con formula completa: Disponibilità × Performance × Qualità
- Benchmark comparativo multi-robot
- Trend temporali con medie mobili

## ⚠️ Anomaly Detection
- Soglie dinamiche per temperatura motore (>60°C warning, >70°C critical)
- Pattern errori collisione anomali
- Degradazione efficienza sotto 75%

## 🔮 Predictive Maintenance
- Regressione trend efficienza ultimi 7 giorni
- Predizione giorni rimanenti alla soglia critica (60% OEE)
- Prioritizzazione interventi

## 📈 Visualizzazione
- Heatmap correlazioni (temperatura vs errori vs efficienza)
- Scatter plot efficienza vs consumo energetico
- Forecast manutenzione con color coding


## Output

| Traiettoria 2D | Profili di moto | Preview progetto |
|:--:|:--:|:--:|
| ![Trajectory](examples/outputs/trajectory_2d.png) | ![Velocity](examples/outputs/velocity_profile.png) | ![Preview](examples/outputs/project_preview.png) |


## Installazione

```bash
git clone https://github.com/tuousername/robot-trajectory-simulator.git
cd robot-trajectory-simulator
pip install -r requirements.txt
