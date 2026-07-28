# 🚀 Desafio DIO: Miniguia Temático com NotebookLM - Dataprev 2026 (Desenvolvimento de Software)

Este repositório contém o projeto prático do desafio da DIO, explorando o uso da Inteligência Artificial (NotebookLM) como ferramenta de aprendizagem ativa, curadoria de conteúdo e organização do conhecimento. 

O foco deste caderno temático é a preparação de alto nível para o concurso da **DATAPREV 2026**, especificamente para o cargo de **Analista de Tecnologia da Informação - Perfil 3: Desenvolvimento de Software**.

---

## 🎯 1. Contexto e Objetivos

A área de Tecnologia da Informação em concursos públicos (especialmente os organizados pela banca FGV) exige uma preparação extenuante, que mistura conhecimentos gerais densos (Português, Lógica) e um núcleo duro de TI (Java, Spring, Arquitetura Hexagonal, Banco de Dados, Metodologias Ágeis). 

**Objetivos de Estudo com este Caderno:**
1. Filtrar e consolidar as regras gramaticais e lógicas mais cobradas pela banca FGV, com foco em "pegadinhas".
2. Sistematizar os requisitos técnicos de TI exigidos no edital.
3. Utilizar o NotebookLM para transformar dezenas de páginas de editais e provas antigas em apostilas de revisão rápida e áudios dinâmicos (podcasts de revisão).

---

## 📚 2. Curadoria de Fontes

Para garantir que a IA não tivesse "alucinações" e fosse cirúrgica nas informações, foi feito o upload de um conjunto de fontes confiáveis (em texto e PDF) no NotebookLM. Foram selecionadas 4 fontes primárias abertas para este projeto:

1. **Edital Oficial DATAPREV 2026 (FGV Conhecimento):** Arquivo PDF oficial contendo as disciplinas, ementas e requisitos do cargo de Desenvolvimento de Software.
2. **Provas Anteriores (FGV e Cebraspe):** Cadernos de provas recentes aplicadas para o cargo de Analista de TI da Dataprev, fundamentais para mapear o estilo de cobrança.
3. **Guia de Estudos Gran Cursos / Estratégia Concursos:** Artigos em formato web detalhando o que estudar para a Dataprev, incluindo o ciclo PDCA e Engenharia de Requisitos.
4. **Resumo TI TOTAL - Bancos de Dados:** Material técnico em PDF focado na resolução de questões sobre normalização, modelo relacional e SQL para concursos.

---

## 🛠️ 3. Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

A extração do melhor conteúdo exigiu testes e refinos nos comandos passados para o NotebookLM. Abaixo documento o processo de engenharia de prompts:

**Tentativa 1: Resumo Simples (Muito genérico)**
*   *Prompt utilizado:* "Resuma o conteúdo de Português do edital."
*   *Resultado:* A IA trouxe apenas uma lista de tópicos (ortografia, coesão, etc.), sem aprofundamento. Faltou direcionamento de estilo.

**Tentativa 2: Prompt Estratégico (Sucesso!)**
*   *Prompt utilizado:* `Com base nas fontes anexadas, escreva o conteúdo completo para o Tópico 1.2: Ortografia oficial e mecanismos de coesão textual. O texto deve ter formato de apostila de cursinho, incluindo: Explicação direta e didática do conceito; Principais pontos de atenção (o que as bancas costumam usar como pegadinha); Exemplos práticos; Tabela de revisão rápida.`
*   *Resultado:* O NotebookLM gerou um material estruturado, identificando o comportamento da banca FGV e isolando casos de anáfora, catáfora e uso do hífen com base em questões reais contidas nas fontes.

**Cicatriz / Troubleshooting (Geração de Imagens):**
*   *O problema:* Tentei pedir para a IA gerar uma capa de YouTube para o Podcast de estudos (`Gera uma imagem para colocar esse podcasts no youtube...`).
*   *A Solução:* O modelo do NotebookLM é baseado em LLM textual e análise de documentos, não gerando imagens nativamente. A "cicatriz" foi contornada solicitando à IA que gerasse um **Prompt de Imagem (Midjourney/DALL-E)** com base nas cores e contexto do edital, que eu pudesse usar em ferramentas externas.

---

## 📖 4. Miniguia de Estudo (Entrega Final)

Com base nas iterações, o caderno gerou materiais robustos. Abaixo apresento a consolidação da entrega:

### A. Resumos Estruturados do Assunto
*   **Língua Portuguesa (A Pegadinha da FGV):** Foco na morfossintaxe e reescrita de frases. A banca avalia o texto como um "organismo vivo". A supressão de vírgulas, por exemplo, não causa erro gramatical na prova, mas altera o sentido de "explicação" para "restrição".
*   **Língua Inglesa (Gramática Semântica):** A prova não pede conjugação isolada. O foco do estudo mapeado pela IA são as *Linkers* (conectivos). Ex: saber a diferença de "Thus" (efeito) e "As" (causa) na frase.
*   **Raciocínio Lógico (A Tabela do Se... Então):** A regra matadora é a dedução. A falácia da afirmação do consequente é a armadilha mais comum mapeada nas fontes de Exatas.

### B. Glossário de Conceitos Aprendidos
*   **Anáfora / Catáfora:** Elementos de coesão textual. Anáfora retoma o que já foi dito (Ex: "Esse"); Catáfora antecipa o que será dito (Ex: "Este").
*   **Contrapositiva:** A regra de equivalência lógica mais cobrada no "Se A, então B". Consiste em inverter as frases e negar ambas ("Se não B, então não A").
*   **Skimming e Scanning:** Estratégias de leitura exigidas para a prova de Inglês. *Skimming* (leitura rápida para ideia central) e *Scanning* (varredura em busca de um dado específico, como um número ou ano).
*   **ACID:** Acrônimo de transações em Banco de Dados (Atomicidade, Consistência, Isolamento e Durabilidade), muito cobrado nas fontes específicas de TI.

### C. Prompts Reutilizáveis (Para Revisão Futura)
Deixo aqui um kit de prompts para quem for utilizar este repositório e quiser continuar estudando com a IA:

1. **Para Geração de Questões Inéditas:**
   > `"Atue como um examinador da banca FGV. Com base no conteúdo dos PDFs anexados, crie 5 questões de múltipla escolha (A a E) de nível difícil sobre [INSERIR TEMA]. Forneça o gabarito comentado ao final."`
2. **Para Criação de Flashcards:**
   > `"Analise as fontes e extraia os 10 conceitos mais importantes sobre [INSERIR TEMA]. Formate a saída como uma tabela, onde a Coluna 1 é a 'Frente do Cartão' (Pergunta/Termo) e a Coluna 2 é o 'Verso do Cartão' (Resposta/Definição rápida)."`
3. **Para Audio Overview (Podcast de Revisão):**
   > `"Gere uma Visão Geral em Áudio (Podcast) focando exclusivamente nas 'pegadinhas' do edital presentes no tópico [INSERIR TEMA]. Os apresentadores devem assumir um tom de urgência e foco em revisão de véspera de prova."`
