# Características do Dataset IoT Industrial

---

## ❗ Objetivo do Dataset
Este dataset é típico para **manutenção preditiva**, onde o objetivo é prever falhas antes que aconteçam, usando dados de sensores IoT para otimizar a manutenção industrial.

---

## 🏭 Categorização de Máquinas
A variável "**Tipo_Máquina**" possui a informação de quais classes os maquinários são categorizados.

O dataset inclui conhecimento específico do domínio com **32 tipos de máquinas** categorizadas em 6 grupos funcionais:

* **Fabricação e Conformação**: Máquina de Corte a Laser, Torno CNC, Forno Industrial, Prensa Hidráulica, Dobradeira/Quinadora, Impressora 3D, Retificadora/Moedor, Fresadora CNC, Injetora de Plástico

* **Processamento e Montagem**: Misturador, Máquina de Pegar e Colocar, Parafusadeira Automatizada, Braço Robótico

* **Manuseio e Logística**: Sistema de Shuttle, Veículo Guiado Automatizado, Correia Transportadora/Esteira, Empilhadeira Elétrica, Ponte Rolante/Guindaste

* **Inspeção e Qualidade**: Sistema de Visão, Máquina de Medição por Coordenadas, Inspetor de Raios-X

* **Embalagem e Finalização**: Rotuladora, Embaladora Termoencolhível, Secador Industrial, Armadora de Caixas, Embaladora a Vácuo, Paletizador

* **Suporte e Utilitários**: Chiller Industrial, Controlador de Válvula, Compressor, Caldeira, Trocador de Calor, Bomba

## 📋 Informações Detalhadas dos Atributos

### 🔧 Identificação e Características da Máquina
**ID_Máquina**
- Identificador único de cada máquina no sistema

**Tipo_Máquina**
- Categoria ou modelo da máquina (ex: torno, fresadora, prensa)

**Ano_Instalação**
- Ano em que a máquina foi instalada na fábrica

**Horas_Operação**
- Total de horas que a máquina já operou desde a instalação

### 📡 Sensores de Monitoramento
**Temperatura_Celsius**
- Temperatura atual da máquina em graus Celsius

**Vibração_mms**
- Nível de vibração medido em milímetros por segundo (indicador de desgaste)

**Ruído_dB**
- Nível de ruído produzido pela máquina em decibéis

**Nível_Óleo_%**
- Percentual do nível de óleo lubrificante no reservatório

**Fluido_Refrigerante_%**
- Percentual do nível de líquido refrigerante

**Consumo_Energia_kW**
- Consumo atual de energia elétrica em quilowatts

### 🌡️ Sensores Específicos
**Intensidade_Laser**
- Intensidade do laser (para máquinas que usam corte/soldagem a laser)

**Pressão_Hidráulica_bar**
- Pressão do sistema hidráulico em bar

**Fluxo_Fluido_Refrigerante_L_min**
- Taxa de fluxo do líquido refrigerante em litros por minuto

**Índice_Calor**
- Índice calculado que representa o nível geral de aquecimento da máquina

### 🔧 Histórico de Manutenção
**Dias_Ultima_Manutenção**
- Número de dias desde a última manutenção realizada

**Histórico_Manutenções**
- Quantidade total de manutenções já realizadas na máquina

**Histórico_Falhas**
- Número de falhas registradas no histórico da máquina

### 🤖 Sistema de IA e Monitoramento
**Supervisão_IA**
- Indica se a máquina está sob supervisão de sistema de IA (True/False)

**Códigos_Erros_30_Dias**
- Quantidade de códigos de erro registrados nos últimos 30 dias

**Eventos_Sobrescrita_IA**
- Número de vezes que operadores humanos sobrescreveram decisões da IA

### 🎯 Predição e Análise
**Vida_Útil_Restante_Dias** 📉📅
- Estimativa de quantos dias a máquina ainda pode operar antes de precisar de manutenção

**Falha_Nos_Próximos_7_Dias** 🎯📅
- **Variável target**: indica se a máquina falhará nos próximos 7 dias (True/False)
