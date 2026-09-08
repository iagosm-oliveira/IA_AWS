# 🧠 Aula 03 — Engenharia de Prompts, Modelos de Fundação (FMs) e Certificações AWS

Este documento centraliza os conceitos teóricos sobre o funcionamento das IAs Generativas, estruturação avançada de prompts, arquitetura de modelos e os passos para as certificações oficiais da AWS, unindo a teoria técnica a exemplos práticos de uso.

---

## 1. Fundamentos da Interação com IA

* **Linguagem Natural:** Forma como os seres humanos se comunicam no dia a dia, sem a sintaxe rígida de código de programação. É a interface principal para interagir com modelos generativos.
* **O que é um Prompt:** É uma instrução, comando ou pergunta escrita em linguagem natural que solicita ao modelo a execução de uma tarefa específica.
  > **Exemplo:** *"Escreva um e-mail formal de 3 linhas cobrando o envio do relatório financeiro de agosto."*
* **Múltiplas Inferências:** Um mesmo prompt pode gerar saídas (inferências) completamente diferentes dependendo do Modelo de Fundação (FM) utilizado (ex: Amazon Titan vs. Anthropic Claude) ou das configurações de aleatoriedade ("temperatura").

---

## 2. Engenharia de Prompts (*Prompt Engineering*)

Para obter resultados precisos, a construção de um prompt deve seguir uma estrutura lógica. É a arte de formular a pergunta certa para obter o resultado perfeito.

**Anatomia de um Prompt de Sucesso:**
* **Contexto:** "Você é um especialista em marketing sênior..."
* **Intuito/Objetivo:** "...e precisa criar um slogan..."
* **Restrições:** "...usando no máximo 5 palavras, sem usar a palavra 'inovação'."
* **Entrada/Saída:** "...para este produto: [Tênis de corrida]. Formato: entregue uma lista com 3 opções."

**Técnicas de Estruturação:**
* **Zero-shot:** O modelo resolve o problema sem receber nenhum exemplo prévio.
  > *"Classifique o sentimento da frase 'A entrega do meu pacote atrasou': "*
* **One-shot:** O prompt inclui um único exemplo prático para guiar o formato da resposta.
  > *"Frase: 'Amei o produto' -> Sentimento: Positivo.*<br>
  > *Frase: 'A entrega atrasou' -> Sentimento: "*
* **Few-shot / Two-shot:** Utiliza múltiplos exemplos para refinar a precisão e a capacidade de decisão da IA em tarefas complexas.
* **Cadeia de Pensamento (*Chain of Thought*):** Instruir a IA a "pensar passo a passo", quebrando um problema complexo em etapas lógicas antes do resultado final.
  > *"João comprou 5 maçãs, comeu 2 e depois comprou mais 4. Pense passo a passo e me diga quantas maçãs ele tem agora."*

---

## 3. Modelos de Fundação (FMs) e LLMs

A regra de ouro do ecossistema generativo: **Todo LLM é um FM, mas nem todo FM é um LLM.** 

* **Foundation Models (FMs):** São o "tronco robusto". Modelos treinados em vastas quantidades de dados que servem de base para diversas tarefas (texto, imagem, áudio).
* **Large Language Models (LLMs):** São os "galhos especializados". FMs focados exclusivamente em entender, processar e gerar texto/linguagem.

**Outras Arquiteturas e Tecnologias de IA:**
* **Transformadores (*Transformers*):** A arquitetura base que revolucionou os LLMs modernos, permitindo o processamento paralelo de palavras.
* **Modelos de Difusão (*Diffusion Models*):** Especializados em criar imagens a partir de "ruído" estático (ex: Stable Diffusion).
* **GANs (*Generative Adversarial Networks*):** Duas redes neurais que competem entre si (um gerador cria a imagem, um discriminador tenta adivinhar se é falsa) para criar dados hiper-realistas.
* **VAEs (*Variational Autoencoders*):** Utilizados para compressão e geração de novos dados baseados em representações latentes.
* **PLN (Processamento de Linguagem Natural):** O campo de estudo que permite às máquinas "lerem", entenderem e derivarem significado de textos humanos.

---

## 4. Como os LLMs Processam Texto

A IA não "lê" a letra "A", ela processa números. Isso ocorre em duas etapas:

1. **Tokens:** O texto é fatiado em pedaços (palavras, sílabas ou caracteres). 
   > **Exemplo:** A palavra "Gato" equivale a 1 token. Uma palavra complexa como "Inconstitucionalmente" pode ser dividida em 4 ou 5 tokens menores. *(Prática da aula: Visualização no Tokenizer da OpenAI).*
2. **Vetores (Incorporações / *Embeddings*):** Os tokens são convertidos em coordenadas matemáticas em um espaço multidimensional. É assim que a IA entende a semântica: ela sabe matematicamente que a palavra "Rei" está muito próxima de "Rainha", mas distante de "Cadeira".

---

## 5. Desafios e Mitigação de Riscos

As saídas geradas por FMs possuem riscos intrínsecos que o Engenheiro de Prompt deve gerenciar:

* **Alucinações:** A IA inventa informações falsas e as apresenta com extrema confiança.
  > *Exemplo: Citar um artigo científico ou número de lei que nunca existiu para justificar uma resposta.*
* **Viés (*Bias*):** Respostas distorcidas baseadas em preconceitos históricos nos dados de treinamento.
  > *Exemplo: Associar automaticamente a palavra "enfermeiro" ao gênero feminino e "engenheiro" ao masculino.*
* **Toxicidade e Ilegalidade:** Geração de conteúdo ofensivo, quebra de direitos autorais ou instruções para burlar sistemas de segurança.

**Como Mitigar (Componentes de uma Saída Ideal):**
1. **Escolha do Modelo:** Selecionar a arquitetura correta (ex: LLM para texto, Difusão para imagem).
2. **Design do Prompt:** Aplicar regras e limites rígidos.
3. **Qualidade dos Dados:** Garantir que o contexto fornecido (como em arquiteturas RAG) seja limpo, ético e confiável.

---

## 6. Atividades Práticas e Certificações AWS

**✅ Laboratórios e Testes do AWS Academy:**
- [x] Módulo 1: Concluído
- [x] Módulo 2: Concluído
- [x] Módulo 3: Concluído
- [x] Módulo 4: Concluído

**🎯 Jornada de Certificação AWS:**
As certificações oficiais validam a expertise técnica na nuvem e orientam a carreira. As trilhas devem ser escolhidas conforme a vocação:
* *Foundational* (Cloud Practitioner) ➡️ *Associate* (Architect, Developer, SysOps) ➡️ *Professional* ou *Specialty* (como a de Machine Learning/AI).
* **Agendamento de Provas:** O exame oficial é gerenciado pela plataforma **Pearson VUE**, que supervisiona a aplicação da prova, podendo ser realizada em centros de teste físicos ou de forma online com fiscalização remota (*proctoring*).