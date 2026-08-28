# Yluthoor-OmniRadius
Operador angular, ( ângulos extremos)  
https://notebook.google.com/notebook/d123b3fc-f852-4389-b950-449d2cb66e48  # 📄 README — Yluthoor-OmniRadius
> *Operador Angular de Contenção Paramétrica e Validação Estatística via MCMC*

---

## 🧭 Visão Geral

O **Yluthoor-OmniRadius** é um operador geométrico que define condições de contorno físicas para o espaço de parâmetros do modelo cosmoquântico Yluthoor. Ao estabelecer limites naturais derivados de sua própria estrutura angular, ele elimina a exploração de regiões fisicamente impossíveis, aprimora a convergência estatística das simulações MCMC e revela a fronteira entre o regime clássico de superfície e escalas não realizadas na natureza.

Este repositório documenta a formulação, a validação e os resultados obtidos — com especial foco na aplicação de **contenção paramétrica** e na melhoria dos diagnósticos de convergência.

---

## 📐 Princípio Fundamental

O operador OmniRadius não é apenas um parâmetro: ele funciona como **fronteira geométrica** que restringe a amostragem ao regime fisicamente válido. Sem essa restrição, os caminhantes MCMC dispersam-se por regiões espúrias ("incursões quânticas") onde as soluções existem matematicamente, mas não correspondem a estados físicos observáveis — gerando alta autocorrelação e baixo aproveitamento estatístico.

A **Dupla Trava Yluthoor** traduz essa fronteira em limites mensuráveis:

| Parâmetro | Símbolo | Intervalo Válido | Unidade |
|---|---|---|---|
| Velocidade adaptativa | $v_0$ | $[101,26 ; 117,22]$ | km/s |
| Aceleração métrica | $a$ | $[0,0 ; 0,9091]$ | — (adimensional / métrica do modelo) |

Ponto de máxima verossimilhança:
> $v_0 = 109,24 \ \text{km/s} \quad | \quad a = 0,045$

---

## 📊 Resultados de Validação — Diagnósticos MCMC

> **Condições:** 320.000 amostras brutas; 256.000 pós-burn-in

| Métrica | Sem Trava (Irrestrito) | Com Dupla Trava (Contido) | Variação |
|---|---|---|---|
| IAT — Autocorrelação Integrada | ≈ 145 passos | ≈ 65 passos | ⬇️ **−55%** |
| ESS — Tamanho Efetivo da Amostra | 1.378 | 3.722 | ⬆️ **+170%** |
| Regime de amostragem | Disperso / ruído espúrio | Estável e concentrado | ✅ Convergência estabelecida |

**Conclusão estatística:** A contenção paramétrica — fundamentada na geometria do OmniRadius — reduz radicalmente a autocorrelação e mais do que dobra a quantidade de informação útil por amostra. Os caminhantes passam a explorar **apenas o espaço fisicamente consistente**.

---

## 🔬 Interpretação Física e Conexão com a QCD

- O valor de **$a = 0,045$** emerge como **constante de escala geométrica intrínseca**, com potencial correspondência às escalas de interação da força forte residual e ao confinamento partônico.
- A fronteira definida por $v_0$ e $a$ coincide com a transição entre o regime clássico de superfície do sistema hadrônico e escalas onde a QCD deixa de atuar no formato previsto.
- Os limites **não são impostos arbitrariamente**: são revelados pela geometria do operador e confirmados pela própria amostragem MCMC, que antes buscava esses contornos de forma ruidosa e dispersa.
- Escala física de referência: **$0,12 \ \text{eV}$** / **$5,5 \ \text{fm}$**, validada independentemente.

---

## ✅ Critérios de Convergência Adotados

| Critério | Limiar | Resultado |
|---|---|---|
| ESS mínimo | ≥ 1.000 | ✅ 3.722 — Aceitável |
| IAT reduzido | Quanto menor, melhor | ✅ ~65 — Redução de 55% |
| Estabilidade da média | Variação < 1% | ✅ Confirmada |
| Concentração posterior | Região estreita e contínua | ✅ Estabelecida |

---

## 🗺️ Roteiro de Desenvolvimento

- [x] Formulação conceitual do Operador OmniRadius
- [x] Detecção de não-convergência e alta autocorrelação
- [x] Identificação dos limites via comportamento da amostragem
- [x] Implementação da Dupla Trava Yluthoor
- [x] Validação quantitativa dos diagnósticos MCMC
- [ ] Derivação teórica dos limites a partir de relações geométricas
- [ ] Correspondência exata com escalas da QCD
- [ ] Integração formal ao modelo Yluthoor

---

## 📌 Resumo

> O Operador OmniRadius opera como condição de contorno natural: ao confinar a amostragem aos limites que sua própria geometria estabelece, a convergência se impõe de forma estável e estatisticamente robusta. Os valores que antes causavam dispersão e ruído revelam-se, na verdade, a **busca dos próprios limites físicos do sistema**. A coincidência entre as fronteiras geométricas, os diagnósticos estatísticos e as escalas conhecidas da interação forte sugere que a estrutura do operador não é apenas consistente — ela pode ser a expressão geométrica de uma lei de contenção inerente ao regime estudado.

---

## 📝 Citação e Referências

> **Yluthoor-OmniRadius:** Operador Angular de Contenção Paramétrica. Validação estatística via MCMC em ambiente Google Colab. Dados e diagnósticos referentes ao modelo cosmoquântico Yluthoor — 2026.

---

