# 🧠 Aula 02 — Introdução à Inteligência Artificial

## 1. Conceitos Globais de IA
Estudada desde 1950, a **Inteligência Artificial (IA)** busca simular a capacidade de raciocínio e tomada de decisão humana em sistemas computacionais.

**Exemplos e Aplicações:**
* **Machine Learning (ML):** Algoritmos que aprendem a partir de dados (base para a IA Generativa).
* **Visão Computacional:** Processamento de imagens, como **OCR** (reconhecimento óptico de caracteres usado em radares de trânsito).
* **Dispositivos Inteligentes:** Automação residencial, assistentes de voz e IoT.
* **IA Responsável:** Práticas éticas voltadas para transparência, privacidade, segurança e mitigação de viés.

---

## 2. Aprendizado de Máquina (Machine Learning)

**Tipos de Aprendizado:**
* **Supervisionado:** Trabalha com **dados rotulados** (*labeled data*), onde cada entrada possui uma resposta conhecida. Divide-se em dois tipos principais de problemas:
  * **Classificação:** Preve rótulos ou categorias discretas (ex: identificar se um e-mail é *spam* ou *não-spam*, se uma imagem é de um gato ou cão).
  * **Regressão:** Preve **valores numéricos contínuos** ou dados numéricos com base em históricos (ex: prever o preço de um imóvel, estimar a temperatura do dia, calcular o valor de uma multa).
* **Não Supervisionado:** Trabalha com **dados não rotulados** (*unlabeled data*) para descobrir padrões e agrupamentos (*clustering*) por conta própria sem intervenção humana.
* **Por Reforço:** Otimiza tomadas de decisão aprendendo por tentativa, erro, recompensas e punições em um ambiente dinâmico.

**Conceitos Fundamentais:**
* **Modelo:** O resultado final gerado após o treinamento dos dados (a "inteligência" criada).
* **Previsão:** A probabilidade calculada pelo modelo ao identificar padrões nos dados.
* **Inferência:** A etapa de validar e processar novos dados em um modelo que já foi treinado.
* **Viés (Bias):** Distorções nos resultados provocadas por dados de treinamento desequilibrados ou incompletos.

---

## 3. Tipos de Dados
1. **Estruturados:** Organizados em tabelas rígidas e bancos relacionais (ex: SQL, planilhas).
2. **Semiestruturados:** Possuem marcações ou tags sem tabela fixa (ex: JSON, XML).
3. **Não Estruturados:** Sem formato predefinido, exigindo técnicas avançadas para interpretação (ex: imagens, áudios, vídeos).

---

## 4. Deep Learning (DL) e IA Generativa
* **Deep Learning (DL):** Imita o cérebro humano por meio de redes neurais profundas. A teoria é antiga, mas evoluiu com o aumento recente do poder de processamento computacional.
* **IA Generativa:** Evolução focada na criação autônoma de novos conteúdos (textos, códigos, imagens e áudios).

---

## 🛠️ Exercício Prático: Hospedando um Site Gerado por IA na AWS

### Passo 1: Criar a VM Windows no EC2
1. Acesse o **Console AWS** → Navegue até o serviço **EC2** → **Instâncias**.
2. Clique em **Launch Instances** (Executar instâncias).
3. Selecione a imagem **Windows Server** e conclua o provisionamento.

### Passo 2: Instalar o Servidor Web (IIS)
1. Conecte-se à VM Windows via RDP.
2. Abra o **Gerenciador de Servidores** (*Server Manager*).
3. Adicione a *feature* de **Web Server (IIS)** e conclua a instalação.

### Passo 3: Criar o Site com IA Generativa
1. Acesse uma ferramenta de IA Generativa (ChatGPT, Claude ou Gemini).
2. Escreva um prompt solicitando a criação de um site completo.
3. Peça para que os códigos **HTML, CSS e JavaScript** fiquem concentrados em um **único arquivo**.

### Passo 4: Hospedar o Site no IIS
1. Na VM Windows, pressione `Win + R`, digite `inetmgr` e pressione **Enter**.
2. Expanda a árvore do servidor no painel esquerdo do IIS.
3. Clique com o botão direito na pasta do site → **Explorar** (abrirá `C:\inetpub\wwwroot`).
4. Delete os arquivos padrões da pasta e cole o seu arquivo `index.html`.