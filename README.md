# MNQ Trading Automation - Pine Script Collection

Collection complète d'indicateurs et stratégies Pine Script v5 pour le trading automatisé du MNQ (Micro E-mini Nasdaq-100).

## 📋 Contenu

### 🎯 Stratégie Principale
- **`mnq_strategy_main.pine`** - Stratégie de trading complète avec gestion des risques

### 📊 Indicateurs d'Analyse
- **`mnq_trend_analyzer.pine`** - Analyse de tendance avec moyennes mobiles et ADX
- **`mnq_momentum_oscillators.pine`** - Oscillateurs de momentum (RSI, Stochastic, MACD, Williams %R)
- **`mnq_volume_analysis.pine`** - Analyse de volume avec OBV, VWAP et détection de spikes
- **`mnq_support_resistance.pine`** - Niveaux de support/résistance et confluence

## 🚀 Installation et Utilisation

### 1. Import dans TradingView
1. Ouvrir TradingView
2. Aller dans Pine Editor
3. Copier-coller le code d'un fichier `.pine`
4. Cliquer sur "Add to Chart"

### 2. Configuration Recommandée
- **Timeframe principal**: 5m, 15m, 1h pour scalping/day trading
- **Instrument**: NQM2024 ou MNQ futures
- **Session**: 9h30-16h00 EST (marché US)

## 📈 Stratégie Principale (mnq_strategy_main.pine)

### Paramètres Configurables
- **Trend Analysis**: EMA rapide/lente, ATR multiplier
- **Momentum**: RSI periods et seuils
- **Volume**: Détection de spikes de volume
- **Risk Management**: Stop loss et take profit en ATR
- **Session**: Filtre horaire pour éviter les heures creuses

### Signaux d'Entrée
- **Long**: Trend haussier + RSI oversold bounce + spike de volume
- **Short**: Trend baissier + RSI overbought drop + spike de volume

### Gestion des Risques
- Stop loss et take profit basés sur l'ATR
- Limite du nombre de trades par jour
- Filtre de session pour éviter les heures de faible liquidité

## 🔍 Indicateurs d'Analyse

### Trend Analyzer
- Analyse multi-timeframe de la tendance
- Moyennes mobiles configurables (SMA/EMA/WMA/HMA)
- Force de tendance avec ADX
- Signaux de changement de tendance

### Momentum Oscillators
- RSI avec détection de divergences
- Stochastic pour timing d'entrée
- MACD pour confirmation de tendance
- Williams %R pour points de retournement
- Confluence de signaux pour forte probabilité

### Volume Analysis
- Analyse du volume vs moyenne
- On Balance Volume (OBV) pour confirmation
- VWAP avec bandes de déviation
- Détection d'épuisement des acheteurs/vendeurs

### Support & Resistance
- Détection automatique des pivots
- Niveaux de session et journaliers
- Retracements Fibonacci
- Zones de confluence pour points clés

## ⚙️ Paramètres Recommandés par Timeframe

### Scalping (1m-5m)
```
EMA Rapide: 5-9
EMA Lente: 13-21
RSI: 8-14
ATR Stop: 1.5-2.0
Volume Spike: 2.0-2.5x
```

### Day Trading (15m-1h)
```
EMA Rapide: 9-13
EMA Lente: 21-34
RSI: 14-21
ATR Stop: 2.0-3.0
Volume Spike: 1.5-2.0x
```

### Swing Trading (4h-1D)
```
EMA Rapide: 13-21
EMA Lente: 34-55
RSI: 21-34
ATR Stop: 3.0-4.0
Volume Spike: 1.2-1.8x
```

## 🔔 Alertes Configurées

Chaque indicateur inclut des alertes pour:
- Signaux d'entrée Long/Short
- Changements de tendance
- Breakouts de niveaux clés
- Divergences détectées
- Confluences importantes

## 📝 Notes Importantes

### Compatibilité
- ✅ Pine Script v5
- ✅ TradingView Premium/Pro/Pro+
- ✅ Compatible mobile et desktop

### Optimisation
- Code optimisé pour performance
- Inputs personnalisables sans recompilation
- Tables d'information en temps réel
- Gestion mémoire efficace

### Limitations
- Utilise uniquement des fonctions natives Pine Script
- Pas de fonctions externes ou bibliothèques tierces
- Respecte les limites TradingView (lignes, labels, etc.)

## 🎨 Personnalisation

### Couleurs et Styles
Tous les indicateurs permettent la personnalisation:
- Couleurs des lignes et zones
- Styles de tracé (ligne, histogramme, etc.)
- Taille des marqueurs de signaux
- Transparence des zones

### Affichage
- Tables d'information déplaçables
- Masquage sélectif des éléments
- Échelles multiples pour overlay

## ⚠️ Disclaimers

- **Risque**: Le trading de futures comporte des risques importants
- **Backtesting**: Toujours tester sur données historiques avant utilisation réelle
- **Capital**: Ne jamais risquer plus que ce que vous pouvez vous permettre de perdre
- **Education**: Ces outils sont à des fins éducatives et d'analyse

---

**Développé par**: Expert Pine Script v5/v6  
**Dernière mise à jour**: 2024  
**Support**: Code prêt à copier-coller, sans erreurs de compilation
