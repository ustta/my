# Extensão Hotmart Upload Automático

## Descrição do Projeto
Extensão para o Chrome que automatiza o upload de arquivos na plataforma Hotmart simulando comportamento humano e manipulando o Shadow DOM para interagir com elementos complexos da interface.

## Principais Funcionalidades
- Simulação de comportamento humano (movimentos de mouse, timing de digitação)
- Manipulação de Shadow DOM para acesso a elementos complexos
- Upload em lote de até 500 arquivos
- Detecção automática do contexto da página
- Interface para gerenciamento de diferentes tipos de arquivos

## Tecnologias Utilizadas
- JavaScript (ES6+)
- Chrome Extension API
- Manipulação avançada de DOM/Shadow DOM
- Algoritmos de simulação humana (curvas Bezier, timing humanizado)

## Estrutura do Projeto

```
/
├── manifest.json           # Configuração da extensão
├── background.js           # Script background (service worker)
├── content.js              # Script injetado nas páginas da Hotmart
├── popup.html              # Interface da extensão
├── popup.css               # Estilos da interface
├── popup.js                # Lógica da interface e comunicação
├── /assets                 # Ícones e recursos visuais
│   ├── icon16.svg          # Ícone 16x16
│   ├── icon48.svg          # Ícone 48x48
│   └── icon128.svg         # Ícone 128x128
└── /utils                  # Módulos de utilidades
    ├── human-simulation.js # Simulação de comportamento humano
    ├── shadow-dom.js       # Manipulação do Shadow DOM
    └── hotmart-navigator.js # Navegação específica da Hotmart
```

## Instruções de Instalação

1. Clone o repositório ou extraia o arquivo ZIP
2. Acesse chrome://extensions/ no seu navegador
3. Ative o "Modo do desenvolvedor"
4. Clique em "Carregar sem compactação"
5. Selecione a pasta do projeto

## Como Usar

1. Clique no ícone da extensão após instalá-la
2. Selecione os arquivos para upload (capa, conteúdo principal, adicionais)
3. Configure as opções de timing e comportamento
4. Navegue até a página de upload da Hotmart
5. Clique em "Iniciar Automação"
6. A extensão irá detectar o contexto da página e realizar o upload automaticamente

## Customização

- **Timing**: Ajuste os valores de delay mínimo e máximo para simular diferentes velocidades de interação
- **Verificação**: Ative/desative a verificação automática de sucesso após uploads
- **Modo Lote**: Configure o tamanho dos lotes para upload de múltiplos arquivos
- **Arquivos**: Selecione diferentes tipos de arquivos para cada contexto de upload

## Changelog
Consulte o arquivo CHANGELOG.md para histórico de versões e atualizações.

## Resolução de Problemas
Consulte o arquivo RESOLUÇÃO_DE_ERRO.md para soluções de problemas comuns de instalação.

## Recursos Técnicos Avançados

### Simulação Humana
- Implementação de curvas Bezier para movimentos de mouse não-lineares
- Variação dinâmica de velocidade para simular aceleração/desaceleração natural
- Padrões de digitação com análise de proximidade de teclas
- Introdução de micro-hesitações e pequenos erros para naturalidade

### Manipulação Shadow DOM
- Travessia recursiva de shadow roots para encontrar elementos encapsulados
- Criação de seletores únicos para elementos dentro de múltiplos shadow roots
- Mapeamento de caminhos para acessar elementos em estruturas complexas
- Técnicas para aguardar elementos que ainda não foram renderizados

### Upload em Lote
- Processamento assíncrono para arquivos grandes
- Gerenciamento de memória para conjuntos de arquivos extensos
- Manipulação de upload em lotes para evitar travamentos do navegador
- Verificação de sucesso por lote com tratamento de erros individualizado