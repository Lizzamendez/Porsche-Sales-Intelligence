# Porsche Sales Intelligence

Dashboard web desenvolvido como projeto do bootcamp **Reclame AQUI — Dados e IA na Prática (DIO)**.

## Objetivo

Transformar uma base sanitizada de vendas da Porsche em uma experiência de leitura comercial que vá além da visualização dos números: **dados → insight → decisão**.

O projeto foi pensado com leitura progressiva e hierarquia visual para que os principais sinais possam ser identificados rapidamente, sem depender da interpretação simultânea de muitos elementos.

## Perguntas de negócio

1. **Onde está concentrada a receita?** — identificar quais modelos representam maior valor comercial.
2. **Onde as vendas acontecem?** — observar a concentração geográfica da operação.
3. **Como as vendas são pagas?** — entender o mix de métodos de pagamento.

Além das perguntas, o dashboard apresenta uma **Leitura Executiva dinâmica**, que interpreta o recorte atual, e um **Pulso da Base**, que resume cobertura, concentração e sinais comerciais.

## Relação com o bootcamp

- **Excel / preparação de dados:** revisão e uso apenas das colunas sanitizadas.
- **Análise de dados:** KPIs, agregações, filtros e comparação entre dimensões.
- **Dashboards:** visualização interativa em HTML, com leitura progressiva.
- **IA e Engenharia de Prompt:** estrutura e refinamento da experiência foram orientados por prompts e iterações em linguagem natural.
- **Tomada de decisão:** os gráficos são acompanhados por interpretações e próximos olhares, conectando números a possíveis decisões.
- **Customer Experience:** o projeto evita inventar métricas de satisfação que não existem na base. O status de entrega é tratado como contexto operacional; uma análise de CX mais completa exigiria dados de NPS, CSAT, reclamações, avaliações ou VoC.

## Tratamento da base

A base original disponibilizada para o desafio foi trabalhada utilizando os campos sanitizados. Preços e anos foram tratados como valores numéricos e os dados utilizados no dashboard foram incorporados ao JavaScript para manter a publicação estática simples e compatível com GitHub Pages.

A base possui **100 registros** e receita total de aproximadamente **US$ 12,83 milhões**.

## Arquitetura

```text
porsche-sales-intelligence/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── dashboard.js
└── README.md
```

## Decisões de design

A interface foi construída para reduzir sobrecarga visual e favorecer a leitura em etapas:

1. **O que aconteceu?** — KPIs.
2. **Qual é o pulso da base?** — sinais rápidos.
3. **O que os dados estão dizendo?** — interpretação automática.
4. **Onde estão os detalhes?** — gráficos e filtros.
5. **O que ainda falta saber?** — conexão com CX e próximos dados necessários.

A identidade visual usa uma linguagem editorial, tipografia de alta hierarquia, bastante espaço negativo e poucos elementos de destaque.

## Publicação

Para publicar:

1. Criar um repositório público com nome legível e em minúsculas, por exemplo `porsche-sales-intelligence`.
2. Enviar `index.html`, a pasta `css`, a pasta `js` e este `README.md`.
3. Ativar GitHub Pages para a branch principal.
4. Testar o endereço publicado e todos os filtros.
5. Entregar no desafio o **link do repositório**, conforme orientação do desafio.

**Dashboard publicado:** adicionar a URL após a publicação.

## Prompt / uso de IA

A construção foi conduzida com uma abordagem iterativa: primeiro foi definida a necessidade de um dashboard comercial, depois foram estabelecidas perguntas de negócio, filtros, indicadores e linguagem visual. A partir do primeiro resultado, foram feitas melhorias em linguagem natural para reforçar legibilidade, interpretação e conexão com o conteúdo do bootcamp.

## Observação sobre CX

Este projeto não transforma dados de vendas em uma falsa métrica de satisfação. A leitura de Customer Experience é apresentada como uma oportunidade de enriquecimento: combinar vendas e operação com dados de VoC, NPS, CSAT, reclamações e avaliações permitiria investigar relações entre comportamento comercial, entrega e experiência percebida.


### Ajustes de legibilidade dos gráficos

- O gráfico de receita mostra os 10 modelos com maior receita e agrupa os demais em “Demais modelos”, evitando excesso de barras e uma grande massa vermelha.
- O gráfico de mercado destaca o estado líder em vermelho e usa barras neutras de alto contraste para os demais estados. A escala começa em zero e o texto auxiliar resume o principal resultado.
- Os textos da interface e as formas de pagamento/situações de entrega são apresentados em português brasileiro; nomes de modelos e siglas de estados permanecem como na base original.
- Cores dos gráficos e legendas se adaptam aos modos claro e escuro.
