# FuzzyMIP Prioritizer

Plataforma computacional para priorizacao fuzzy de acoes estrategicas, combinando logica fuzzy e matriz de Impacto e Probabilidade.

## Proposito

O FuzzyMIP Prioritizer apoia a classificacao e o ranqueamento de acoes, ameacas e oportunidades a partir de tres componentes:

- impacto fuzzy no negocio;
- probabilidade fuzzy de ocorrencia;
- qualidade da evidencia utilizada na avaliacao.

O indice principal e calculado por:

```text
Indice I/P = Impacto fuzzy x Probabilidade fuzzy
Indice ajustado = Indice I/P x Fator de evidencia
```

## Estrutura metodologica

A ferramenta separa a leitura decisoria de ameacas e oportunidades:

- ameacas sao interpretadas como risco e orientam acoes de mitigacao;
- oportunidades sao interpretadas como potencial estrategico e orientam acoes de captura de valor.

Para evitar falsa precisao, o usuario informa a base da avaliacao:

- dado real / mensurado;
- estimativa fundamentada;
- percepcao preliminar;
- baixa evidencia.

Essa informacao aplica um fator de abatimento ao indice, permitindo que avaliacoes pouco sustentadas nao tenham o mesmo peso de dados mensurados.

## Como executar localmente

```bash
pip install -r requirements.txt
streamlit run fuzzyip_app.py
```

## Arquivos principais

- `fuzzyip_app.py`: interface Streamlit.
- `fuzzyip/core.py`: calculos fuzzy, ranking e estatisticas.
- `fuzzyip/report.py`: geracao do relatorio PDF.
- `assets/`: logomarcas institucionais e links de perfil.

## Autor

Desenvolvido por David de Oliveira Costa, Doutorando em Engenharia de Computacao, 2026.

## Projeto paralelo: FuzzyMIP com boxplot horizontal

Esta versão mantém o fluxo principal do FuzzyMIP e substitui o card de média I/P por um boxplot horizontal compacto, sem escala visível. O objetivo é evidenciar, na própria faixa de indicadores, se as ações avaliadas apresentam pontuações próximas entre si ou se alguma ação se destaca como mais crítica ou prioritária.
