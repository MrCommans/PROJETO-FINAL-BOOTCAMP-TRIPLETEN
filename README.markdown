# Projeto Final: Teste do Aplicativo Urban Scooter - TripleTen

## Visão Geral

Este projeto foi desenvolvido como o **Projeto Final do Bootcamp de Análise de QA da TripleTen**. O objetivo foi realizar testes abrangentes do aplicativo **Urban Scooter**, cobrindo sua interface web, aplicativo móvel e backend (API e banco de dados). O projeto foi dividido em três tarefas principais: testes manuais da interface web, testes do aplicativo móvel em um emulador Android e testes do backend via Postman e consultas SQL. Os resultados foram documentados em um arquivo do Google Sheets, com bugs registrados no Jira.

## Objetivos do Projeto

- **Tarefa 1 (Web)**: Testar o formulário "About Customer" da interface web do Urban Scooter, validando campos como nome e número de telefone em dois navegadores.
- **Tarefa 2 (Móvel)**: Testar as funcionalidades destacadas do aplicativo móvel Urban Scooter, incluindo layout e comportamento, em um emulador Android.
- **Tarefa 3 (Backend)**: Testar os endpoints da API para adicionar e excluir entregadores, além de verificar o banco de dados associado.
- **Documentação**: Registrar casos de teste, resultados e bugs em um arquivo do Google Sheets e no Jira, garantindo rastreabilidade e clareza.

## Metodologia

### Tarefa 1: Teste da Interface Web do Urban Scooter

1. **Análise de Requisitos**:
   - Estudei os requisitos do aplicativo web disponíveis no link fornecido e consultei os layouts no Figma para entender o formulário "About Customer" (título: "Para quem é a scooter").
   - Identifiquei os campos a serem testados: nome e número de telefone.

2. **Criação de Casos de Teste**:
   - Desenvolvi casos de teste positivos (ex.: nome válido, número de telefone no formato correto) e negativos (ex.: campos vazios, número inválido) para o formulário "About Customer".
   - Registrei os casos na aba correspondente do modelo do Google Sheets.

3. **Execução de Testes**:
   - Realizei os testes em dois navegadores:
     - **Google Chrome** (versão 85 ou superior, resolução 1280x720)
     - **Opera** (versão 71 ou superior, resolução 1280x720)
   - Marquei os resultados como APROVADO ou REPROVADO na planilha.
   - Para testes reprovados, criei relatórios de bugs no Jira, incluindo título, etapas, resultado esperado, resultado real e prioridade (Bloqueador, Crítico, Grande, Pequeno ou Trivial).
   - Vinculei os IDs dos relatórios de bugs à coluna correspondente no Google Sheets.

### Tarefa 2: Teste do Aplicativo Móvel Urban Scooter

1. **Preparação do Ambiente**:
   - Iniciei o servidor do Urban Scooter para obter a URL de acesso.
   - Baixei o APK do aplicativo móvel Urban Scooter e instalei no emulador **Android Studio** (Pixel 5, Android 31).
   - Configurei o aplicativo inserindo a URL da API no campo fornecido (ícone "?" na tela inicial).
   - Criei um entregador via API POST, conforme documentação no `URL+/docs/pt/`, enviando os parâmetros no formato JSON.

2. **Análise de Requisitos**:
   - Estudei os requisitos do aplicativo móvel, focando nas funcionalidades destacadas em amarelo.
   - Consultei os designs no Figma para validar o layout.

3. **Criação de Casos de Teste**:
   - Desenvolvi casos de teste para as funcionalidades destacadas, cobrindo layout (ex.: disposição de elementos, ortografia) e comportamento (ex.: interação com funcionalidades específicas).
   - Incluí cenários positivos e negativos, registrados na aba correspondente do Google Sheets.

4. **Execução de Testes**:
   - Executei os testes no emulador Pixel 5, ajustando o horário do emulador quando necessário para testar requisitos baseados em tempo.
   - Marquei os resultados como APROVADO ou REPROVADO na planilha.
   - Registrei bugs no Jira para testes reprovados, vinculando os IDs à planilha.

5. **Solução de Bloqueios**:
   - Quando um teste falhou em um navegador ou no aplicativo, busquei alternativas (ex.: recriar o teste em outro navegador ou criar pedidos via interface web para visualização no aplicativo móvel).

