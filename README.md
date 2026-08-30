# 🦉 StatFly

[![Electron](https://img.shields.io/badge/Electron-31.1-47848F?logo=electron&logoColor=white)](https://www.electronjs.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.5-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.3-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Bun](https://img.shields.io/badge/Bun-1.1-000000?logo=bun&logoColor=white)](https://bun.sh/)
[![Vitest](https://img.shields.io/badge/Vitest-2.1-6E9F18?logo=vitest&logoColor=white)](https://vitest.dev/)
[![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)](#-distribuição)
[![License](https://img.shields.io/badge/License-MIT-green)](#-licença)

**Jogo educativo de Estatística inspirado em Flappy Bird** — Electron + Bun + TypeScript + React.

Voe com *Statzinho*, a coruja-estudante, desvie de obstáculos e responda perguntas de Estatística de múltipla escolha. Cada colisão pausa o jogo e abre uma questão; errar pode custar vidas, acertar rende pontos, combos e XP.

> Desenvolvido por **Erick de S.C. Araújo**

---

## 🎮 Visão geral

- **51 fases** na Campanha (0–50), **1 pergunta por fase**, com dificuldade por bloco:
  - Fases **0–9**: básico · **10–24**: intermediário · **25–39**: avançado · **40–50**: difícil
- **Banco de 259 questões**:
  - 80 básicas · 80 intermediárias · 60 avançadas · 39 difíceis
  - Cobre: estatística descritiva, probabilidade, distribuições, amostragem, inferência, testes de hipóteses, correlação, regressão, ANOVA e estatística bayesiana
- **Sem repetição na mesma partida** · questões erradas vão para o modo **Revisão**
- **Dificuldade adaptativa**: sobe um nível com ≥ 80% de acerto e desce com ≤ 40%, priorizando seus tópicos mais fracos
- **Explicação após cada resposta**
- Sistemas de **vidas, pontuação, combos, progressão, XP e níveis**
- **Perfil do jogador** com estatísticas por tópico/dificuldade, gráficos (SVG, offline), histórico e **16 conquistas**
- **Recomendações de estudo** baseadas em erros e desempenho
- **Salvamento local** (localStorage), **100% offline**, efeitos sonoros sintetizados (Web Audio API, opcionais)
- **Acessibilidade**: navegação por teclado, foco visível, `aria-live`, redução de animações e alto contraste

## 🕹️ Modos de jogo

| Modo | Descrição |
| --- | --- |
| 🗺️ **Campanha** | 51 fases progressivas, uma pergunta por fase, 3 vidas e estrelas |
| 🎯 **Treino** | Voo livre com tópico escolhido, sem perda de vidas |
| 📚 **Revisão** | Quiz com as questões que você errou (acertar "resolve" o item) |
| ⚡ **Desafio** | Voo com velocidade crescente e vidas limitadas |
| ♾️ **Infinito** | Voo sem fim, sem perder vidas, dificuldade progressiva |
| 🎓 **Exame** | 20 questões (5 por dificuldade), 30 minutos, nota de 0 a 100 |

## 🎹 Controles

- **Espaço / ↑ / W / clique** — voar
- **P** — pausar · **M** — ligar/desligar som
- Alternativas: clique ou **setas + Enter**

Cobrem: integridade das 259 questões, seletores (sem repetição em campanha de 51 fases, exame com 20 questões únicas), física do motor (gravidade, voo, colisão, meta, chão), pontuação/XP/níveis/estrelas, conquistas e recomendações de estudo.

## 📦 Distribuição

- **Electron** com `contextIsolation: true` e `sandbox: true` (renderer sem acesso ao Node); menu padrão (File/Edit/View/Window) removido — no macOS é mantido o menu mínimo da plataforma.
- O jogo roda inteiramente **offline**; não há servidor nem telemetria.
- Saves ficam no `localStorage` do perfil do Electron (`userData`).

## 📄 Licença

MIT © 2024 Erick de S.C. Araújo
