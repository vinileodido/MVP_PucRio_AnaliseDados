# Características do Dataset IoT Industrial

Origem do dataset: [https://www.kaggle.com/datasets/canozensoy/industrial-iot-dataset-synthetic](https://www.kaggle.com/datasets/canozensoy/industrial-iot-dataset-synthetic)

<BR>

---

<BR>

## ❗ Objetivo do Dataset
Este dataset é típico para **manutenção preditiva**, onde o objetivo é prever falhas antes que aconteçam, usando dados de sensores IoT para otimizar a manutenção industrial.

* ⚠️ Atenção: Todos os dados são totalmente **sintéticos**, criados para imitar tendências industriais realistas para exploração e modelagem seguras. **Não foram utilizados dados do mundo real.**
<BR>
<BR>

---

## 📋 Informações Detalhadas dos Atributos

### 🔧 Identificação e Características da Máquina
* **ID_Máquina**: Identificador único de cada máquina no sistema

* **Tipo_Máquina**: Categoria ou modelo da máquina (ex: torno, fresadora, prensa)

* **Ano_Instalação**: Ano em que a máquina foi instalada na fábrica

* **Horas_Operação**: Total de horas que a máquina já operou desde a instalação

### 📡 Sensores de Monitoramento
* **Temperatura_Celsius**: Temperatura atual da máquina em graus Celsius

* **Vibração_mms**: Nível de vibração medido em milímetros por segundo (indicador de desgaste)

* **Ruído_dB**: Nível de ruído produzido pela máquina em decibéis

* **Nível_Óleo_%**: Percentual do nível de óleo lubrificante no reservatório

* **Fluido_Refrigerante_%**: Percentual do nível de líquido refrigerante

* **Consumo_Energia_kW**: Consumo atual de energia elétrica em quilowatts

### 🌡️ Sensores Específicos
* **Intensidade_Laser**: Intensidade do laser (para máquinas que usam corte/soldagem a laser)

* **Pressão_Hidráulica_bar**: Pressão do sistema hidráulico em bar

* **Fluxo_Fluido_Refrigerante_L_min**: Taxa de fluxo do líquido refrigerante em litros por minuto

* **Índice_Calor**: Índice calculado que representa o nível geral de aquecimento da máquina

### 🔧 Histórico de Manutenção
* **Dias_Ultima_Manutenção**: Número de dias desde a última manutenção realizada

* **Histórico_Manutenções**: Quantidade total de manutenções já realizadas na máquina

* **Histórico_Falhas**: Número de falhas registradas no histórico da máquina

### 🤖 Sistema de IA e Monitoramento
* **Supervisão_IA**: Indica se a máquina está sob supervisão de sistema de IA (True/False)

* **Códigos_Erros_30_Dias**: Quantidade de códigos de erro registrados nos últimos 30 dias

* **Eventos_Sobrescrita_IA**: Número de vezes que operadores humanos sobrescreveram decisões da IA

### 🎯 Predição e Análise
* **Vida_Útil_Restante_Dias** 📉📅: Estimativa de quantos dias a máquina ainda pode operar antes de precisar de manutenção

* **Falha_Nos_Próximos_7_Dias** 🎯📅 - **Variável target**: Indica se a máquina falhará nos próximos 7 dias (True/False)
<BR>
<BR>

---

<BR>

## 🏭 Categorização de Máquinas

* ⚠️ Atenção: Esta variável não é original do dataset, com base em similaridades de funções foram criadas categorias para as máquinas. Esta é uma das ações de **Engenharia de Atributos**, onde criamos novas informações baseadas nas existentes.
<BR>
<BR>

A variável "**Tipo_Máquina**" possui a informação de quais classes os maquinários são categorizados.
Porém, para visualizar 33 categorias simultaneamente traz um desafio computacional, visto que temos um dataset de 500000 instâncias.
Para facilitar, agrupamos em 6 categorias:

* **Fabricação e Conformação**;

* **Processamento e Montagem**;

* **Manuseio e Logística**;

* **Inspeção e Qualidade**;

* **Embalagem e Finalização**;

* **Suporte e Utilitários**;
<BR>

### Tabela contendo as categorias de cada tipo de máquina

| Categoria_Funcional_Máquina | Tipo_Máquina | Explicação |
|------------------------------|---------------|------------|
| Fabricação e Conformação | Máquina de Corte a Laser | Utiliza um feixe de laser para cortar ou gravar materiais com extrema precisão. |
| Fabricação e Conformação | Torno CNC | Máquina que rotaciona uma peça para modelá-la com ferramentas de corte. |
| Fabricação e Conformação | Forno Industrial | Equipamento de alta temperatura para processos como tratamento térmico de metais. |
| Fabricação e Conformação | Prensa Hidráulica | Máquina que usa um cilindro hidráulico para gerar força de compressão para prensar ou moldar. |
| Fabricação e Conformação | Dobradeira / Quinadora | Máquina-ferramenta utilizada especificamente para dobrar chapas metálicas. |
| Fabricação e Conformação | Impressora 3D | Máquina que constrói objetos tridimensionais camada por camada a partir de um modelo digital. |
| Fabricação e Conformação | Retificadora / Esmeril Industrial | Máquina que usa um rebolo abrasivo para remover material e dar acabamento de alta precisão. |
| Fabricação e Conformação | Fresadora CNC | Máquina que usa ferramentas de corte rotativas para remover material de uma peça. |
| Fabricação e Conformação | Injetora de Plástico | Máquina que fabrica peças plásticas injetando material plástico fundido em um molde. |
| Processamento e Montagem | Misturador | Equipamento para combinar ou homogeneizar diferentes materiais para criar um produto final. |
| Processamento e Montagem | Máquina de Pegar e Colocar | Robô que pega componentes e os posiciona em outro local, comum na montagem de eletrônicos. |
| Processamento e Montagem | Parafusadeira Automatizada | Sistema robótico que aperta parafusos de forma autônoma, garantindo torque consistente. |
| Processamento e Montagem | Braço Robótico | Braço mecânico programável usado para soldar, pintar, montar, manusear, etc. |
| Manuseio e Logística | Sistema de Shuttle | Sistema automatizado onde um carro motorizado guarda e recupera caixas/paletes em estantes. |
| Manuseio e Logística | Veículo Guiado Automatizado | Robô móvel que transporta materiais de forma autônoma dentro de uma fábrica ou armazém. |
| Manuseio e Logística | Esteira Transportadora | Sistema de transporte contínuo que move produtos ou materiais entre estações de trabalho. |
| Manuseio e Logística | Empilhadeira Elétrica | Veículo para levantar e mover cargas pesadas, ideal para ambientes internos. |
| Manuseio e Logística | Ponte Rolante Suspensa (Guindaste) | Utilizado para içar e mover cargas extremamente pesadas que outras máquinas não conseguem. |
| Inspeção e Qualidade | Sistema de Visão | Usa câmeras e software para inspeção de qualidade, detecção de defeitos e guiamento de robôs. |
| Inspeção e Qualidade | Máq. de Medição por Coordenadas (MMC) | Dispositivo de alta precisão para medir as dimensões geométricas de um objeto. |
| Inspeção e Qualidade | Inspetor de Raios-X | Sistema que usa raios-X para detectar contaminantes físicos dentro de produtos. |
| Embalagem e Finalização | Rotuladora | Máquina que aplica etiquetas ou rótulos em produtos, embalagens ou recipientes. |
| Embalagem e Finalização | Embaladora Termoencolhível | Envolve um produto com filme plástico e aplica calor para que o filme encolha e se ajuste. |
| Embalagem e Finalização | Secador Industrial | Equipamento que remove umidade de materiais, geralmente antes de embalar. |
| Embalagem e Finalização | Montadora de Caixas | Máquina que monta caixas de papelão automaticamente a partir de peças planas. |
| Embalagem e Finalização | Embaladora a Vácuo | Máquina que remove o ar de uma embalagem antes de selá-la, estendendo a vida útil do produto. |
| Embalagem e Finalização | Paletizador | Máquina que organiza e empilha caixas ou produtos de forma automática sobre um palete. |
| Suporte e Utilitários | Chiller Industrial | Sistema de refrigeração que remove o calor de um líquido para resfriar equipamentos e processos. |
| Suporte e Utilitários | Controlador de Válvula | Dispositivo que gerencia a abertura e o fechamento de válvulas para regular o fluxo de fluidos. |
| Suporte e Utilitários | Compressor | Gera ar comprimido para alimentar ferramentas pneumáticas e atuadores em toda a fábrica. |
| Suporte e Utilitários | Caldeira | Equipamento que aquece água para gerar vapor para aquecimento e processos industriais. |
| Suporte e Utilitários | Trocador de Calor | Dispositivo que transfere calor entre dois fluidos sem que eles se misturem. |
| Suporte e Utilitários | Bomba | Dispositivo mecânico que move fluidos (líquidos ou gases) através de um sistema. |