### Tarefa 3: Teste do Backend do Urban Scooter

1. **Preparação do Ambiente**:
   - Iniciei o servidor para obter a URL do projeto e acessei a documentação da API em `URL+/docs/pt/`.
   - Configurei o **Postman** com a URL para testar os endpoints da API.
   - Conectei-me ao banco de dados `scooter_rent` usando o comando `psql -U morty -d scooter_rent` (senha: `smith`), considerando aspas duplas para tabelas com letras maiúsculas (ex.: `SELECT * FROM "Couriers"`).

2. **Análise de Requisitos**:
   - Examinei os requisitos de backend, focando nos endpoints destacados em amarelo para adicionar e excluir entregadores.

3. **Criação de Casos de Teste**:
   - Desenvolvi casos de teste para os endpoints de adicionar e excluir entregadores, incluindo:
     - **Cenários positivos**: Ex.: adicionar um entregador com dados válidos, excluir um entregador existente.
     - **Cenários negativos**: Ex.: tentar adicionar um entregador com dados inválidos, excluir um entregador inexistente.
   - Registrei os casos na aba "Tarefa 3: Casos de teste da API" do Google Sheets.

4. **Execução de Testes**:
   - Testei os endpoints via Postman, verificando códigos de resposta HTTP, payloads e comportamento do banco de dados.
   - Validei os dados no banco de dados com consultas SQL, garantindo consistência com as ações da API.
   - Marquei os resultados como APROVADO ou REPROVADO na planilha.
   - Registrei bugs no Jira para testes reprovados, vinculando os IDs à planilha.

## Ferramentas Utilizadas

- **Google Chrome e Opera**: Para testes da interface web (versões 85+ e 71+, respectivamente, resolução 1280x720).
- **Android Studio**: Para execução do aplicativo móvel no emulador Pixel 5 (Android 31).
- **Postman**: Para testes dos endpoints da API.
- **PostgreSQL**: Para consultas no banco de dados `scooter_rent`.
- **Google Sheets**: Para documentar casos de teste, resultados e links para relatórios de bugs.
- **Google Docs**: Para anexar o link do modelo e outros recursos.
- **Jira**: Para registro de bugs.
- **Figma**: Para consulta dos layouts do aplicativo web e móvel.
- **Urban Scooter**: Aplicativo testado (web, móvel e backend).

## Estrutura do Repositório

- `Teste do Urban Scooter.xlsx`: Modelo preenchido com casos de teste, resultados e links para relatórios de bugs (nomeado como "[Seu Nome], [Sobrenome], [Grupo] — Projeto Final").
- `Teste do Urban Scooter.docx`: Documento com links para a planilha e outros recursos (nomeado conforme instruções).
- `README.md`: Este arquivo, descrevendo o projeto.

## Resultados

- Criei e executei casos de teste abrangentes para o formulário "About Customer" da interface web, validando funcionalidade e layout em dois navegadores.
- Testei as funcionalidades destacadas do aplicativo móvel Urban Scooter, garantindo cobertura de layout e comportamento, com ajustes no emulador para superar bloqueios.
- Validei os endpoints de adicionar e excluir entregadores no backend, verificando a consistência com o banco de dados.
- Documentei todos os resultados no Google Sheets e registrei bugs no Jira, assegurando rastreabilidade e clareza.
- Contribuí para a garantia de qualidade do Urban Scooter, identificando e reportando problemas para melhorar a experiência do usuário.

## Sobre Mim

Sou um profissional em transição de carreira para a área de Qualidade de Software, com formação no **Bootcamp de Análise de QA da TripleTen**. Minha experiência prévia em ambientes dinâmicos me proporcionou habilidades como atenção aos detalhes, organização e colaboração. Estou entusiasmado para aplicar meus conhecimentos em testes manuais e automatizados, abrangendo interfaces web, aplicativos móveis e APIs, para garantir a qualidade de produtos digitais.

## Contato

- 📍 São Paulo, Brasil
- 📧 luis_commans@hotmail.com
- 🔗 https://www.linkedin.com/in/danilocommansqa
- 💻 https://github.com/MrCommans

Obrigado por visitar meu repositório! 🛵
