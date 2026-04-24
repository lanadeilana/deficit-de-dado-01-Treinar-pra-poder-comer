# Déficit de Dado — Edição 001
## Treinar pra poder comer: a relação das mulheres BR com exercício e culpa

> Análise de dados por trás da newsletter **Déficit de Dado**  
> por [@lanadeilana](https://substack.com/@lanadeilana)

📖 **Leia o artigo completo:** [Substack — Déficit de Dado, Ed. 001](https://substack.com/@lanadeilana)  
💼 **LinkedIn:** [/lanadeilana](https://linkedin.com/in/lanadeilana)

---

## O que este repositório contém

Três notebooks Python que sustentam a análise publicada na edição 001 da newsletter **Déficit de Dado** — sobre a relação das mulheres brasileiras com exercício, comida e culpa, e o mercado que lucra com isso.

| Notebook | O que analisa | Fontes |
|---|---|---|
| `01_mercado_fitness_brasil.ipynb` | Crescimento do setor fitness BR 2019–2024, faturamento, perfil de praticantes | Panorama Setorial Fitness Brasil 2024, InvestNews, Nuvemshop |
| `02_transtornos_alimentares_genero.ipynb` | Prevalência de transtornos alimentares no BR com recorte de gênero | OMS, Câmara dos Deputados, SciELO, RBNE |
| `03_google_trends_culpa_fitness.ipynb` | Análise de buscas brasileiras sobre compensação alimentar e culpa fitness (2019–2024) via pytrends | Google Trends |

---

## Como rodar localmente

```bash
# Clone o repositório
git clone https://github.com/lanadeilana/deficit-de-dado
cd deficit-de-dado

# Instale as dependências
pip install pandas matplotlib seaborn plotly pytrends

# Abra os notebooks
jupyter notebook
```

> **Nota sobre pytrends:** o Google Trends tem rate limit. Se receber erro 429,  
> aguarde ~60 segundos entre requisições. Os dados coletados em CSV estão  
> disponíveis na pasta `/dados` para reprodutibilidade sem nova coleta.

---

## Dados chave da análise

| Métrica | Valor | Fonte |
|---|---|---|
| Faturamento do setor fitness BR (2024) | R$ 17 bilhões | Panorama Setorial 2024 |
| Crescimento do setor (2019–2024) | +44% | InvestNews |
| Número de academias no Brasil | 57 mil (2º do mundo) | Fitness Brasil / Health & Fitness Association |
| Brasileiros matriculados em academias | 4,9% da população | Panorama Setorial 2024 |
| Praticantes que são mulheres | 38% | Panorama Setorial 2024 |
| Mulheres BR com compulsão alimentar | ~13% | OMS |
| Diagnósticos de transtornos alimentares: mulheres | 90% | Câmara dos Deputados (USP/2023) |
| Total estimado de pessoas com TA no Brasil | 15 milhões | Prof. Táki Cordás / USP |
| Crescimento em vendas de creatina (2024) | +346% | Nuvemshop |

---

## Metodologia

- Dados quantitativos de faturamento e mercado: coletados manualmente a partir de relatórios públicos setoriais, com fonte citada em cada célula
- Dados de saúde: fontes acadêmicas (SciELO) e institucionais (OMS, Câmara dos Deputados)
- Google Trends: índices relativos via pytrends — representam interesse relativo (0–100), não volumes absolutos
- Todas as limitações metodológicas estão documentadas no notebook 02

**Nenhum dado foi fabricado. Toda correlação apresentada é acompanhada de ressalva sobre causalidade.**

---

## Estrutura do repositório

```
deficit-de-dado-ed001/
│
├── 01_mercado_fitness_brasil.ipynb
├── 02_transtornos_alimentares_genero.ipynb  
├── 03_google_trends_culpa_fitness.ipynb
│
├── dados/
│   ├── dados_trends_culpa_fitness.csv      # gerado pelo nb 03
│   └── dados_trends_dieta_transtornos.csv  # gerado pelo nb 03
│
├── figuras/
│   ├── fig01_mercado_fitness.png
│   ├── fig02_perfil_praticantes.png
│   ├── fig03_suplementos.png
│   ├── fig04_transtornos_genero.png
│   ├── fig05_crescimento_paralelo.png
│   ├── fig06_trends_culpa_fitness.png
│   └── fig07_sazonalidade.png
│
└── README.md
```

---

## Sobre o projeto

**Déficit de Dado** é uma newsletter de análise de dados sobre corpo, comportamento e o que ninguém mede no Brasil.

Cada edição combina dado público + análise original + narrativa sem moralismo.  
O repositório GitHub é parte do portfólio — toda análise é reprodutível.

---

## Licença

Código disponível sob licença MIT.  
Os dados de terceiros pertencem às respectivas fontes — veja citações nos notebooks.
