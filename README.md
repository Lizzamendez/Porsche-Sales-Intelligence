Porsche Sales Intelligence
Dados de vendas transformados em leitura comercial
Dashboard interativo desenvolvido como projeto prático do bootcamp Reclame AQUI — Dados e IA na Prática, da DIO. O projeto demonstra como preparar uma base sanitizada, formular perguntas de negócio e usar visualização e IA para transformar dados em informações mais fáceis de interpretar.
Publicação: antes da entrega, substitua os campos de URL abaixo pelos endereços reais do seu repositório e da dashboard publicada. Não envie o README com os campos de exemplo.

- Dashboard publicada: https://lizzamendez.github.io/Porsche-Sales-Intelligence/
- Repositório público: https://github.com/Lizzamendez/Porsche-Sales-Intelligence
1. Objetivo do projeto
Criar uma dashboard web que permita explorar dados de vendas de veículos Porsche por modelo, localização, ano do modelo, forma de pagamento e situação da entrega. A interface foi pensada para leitura progressiva: primeiro os indicadores principais, depois os insights e, por fim, os gráficos que permitem investigar os detalhes.

O projeto conecta as etapas trabalhadas no bootcamp:

preparação da base → perguntas de negócio → análise → dashboard → interpretação → apoio à decisão
2. Perguntas de negócio
As três perguntas foram escolhidas para analisar dimensões complementares da operação comercial: valor gerado, distribuição geográfica e comportamento de pagamento.
01 — Onde está concentrada a receita?
Visualização: ranking de receita por modelo.

Por que importa: permite identificar quais modelos representam maior contribuição para a receita total do recorte e comparar essa contribuição entre modelos. Pode orientar investigações posteriores sobre mix comercial, campanhas e planejamento de estoque.

Como interpretar: receita total não é o mesmo que quantidade vendida, ticket médio ou margem de lucro. A base não contém custos, portanto não é possível calcular rentabilidade.
02 — Onde as vendas acontecem?
Visualização: ranking dos estados com maior quantidade de vendas.

Por que importa: mostra em quais mercados os registros de venda estão concentrados e ajuda a levantar perguntas para uma análise comercial regional.

Como interpretar: o ranking considera volume de vendas, não receita, população, participação de mercado ou rentabilidade de cada estado.
03 — Como as vendas são pagas?
Visualização: distribuição das vendas por forma de pagamento.

Por que importa: ajuda a compreender o mix de pagamento observado na base e pode apoiar análises operacionais sobre os tipos de transação.

Como interpretar: a frequência de uma forma de pagamento não indica, por si só, satisfação do cliente, preferência de toda a clientela ou qualidade da experiência.
Indicadores de acompanhamento
- Vendas: quantidade de registros no recorte selecionado.
- Receita: soma dos valores de venda.
- Ticket médio: receita dividida pela quantidade de registros considerados.
- Modelo líder: destaque de modelo conforme o indicador exibido na dashboard.
Os filtros de modelo, estado, cidade, ano do modelo, forma de pagamento e situação da entrega atualizam os indicadores e as visualizações. A leitura executiva acompanha o recorte selecionado.
3. Prompt usado para criar a dashboard
O desenvolvimento foi feito com ChatGPT, por meio de uma conversa iterativa. O prompt abaixo resume a solicitação inicial usada para orientar a solução; as alterações posteriores foram feitas em etapas, após observar o resultado no navegador e identificar pontos de melhoria.
Prompt-base
Crie uma dashboard interativa de vendas Porsche usando HTML, CSS e JavaScript, adequada para publicação como site estático no GitHub Pages. Use apenas a base sanitizada fornecida. Inclua filtros por modelo, estado, cidade, ano do modelo, forma de pagamento e situação da entrega; indicadores de vendas, receita, ticket médio e modelo líder; e visualizações para responder a estas perguntas: “Onde está concentrada a receita?”, “Onde as vendas acontecem?” e “Como as vendas são pagas?”. Faça os filtros atualizarem os KPIs, os gráficos e a leitura executiva. Desenvolva uma identidade visual premium, inspirada na Porsche, com hierarquia clara, leitura progressiva, textos legíveis e boa acessibilidade visual. Inclua modo claro e modo escuro com contraste adequado. Diferencie receita de volume de vendas e não invente métricas de experiência do cliente que não existam na base. Organize o projeto em index.html, css/styles.css, js/dashboard.js e README.md.

Evolução do prompt até a versão final
O primeiro resultado foi refinado com instruções adicionais em linguagem natural. As principais mudanças foram:
1. Legibilidade e identidade visual: criar os modos claro e escuro, reforçar o contraste de textos, eixos, legendas e barras e manter o vermelho Porsche como destaque, sem preencher todos os gráficos de vermelho.
2. Gráficos mais interpretáveis: ordenar a receita por modelo, limitar o ranking principal aos dez primeiros e separar os demais modelos do ranking; melhorar o contraste do gráfico por estado e deixar as legendas de pagamento mais claras.
3. Hierarquia dos indicadores: dar mais destaque aos KPIs, reduzir textos secundários e separar visualmente resumo executivo, insights e análise detalhada.
4. Insights mais objetivos: transformar parágrafos longos em observações curtas, com métricas importantes em evidência e textos atualizados conforme os filtros.
5. Conclusão executiva: acrescentar uma síntese final para leitura rápida, sem misturar receita, volume de vendas e outras métricas diferentes.
6. Responsabilidade analítica: explicitar o que a base não permite concluir, especialmente sobre satisfação, NPS, percepção da marca e sentimento do cliente.
O resultado final não foi obtido com um único prompt: foi construído em ciclos de geração, inspeção, identificação de problemas e refinamento.
4. Tratamento da base antes de usar a IA
A planilha disponibilizada para o desafio já continha campos sanitizados. Antes de incorporar os dados ao dashboard, foi necessário organizar os campos e garantir que os valores pudessem ser analisados corretamente.
- Foram usados os campos sanitizados relacionados a data da venda, modelo, ano do modelo, preço, quilometragem, forma de pagamento, cidade, estado e situação da entrega.
- Os campos foram organizados em nomes consistentes no código: sale_date, model, model_year, sale_price, mileage, payment_method, city, state e delivery_status.
- Preço e ano do modelo foram tratados como valores numéricos para permitir agregações e filtros.
- Datas inválidas ou ausentes foram representadas como nulas; elas não foram convertidas em datas fictícias.
- Os dados necessários foram incorporados ao JavaScript para que a dashboard pudesse funcionar como site estático, sem depender de uma API ou de uma leitura externa de CSV.
- Os nomes originais de modelos, cidades, estados e categorias da base foram preservados na camada de dados. Os textos da interface foram adaptados para português brasileiro quando aplicável.
A base contém 100 registros. A soma dos valores de venda é de aproximadamente US$ 12,83 milhões; os indicadores exibidos podem mudar conforme os filtros aplicados. A moeda foi mantida em dólares porque os valores da base original estão em USD.

