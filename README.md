# 🔄 Conversor SpeciesLink → JABOT

[![GitHub Pages](https://img.shields.io/badge/Acessar%20Ferramenta-Online-brightgreen)](https://cobranemona.github.io/conversor-specieslink-jabot)
[![Licença](https://img.shields.io/badge/Licença-MIT-blue.svg)](LICENSE)

Ferramenta web gratuita para converter dados do SpeciesLink para o formato padronizado JABOT, utilizado por herbários e coleções biológicas brasileiras.

---

## 📖 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Como Usar](#como-usar)
- [Instalação Local](#instalação-local)
- [Mapeamento de Campos](#mapeamento-de-campos)
- [Limitações Conhecidas](#limitações-conhecidas)
- [Contribuindo](#contribuindo)
- [Licença](#licença)
- [Contato](#contato)

---

## 📋 Sobre o Projeto

O **Conversor SpeciesLink → JABOT** foi desenvolvido para facilitar a migração de dados de biodiversidade entre plataformas. O SpeciesLink é uma rede de informações de coleções biológicas, enquanto o JABOT é o sistema de gerenciamento utilizado pelo Jardim Botânico do Rio de Janeiro e diversas instituições parceiras.

Esta ferramenta automatiza tarefas como:
- Conversão de coordenadas
- Normalização de nomes de pesquisadores
- Extração de informações ecológicas
- Padronização de campos obrigatórios

### Por que usar este conversor?

- ✅ **Economia de tempo**: Processa centenas de registros em segundos
- ✅ **Redução de erros**: Elimina digitação manual e inconsistências
- ✅ **Padronização**: Segue rigorosamente o formato exigido pelo JABOT
- ✅ **Gratuito e online**: Não requer instalação ou cadastro
- ✅ **Código aberto**: Totalmente transparente e auditável

---

## 🚀 Funcionalidades

### Processamento Automático
- [x] Conversão de coordenadas decimais para Graus-Minutos-Segundos (GMS)
- [x] Detecção automática de coordenadas já em formato GMS
- [x] Normalização de nomes de coletores (formato: `Sobrenome, Iniciais`)
- [x] Normalização de nomes de determinadores
- [x] Extração de hábito a partir das notas de coleta
- [x] Extração de habitat a partir das notas de coleta
- [x] Capitalização de texto em campos de notas
- [x] Processamento em lote de múltiplos registros

### Formatos Suportados
- Entrada: Planilhas Excel (.xlsx) exportadas do SpeciesLink
- Saída: Planilha Excel (.xlsx) formatada para importação no JABOT

### Interface
- Design responsivo e intuitivo
- Barra de progresso em tempo real
- Mensagens de erro e avisos
- Sem necessidade de servidor ou instalação

---

## 📝 Como Usar

### Uso Online (Recomendado)

1. Acesse: [https://cobranemona.github.io/conversor-specieslink-jabot](https://cobranemona.github.io/conversor-specieslink-jabot)
2. Preencha o nome do projeto
3. Opcionalmente, personalize o nome do arquivo de saída
4. Selecione o arquivo .xlsx exportado do SpeciesLink
5. Clique em "Converter e Baixar"
6. Aguarde o processamento e faça o download do arquivo convertido

### Dados Necessários no Arquivo de Entrada

O arquivo do SpeciesLink deve conter minimamente:
- `catalognumber` (Número de Tombo)
- `family` (Família)
- `genus` (Gênero)
- `species` (Espécie)

Campos opcionais que enriquecem a conversão:
- `verbatimlatitude` / `verbatimlongitude` (Coordenadas)
- `collector` (Coletor principal)
- `identifiedby` (Determinador)
- `country` / `stateprovince` / `county` / `locality`
- `daycollected` / `monthcollected` / `yearcollected`
- `notes` (Notas de coleta - usadas para extrair hábito/habitat)

### Estrutura de Saída

O arquivo convertido contém as 56 colunas do padrão JABOT, incluindo:
- Dados taxonômicos (família, gênero, espécie, autor)
- Localização (país, estado, município, localidade)
- Coordenadas em GMS (graus, minutos, segundos, direção)
- Dados de coleta (coletor, número, data)
- Dados de determinação (determinador, data)
- Informações ecológicas (hábito, habitat)
- Metadados (projeto, sigla da coleção)

---

## 💻 Instalação Local

### Pré-requisitos
- Navegador web moderno (Chrome, Firefox, Edge, Safari)
- Git (opcional, para clonar o repositório)

### Passos

1. **Clone o repositório:**
```bash
git clone https://github.com/cobranemona/conversor-specieslink-jabot.git
