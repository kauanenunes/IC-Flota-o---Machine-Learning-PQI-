# IC sobre "Avaliação de parâmetros de flotação utilizando Machine Learning"
Esse repositório será usado para organizar pesquisas e estudos acerca da minha IC com orientação do professor Ardson Vianna.

# 🧪 Anotações: Célula Jameson e Flotação de Espuma

> **💡 Nota do projeto:** Moinhos são difíceis de modelar matematicamente. O uso de **Redes Neurais / IA** surge como uma alternativa viável para esse tipo de desafio.

## O que é a Célula Jameson?
É uma **célula de flotação de espuma**, utilizada num processo para separar seletivamente materiais hidrofóbicos (que repelem água) e hidrofílicos (que têm afinidade com a água). 
* **Critério de Sucesso:** Bolha bem formada e correndo (transbordando) adequadamente.
* **Aplicações:** Indústrias de processamento mineral, reciclagem de papel e tratamento de águas.

**Definição da Operação:**
Trata-se de uma operação unitária onde os minerais valiosos são separados do material sem valor. Isso é feito tornando os minerais hidrofóbicos, para que se fixem em bolhas de ar e subam à superfície, formando uma espuma rica em minério.

**Principais Características e Vantagens:**
* ⬆️ **Maior intensidade** e ⬇️ **menor tamanho** em relação às células de flotação de colunas convencionais.
* Não requer compressor de ar para forçar a suspensão das partículas de minério moído na água (mistura também chamada de **lama ou polpa**).
* **Eficiência Energética:** A ausência de compressor e de partes móveis resulta em um **menor consumo de energia** quando comparada às células convencionais.

---

## ⚙️ Princípios de Funcionamento

**1. Tubo de Descida (*Downcomer*):** 
Ao contrário dos métodos tradicionais, a polpa (minério + água) e o ar são introduzidos *juntos* em uma coluna cilíndrica chamada "tubo de descida".

**2. Efeito de Vácuo:** 
A polpa é injetada no topo desse tubo como um jato de alta velocidade. Esse jato cria um cisalhamento e um vácuo parcial que puxa *naturalmente* o ar atmosférico para dentro do tubo.
* *Benefício direto:* Elimina a necessidade de compressores mecânicos para injetar o ar.

**3. Mistura Intensa:** 
Dentro do tubo de descida, ocorre uma mistura de altíssima velocidade e intensidade.
* *O diferencial:* O ar é quebrado em bolhas muito finas. Isso cria um ambiente de altíssima eficiência onde a probabilidade de contato entre a partícula de minério e a bolha de ar é de **virtualmente 100%**.

**4. Separação no Tanque:** 
A mistura aerada desce pelo tubo e é descarregada no tanque principal da célula.
* *Formação da Espuma (O Concentrado):* Como o tanque tem uma área muito maior que o tubo, a velocidade do fluido diminui bruscamente. Isso permite que as bolhas, agora carregadas de minerais valiosos, subam suavemente à superfície para formar a espuma.
* *Descarte:* O material indesejado (rejeito), que permaneceu hidrofílico, afunda e é descarregado pelo fundo do tanque.


# 🧪 Anotações: Flotação por Espuma e a Química da Separação

## O que é a Flotação por Espuma?
É um **processo de separação física** com o objetivo de separar o que tem valor do que não tem, aproveitando as propriedades físico-químicas das partículas.
* **Principal aplicação:** Indústria mineral e tratamento de água.

**Etapas Iniciais:**
1. **Base:** Mistura de água e minério moído ➔ Formação da **"polpa"**.
2. **Injeção de ar:** Injetar ar dentro da polpa para criar o ambiente de separação.

---

## 🧪 A Química da Separação
O processo utiliza reagentes químicos que alteram as propriedades das partículas para permitir a separação.

* O minério que possui valor econômico (ex: ouro) é tratado para se tornar **hidrofóbico** [*Veja o tópico 1*].
    * Por ser hidrofóbico, o mineral valioso repele a água e adere (gruda) nas bolhas de ar que estão sendo injetadas [*Veja o tópico 2*].
* Por outro lado, o material sem valor (rejeito) permanece **hidrofílico** e não gruda nas bolhas, ficando retido na água e indo para o fundo do tanque [*Veja o tópico 3*].