Privacidade e escopo: o projeto utiliza a base sanitizada fornecida para o desafio. Antes de publicar, confira se o repositório não contém a planilha original ou qualquer arquivo com dados pessoais ou não sanitizados.
5. Ferramenta de IA utilizada
- ChatGPT: utilizado diretamente na conversa para planejar, gerar e refinar a estrutura, os textos, a apresentação visual e o código do projeto.
- Canvas: não foi usado como ferramenta de execução nesta versão.
- Agente com skill: não foi utilizado.
Essa descrição registra o fluxo realmente adotado, sem atribuir ao projeto ferramentas que não fizeram parte do desenvolvimento.
6. Tecnologias e estrutura
- HTML5 — estrutura da página.
- CSS3 — identidade visual, responsividade e temas claro/escuro.
- JavaScript — filtros, cálculos, insights e atualização dos gráficos.
- Chart.js — renderização das visualizações.
- GitHub Pages — hospedagem estática da dashboard.
porsche-sales-intelligence/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── dashboard.js
└── README.md
7. Como executar e testar
1. Clone ou baixe o repositório.
2. Abra index.html em um navegador com acesso à internet, pois o Chart.js é carregado por CDN.
3. Altere os filtros e confirme que os KPIs, gráficos e insights acompanham o recorte selecionado.
4. Alterne entre modo claro e escuro e confira a legibilidade dos rótulos, eixos e legendas.
5. Teste também a página publicada pelo GitHub Pages, não apenas a cópia local.
8. Publicação no GitHub Pages
1. Crie um repositório público na sua própria conta do GitHub. Um nome sugerido é porsche-sales-intelligence.
2. Envie index.html, a pasta css/, a pasta js/ e o README.md para a raiz do repositório.
3. Abra Settings → Pages.
4. Em Build and deployment, selecione publicação a partir de uma branch, escolha a branch principal (normalmente main) e a pasta / (root).
5. Salve e aguarde a conclusão da publicação.
6. Abra a URL fornecida pelo GitHub Pages e teste os filtros, os gráficos e os dois temas.
7. Substitua os campos abaixo pelas URLs reais antes de entregar o desafio.
   - URL da dashboard publicada: ADICIONE_A_URL_REAL_DO_GITHUB_PAGES
   - URL do repositório público: ADICIONE_A_URL_REAL_DO_REPOSITORIO
O endereço da dashboard deve apontar para o site publicado. O link enviado como repositório do projeto deve apontar para o repositório público na sua conta. Não invente nem mantenha URLs de exemplo na entrega final.

9. Evidências de funcionamento
Capturas de tela ajudam a demonstrar que o projeto foi publicado e que a interação funciona. Depois de criar as capturas, adicione-as ao repositório e use os caminhos correspondentes aqui.

Sugestão de estrutura:
screenshots/
├── dashboard-visao-geral.png
├── dashboard-filtro-aplicado.png
└── dashboard-modo-escuro.png
Recomendação para as evidências:
- Visão geral: dashboard publicada com os KPIs e os gráficos visíveis.
- Filtro aplicado: escolha um modelo ou estado e capture a atualização dos indicadores e gráficos.
- Modo escuro: mostre a legibilidade dos gráficos e das legendas no tema escuro.
Adicione as imagens apenas depois de salvá-las no repositório; não deixe referências a arquivos que ainda não existem.
10. Limites da análise e conexão com Customer Experience
Esta base permite analisar dimensões comerciais e alguns aspectos operacionais, mas não contém medidas diretas de NPS, CSAT, satisfação, percepção da marca, sentimento do cliente, Voice of Customer (VoC) ou reclamações. Por isso, o dashboard não afirma que um modelo, estado ou forma de pagamento gera uma experiência melhor.

Uma próxima etapa seria combinar os dados comerciais com pesquisas de satisfação, reclamações, dados de atendimento e indicadores de entrega. Essa integração permitiria investigar possíveis relações entre a operação e a experiência percebida, formulando hipóteses sem confundir correlação com causalidade.
11. Conclusão executiva
O Porsche Sales Intelligence transforma uma base sanitizada em uma experiência interativa de análise comercial. Os filtros permitem explorar diferentes recortes; os KPIs mostram a dimensão geral; os gráficos respondem às três perguntas de negócio; e as leituras executivas ajudam a identificar o que merece investigação.

O principal aprendizado demonstrado é o fluxo preparar dados → formular perguntas → analisar → comunicar insights → apoiar decisões, reconhecendo também os limites das informações disponíveis.
