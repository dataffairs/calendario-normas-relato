# Calendário das normas de relato de sustentabilidade

O calendário das normas de relato de sustentabilidade em português: quando cada norma passou por consulta pública, quando foi aprovada, quando é lançada e a partir de quando é obrigatória. Cada data aponta para a fonte oficial de onde saiu.

Mantido pela [Dataffairs](https://www.dataffairs.com/?utm_source=github), consultoria especializada em sustentabilidade, ESG e comunicação de resultados corporativos.

## O que está no calendário hoje

As três Normas Setoriais da GRI para serviços financeiros:

| Norma | Para quem | Aprovação pelo GSSB | Lançamento | Vigência |
|---|---|---|---|---|
| GRI 16: Setor Bancário | banco de varejo, comercial, corporativo e de investimento | 17/09/2026 | 2027 | relatos publicados a partir de 01/01/2029 |
| GRI 17: Mercado de Capitais | titularidade, gestão de ativos e de patrimônio, custódia e consultoria de investimentos | 17/09/2026 | 2027 | relatos publicados a partir de 01/01/2029 |
| GRI 18: Setor de Seguros | seguro de vida, seguros gerais, resseguro, corretores e agentes | 17/09/2026 | 2027 | relatos publicados a partir de 01/01/2029 |

A consulta pública das minutas das três normas foi de 05/03/2025 a 31/05/2025.

Veja a leitura completa no artigo [GRI 16, 17 e 18: o setor financeiro passa a integrar o sistema de normas da GRI](https://www.dataffairs.com/conteudos/gri-16-17-e-18-normas-setoriais-servicos-financeiros?utm_source=github): a quem cada norma se aplica, os temas do setor e um plano de ação até 2029.

## Como ler as datas

- **Consulta pública**: a minuta recebe comentários. Minuta não é norma, e o texto final pode mudar.
- **Aprovação**: o órgão emissor aprova o texto final. Na GRI é o GSSB, órgão independente responsável pela elaboração das Normas GRI; no ISSB, o próprio conselho da IFRS Foundation; nas ESRS, a Comissão Europeia, a partir da proposta da EFRAG.
- **Vigência**: a data a partir da qual a norma é obrigatória para quem relata em conformidade com as Normas GRI. Ela vale pela data de publicação do relatório, e não pelo exercício relatado. Na prática, o relatório do ano fiscal de 2028, se publicado em 2029, já precisa seguir a GRI 16, 17 ou 18.

Até a vigência, o uso é voluntário.

## Como usar

Abra o [`calendario.csv`](calendario.csv) numa planilha ou leia direto no código. O arquivo é UTF-8, separado por vírgula, com uma linha por norma.

| Coluna | O que traz |
|---|---|
| `referencial` | a família de normas: `GRI`, `ISSB`, `ESRS`, `CVM` |
| `orgao_emissor` | quem publica e aprova a norma (GSSB na GRI, ISSB na IFRS Foundation, EFRAG e Comissão Europeia nas ESRS, CVM e CBPS no Brasil) |
| `tipo` | `universal`, `setorial`, `temática` ou `regulação` |
| `abrangencia` | onde vale: `global`, `União Europeia`, `Brasil` |
| `norma` | o código da norma |
| `nome_oficial` | o nome oficial, como o órgão emissor publica |
| `nome_em_portugues` | o nome em português |
| `setor` | as atividades cobertas |
| `consulta_publica` | o período da consulta pública, `AAAA-MM-DD a AAAA-MM-DD` |
| `aprovacao` | a data de aprovação pelo órgão emissor, `AAAA-MM-DD` |
| `lancamento` | o ano do lançamento global |
| `vigencia` | a data a partir da qual a norma é obrigatória, `AAAA-MM-DD` |
| `fonte_oficial_aprovacao` | a página oficial que traz a consulta, a aprovação e o lançamento |
| `fonte_oficial_vigencia` | o texto oficial da norma, que traz a vigência |
| `artigo_dataffairs` | o artigo da Dataffairs sobre a norma |

Exemplo em Python:

```python
import csv

with open("calendario.csv", encoding="utf-8") as arquivo:
    for linha in csv.DictReader(arquivo):
        print(linha["norma"], "obrigatória a partir de", linha["vigencia"])
```

## Fonte de cada data

| Data | Fonte oficial |
|---|---|
| Consulta pública, de 05/03/2025 a 31/05/2025 | [página do projeto na GRI](https://www.globalreporting.org/standards/standards-development/standards-for-banking-capital-markets-and-insurance/) |
| Aprovação pelo GSSB em 17/09/2026 | [página do projeto na GRI](https://www.globalreporting.org/standards/standards-development/standards-for-banking-capital-markets-and-insurance/) e [reuniões do GSSB](https://www.globalreporting.org/standards/global-sustainability-standards-board/gssb-meetings/) |
| Lançamento global em 2027 | [página do projeto na GRI](https://www.globalreporting.org/standards/standards-development/standards-for-banking-capital-markets-and-insurance/) |
| Vigência em 01/01/2029 | texto aprovado de cada norma: [GRI 16](https://www.globalreporting.org/media/3brfirew/gri-16-banking-sector-2027-1.pdf), [GRI 17](https://www.globalreporting.org/media/ncmfw2xh/gri-17-capital-markets-sector-2027.pdf) e [GRI 18](https://www.globalreporting.org/media/s5tb5d45/gri-18-insurance-sector-2027.pdf) |

Datas consultadas em novembro de 2026. As datas de um projeto de norma podem mudar: confira a fonte oficial antes de fechar o seu plano.

## Encontrou uma data errada ou desatualizada?

Abra uma issue com a data e o link da fonte oficial. Só entra no calendário data com fonte.

## Para ir além

- Faça o [Diagnóstico ESG gratuito](https://www.dataffairs.com/diagnostico-esg?origem=github) e veja em que estágio de maturidade ESG está a sua empresa.
- Capacite a equipe no curso [Relatórios de Sustentabilidade e ESG](https://www.dataffairs.com/treinamentos/relatorios-de-sustentabilidade-e-esg?utm_source=github), que percorre o sistema GRI, das Normas Universais às Setoriais.
- Conheça a [consultoria em relatórios de sustentabilidade](https://www.dataffairs.com/servicos/relatorios-de-sustentabilidade?utm_source=github).

## Licença

O conteúdo deste repositório está sob a licença [Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)](LICENSE). Use, copie e adapte, inclusive para fins comerciais, citando: **"Calendário das normas de relato de sustentabilidade, Dataffairs (https://www.dataffairs.com)"**.

Os textos das normas são da Global Reporting Initiative e não estão neste repositório: aqui ficam só as datas e os links para as fontes oficiais.
