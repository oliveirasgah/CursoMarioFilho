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
- __Como essa solução será usada em produção?__
    - Através de um web app
- __Como eu vou saber que deu certo?__
    - Uso de métricas

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
- Exemplo de métrica secundária: quanto tempo eu passo selecionando vídeos
    - Não serão implementadas métricas secundárias

### 1.2 Como escolher um problema para resolver
- Perguntas
    - Como escolher o problema para trabalhar?
    - Quais são os seus interesses?
    - O quão fácil é achar dados para a sua solução?
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
        - Previsão de acessos
        - Previsão de cancelamento
- Projetos interessantes pessoais
    - Verificar quais são os meus interesses
    - Mantém a motivação para continuar os estudos
- Complexidade para obtenção de dados para a solução
    - De preferência, buscar datasets prontos
    - Caso não haja, será preciso encontrar __fontes de informação__
        - É importante fazer uma lista de fontes de informação ideais
            - Uma suposta fonte que possuísse exatamente os dados que gostaríamos de ter
            - A partir disso, selecionar as fontes de dados mais interessantes
    - Mínimo de dados precisos
        - No caso do projeto do curso, características dos vídeos (de preferência, o título) e label

## 2. Prepare os Dados
### 2.1 Criando o coletor da página de busca do YouTube
- O objetivo é obter todos os dados necessários para a realização do projeto
- De preferência, realizar versionamento dos dados que estão sendo usados
- É possível buscar formas de paginação no YouTube online

#### 2.7 Criando as primeiras features
- Precision
    - _"De todos os exemplos que o meu modelo diz
    que são positivos, quantos ele realmente acertou?"_
- Recall
    - _"De todos os exemplos que são realmente positivos, quantos o meu modelo previu como
    positivos?"_

#### 2.9 Active Learning e adicionando features de texto do título
- Active Learning
    - Quando utilizar?
        - Quando há um orçamento muito pequeno
            - É muito caro fazer anotações em novos exemplos
        - Há pouco tempo para fazer anotações em novos exemplos
            - Ao invés de realizar as anotações aleatóriamente, as anotações são realizadas em um conjunto específico de exemplos que nos tragam muito mais ganho nas anotações
        - Exemplo: dados médicos
            - É necessário ter um corpo de especialistas para analisar novos exemplos, o que pode se tornar uma tarefa custosa e pode demorar um tempo
    