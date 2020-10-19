# Projeto de Data Science
## 1. Defina o Problema 
### 1.1 Traduzindo a ideia para a linguagem de data science
- É necessário saber traduzir o problema de negócios para um problema que possamos resolver com dados.
- É preciso conhecer o problema que devemos resolver, pois é possível se passar semanas resolvendo o problema errado.
#### Definição do problema
- __Qual é o problema?__
    - Gasto muito tempo buscando novos vídeos no YouTube.
- __Qual a solução ideal?__
    - Ter uma lista apenas dos vídeos que eu, com certeza, vou gostar.
- __Como eu posso fazer isso com Data Science/ML?__
    - Criar uma solução de recomendação de vídeos.

#### Possíveis abordagens
- Ponto de corte
    - Retornar apenas top N
- Ranking
    - Ordene os vídeos mais interessantes primeiro

#### Uso da solução em produção
- Web App
    - Possui os links para os vídeos
    - Possui as previsões ordenadas

#### Métricas
- Grande subjetividade
    - O usuário pode gostar ou não dos vídeos
- Tipos de métricas
    - Primária
        - Métrica principal para avaliação da solução
        - É única em todo o projeto, não há mais de uma métrica primária
    - Secundária
        - Utilizada para dar apoio à métrica primária
        - Podem haver diversas métricas secundárias em um projeto
- Possível métrica primária: quantos vídeos entre os top N recomendados eu assisti até o final
    - Os top N recomendados são mais assistidos do que os top N na recomendação do YouTube
    - Não é muito boa
        - Sujeito a preferência do usuário no momento de escolha dos vídeos
        - O usuário pode decidir não assistir a um vídeo no momento
- Métrica primária: dos top N vídeos, quantos eu coloco na lista de Watch Later
- Métrica(s) secundária(s): quanto tempo eu passo selecionando vídeos
    - Não serão implementadas métricas secundárias

### 1.2 Como escolher um problema para resolver
- É importante escolher projetos que sejam simples
    - Projetos complicados podem demorar muito e pode não ser possível entregar valor para a empresa
    - Dessa forma, é importante ter pequenas vitórias
    - Projetos simples são projetos que já tenham sido resolvidos por outras pessoas
- Projetos interessantes para empresas
    - Recomendação
        - Aumento de vendas
        - Marketing
    - Time series
        - Previsão de demanda
        - Previsão de cancelamento
- Projetos interessantes pessoais
    - Verificar quais são os meus interesses
    - Mantém a motivação para continuar os estudos
- Complexidade para obtenção de dados para a solução
    - De preferência, buscar datasets prontos
    - Caso não haja, será preciso encontrar fontes de informação
        - É importante fazer uma lista de fontes de informação ideais
    - Mínimo de dados precisos
        - No caso do projeto do curso, características dos vídeos e label

## 2. Prepare os Dados
### 2.1 Criando o coletor da página de busca do YouTube
- O objetivo é obter todos os dados necessários para a realização do projeto
- De preferência, realizar versionamento dos dados que estão sendo usados
- É possível buscar formas de paginação no YouTube online