---

## 📌 Detalhamento do Processo (Mergulhando na Teoria)

### 1️⃣ Como as partículas se tornam hidrofóbicas?
Isso ocorre com o uso de um reagente químico.
* O principal reagente é o **coletor**, que é uma molécula bipolar. 
    * *Estrutura:* Uma extremidade tem afinidade e gruda no ouro, e a outra extremidade (uma cadeia de hidrocarboneto) repele a água.
* Quando o coletor é adicionado à polpa, ele "veste" as partículas de ouro, deixando as "caudas" oleosas apontadas para fora, repelindo a água.
* *Nota extra:* Também usam-se espumantes e modificadores de pH no processo.

### 2️⃣ Por que o ouro adere às bolhas?
É uma questão de atração e repulsão (termodinâmica).
* Como a partícula de ouro agora está coberta por uma camada química que repele a água, estar cercada por água gasta muita energia e a deixa "desconfortável".
* Quando a bolha de ar passa perto, a partícula de ouro "foge" da água e gruda na bolha de ar.
* O **ambiente gasoso (a bolha) é o único refúgio seguro** dentro daquele tanque de água para a partícula hidrofóbica.

### 3️⃣ Dá pra ver o rejeito no fundo do processo? Como esse rejeito é retirado?
* **NÃO** dá para enxergar **nada** além da espuma, pois a "polpa" é extremamente turva, densa e opaca (semelhante a barro/lama).
* **Onde a IA entra:** Como só dá para ver a espuma transbordando na superfície, é por isso que a **visão computacional do projeto é focada no topo do tanque**.
* **Retirada do Rejeito:** O rejeito é retirado na descarga de fundo, onde há válvulas e tubulações. Nesse processo contínuo (onde a polpa entra por cima e a espuma transborda pela borda superior), a lama pesada com o rejeito é sugada e bombeada pelas saídas de fundo.
* **Destino do Rejeito:** Esse rejeito vai para outras etapas de tratamento para tentar recuperar o restinho de ouro que sobrou ou, finalmente, é enviado para as famosas barragens de rejeito.

---

## 🌊 Dinâmica da Espuma, Célula Jameson e a IA

### 🔄 Dinâmica da Espuma e o Transbordo
1. As bolhas carregadas com partículas de minério valioso sobem à superfície do tanque.
2. Essas bolhas se acumulam no topo, formando uma espuma rica em minério.
3. Chegando ao ponto crítico do processo: ocorre o **transbordo**, para que o material rico em minério possa ser recolhido.

### ⚙️ Célula Jameson (Diferencial)
Diferente dos processos convencionais, na Célula Jameson (CJ) há o **tubo de descida**.
* Nesse tubo ocorre a mistura intensa de ar e polpa.
* Nessa mistura de **alta velocidade e intensidade**, cria-se um **vácuo** parcial no sistema.
* A grande diferença é que, com esse vácuo e intensidade, são criadas **bolhas muito finas**.
* Esse tamanho reduzido de bolhas é uma vantagem enorme, pois aumenta a probabilidade de **contato com a partícula** do minério para uma taxa de quase **100%**.

### 🤖 Como a IA Entra Nisso?
*A eficiência do processo depende da espuma transbordando constantemente.*
* Tradicionalmente, na indústria, a leitura de parâmetros como o tamanho de bolhas, estabilidade e transbordo da espuma é feita no **"olhômetro"** de um operador.
* A visão computacional entra para **automatizar** essa leitura visual ➔ garantindo **medições precisas e constantes**, sem depender de análises subjetivas ou da presença constante de um operador.

---

## 💻 O Básico de ML (Machine Learning)

### 🛠️ Engenharia de Software e Boas Práticas
* Utilizar **boas práticas** no VS Code, criando códigos **modulares**.
* Manter o controle de versões no GitHub.
* ⚠️ **Atenção:** NÃO CRIAR um arquivo gigante! ➔ **CRIAR MÓDULOS** com funções específicas.
* **Separação por pastas:**
  * Uma para imagens cruas.
  * Uma para imagens tratadas.
  * Uma para scripts.

### 🖼️ Como o Computador Enxerga a Imagem?
A imagem para o computador é enxergada como uma grande tabela / matriz de números.
> **Definição:** `Pixel` = a menor unidade de uma imagem.

