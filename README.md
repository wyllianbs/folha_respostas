# Folha de Respostas - $\LaTeX$ Template

Template $\LaTeX$ para geração de folhas de respostas de múltipla escolha para leitura óptica de marca (OMR).

## 📋 Descrição

Este template permite a criação de folhas de respostas padronizadas para provas e avaliações, com suporte a diferentes quantidades de questões e marcadores de alinhamento para leitura óptica automatizada.

## ✨ Características

- **Múltiplas configurações de questões**: Suporte para 10, 20, 25, 30, 40, 50 ou 60 questões.
- **Alternativas flexíveis**: Opções A-E para múltipla escolha e V/F para verdadeiro/falso.
- **Campo de matrícula**: Grade numérica (0-9) para preenchimento de 8 dígitos.
- **Campo de tipo de prova**: Identificação do tipo de prova (1-5).
- **Marcadores de alinhamento**: Cantos com marcadores para leitura óptica.
- **Layout otimizado**: Design em colunas para melhor aproveitamento do espaço.
- **Instruções incluídas**: Orientações claras para preenchimento correto.

## 📦 Requisitos

### Pacotes $\LaTeX$ necessários:
- `inputenc` (UTF-8)
- `fontenc` (T1)
- `geometry`
- `tikz`
- `array`
- `tabularx`
- `tcolorbox`
- `multicol`
- `stix`
- `fontawesome5`
- `setspace`
- `enumitem`
- `ragged2e`
- `ifthen`
- `mdframed`
- `xcolor`
- `xparse`
- `lmodern`, `amsmath`, `amsfonts`, `amssymb`
- `helvet`

## 🚀 Como Usar

### 1. Configuração Básica

Edite as variáveis de configuração no início do documento:

```latex
\newcommand{\uf}{Universidade Federal de Santa Catarina}
\newcommand{\centro}{Centro Tecnológico (CTC)}
\newcommand{\departamento}{Departamento de Informática e Estatística (INE)}
\newcommand{\professor}{Nome do Professor}
\newcommand{\assunto}{FOLHA DE RESPOSTAS}
```

### 2. Definir Número de Questões

Ajuste a variável `\numquestions` para o número desejado:

```latex
\newcommand{\numquestions}{60} % Opções: 10, 20, 25, 30, 40, 50, 60
```

### 3. Personalizar Logo

Substitua o arquivo de logo pela imagem da sua instituição:

```latex
\newcommand{\logoUFSCv}{figs/brasao_UFSC_vertical_sigla.pdf}
```

### 4. Compilação

Compile o documento usando:

```bash
pdflatex folha_respostas.tex
```

Ou use seu editor $\LaTeX$ preferido (recomendado: Kile para Linux).

## 🎨 Personalização

### Cores

Ajuste as cores dos elementos:

```latex
\newcommand{\bubblefillcolor}{blue}       % Cor de preenchimento das bolhas
\newcommand{\bubblefontcolor}{gray!70}    % Cor das letras nas bolhas
```

### Tamanhos

Modifique os tamanhos dos elementos:

```latex
\newcommand{\circlesize}{5pt}             % Tamanho dos círculos
\newcommand{\bubblefontsize}{7pt}         % Tamanho da fonte nas bolhas
\newcommand{\markerfontsize}{8pt}         % Tamanho dos marcadores
```

### Espaçamento

Ajuste o espaçamento entre linhas:

```latex
\renewcommand{\arraystretch}{1.7}         % Espaçamento vertical das tabelas
```

## 📐 Estrutura do Layout

O layout é dividido em três seções principais:

1. **Cabeçalho**: Logo, informações institucionais e campos para nome/turma.
2. **Identificação**: 
   - Instruções de preenchimento.
   - Grade de matrícula (8 dígitos).
   - Tipo de prova (1-5).
3. **Questões**: Distribuídas em até 3 colunas, dependendo da quantidade.

## 📝 Marcadores de Alinhamento

O template inclui 4 marcadores nos cantos da folha para facilitar a leitura óptica. Existem 5 estilos disponíveis:

1. Quadrado preenchido (padrão).
2. Quadrado vazado.
3. Quadrado com círculo no centro.
4. Quadrado com ponto no centro.
5. Quadrado com círculo e ponto no centro.

Para alterar o estilo, modifique o último parâmetro da função `\markerboxcorner`:

```latex
\markerboxcorner[0pt]{18pt}[1.25pt][5.5pt][5] % 5 = estilo 5
```

## 🖨️ Recomendações de Impressão

- **Papel**: A4.
- **Margem**: 0.75cm em todos os lados.
- **Impressão**: Frente apenas (verso deve ficar em branco).
- **Qualidade**: Alta resolução para garantir leitura óptica precisa.


## 📂 Exemplos

O diretório `samples/` contém exemplos pré-compilados de folhas de respostas com diferentes quantidades de questões (10, 20, 25, 30, 40, 50 e 60). Consulte estes arquivos para visualizar o resultado final antes de personalizar seu próprio template.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:

- Reportar bugs.
- Sugerir novas funcionalidades.
- Melhorar a documentação.
- Enviar pull requests.

## 📜 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor

**Prof. Wyllian B. da Silva**  
Departamento de Informática e Estatística (INE)  
Universidade Federal de Santa Catarina (UFSC)

---

**Nota**: Este template foi desenvolvido especificamente para uso na UFSC, mas pode ser facilmente adaptado para outras instituições de ensino.