**1. Exemplo: Imagem em Preto e Branco**
* Cada "quadradinho" (pixel) recebe um valor de `0` (preto absoluto) a `255` (branco absoluto).

**2. Imagens em Escala de Cinza**
* São formadas por matrizes 2D.

**3. Imagens Coloridas RGB**
* São formadas por matrizes 3D.
* Possuem uma estrutura mais complexa, com 3 matrizes sobrepostas, formando um **tensor**.
* As matrizes representam:
  1. Tons de vermelho (*Red*)
  2. Tons de verde (*Green*)
  3. Tons de azul (*Blue*)
  * *(Exemplo: a leitura de um valor 50 pode representar a sombra da borda da bolha).*
* Um único pixel na coordenada `x` e `y` é lido por 3 números: **Px,y = [R, G, B]**.

### 🧮 O Processamento
* O computador faz operações matemáticas com as matrizes (soma, multiplicação, etc.) para destacar contrastes abruptos entre um número de valor 200 (centro claro) e... *(continua na próxima página)*

---

## 🧮 Machine Learning: Tratamento e Classificação de Dados

### 📉 Normalização (Norm)
*Consiste em "espremer" os dados para uma escala padrão e menor, geralmente entre 0 e 1.*
* No básico, o valor máximo é 255 e o valor mínimo é 0. Basicamente é dividir o valor por 255.
* **Por que fazer isso?** Deixa o modelo mais rápido, estável e preciso.
* Exemplo: Pixel 255 vira 1, pixel 0 vira 0, pixel 127 vira 0,5.

**A fórmula matemática:**
$$X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}} = \frac{X}{X_{max}}$$

### 🎯 Algoritmo KNN (K-Nearest Neighbors)
* Clássico de **aprendizado supervisionado** (onde damos exemplos já classificados ao algoritmo).
* **COMO?** Ele classifica um dado novo com base na maioria dos seus vizinhos mais próximos.

**Na Prática:**
1. Imagine que tenho várias fotos de bolhas que já estão rotuladas no banco de dados como "boas" ou "ruins" para o transbordo.
2. Quando uma bolha nova chega, o KNN calcula a **distância matemática** (Distância Euclidiana) entre essa bolha nova e todas as outras do seu banco de dados.

**Fórmula da Distância Euclidiana:**
$$d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

* **A Decisão:** Se você definir a variável **K=3**, o algoritmo seleciona apenas as 3 bolhas vizinhas mais parecidas com a nova. Se 2 dessas forem "boas" e 1 for "ruim", ele classifica a nova imagem como "boa".

---

## 🧩 Aprendizado Não Supervisionado e Clusterização

### 🔍 Clusterização
* Método de **aprendizado não supervisionado**.
* Consiste em jogar os dados para o computador sem dar nenhum rótulo ou gabarito prévio.
* **Objetivo:** O algoritmo deve encontrar padrões ocultos e agrupar os dados por similaridade estrutural, criando *"clusters"* (grupos).

**No nosso projeto:** Podemos fornecer centenas de imagens do processo para o algoritmo, sem dizer nada a ele. A máquina **deduz sozinha** e agrupa as imagens, descobrindo, por exemplo, que existem 3 padrões de espuma:
* **Grupo A:** Bolhas miúdas e homogêneas
* **Grupo B:** Bolhas estourando
* **Grupo C:** Bolhas gigantes

### 🌳 Dendrograma e Clusterização Hierárquica
* **Dendrograma:** Representação visual de um tipo específico de clusterização. Ajuda a decidir qual nível de detalhamento é melhor.
* **Clusterização Hierárquica (Como funciona?):**
  1. O algoritmo vai juntando as imagens mais parecidas de duas em duas, criando pequenos grupos.
  2. Depois, ele junta esses pequenos grupos em grupos maiores e assim por diante.
* **O Gráfico:** O resultado visual é um gráfico em formato de árvore. Na base ficam as imagens separadas e, subindo nos galhos, as imagens vão se unindo.
* **Utilidade do Dendrograma:** Decidir visualmente qual é o melhor "corte" a ser feito na árvore, determinando assim o número ideal de grupos de bolhas para o estudo.
