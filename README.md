# Plano para Site de Consumo Consciente e Economia Sustentável

## Visão Geral
Este plano detalha a criação de um site estático com cinco páginas HTML interligadas sobre o tema "Consumo Consciente e Economia Sustentável." Cada página seguirá as melhores práticas do HTML5, incluirá estilos CSS externos, navegação comum, tratamento de erros em elementos de imagem e uso adequado de tags semânticas. Um arquivo favicon.ico deve ser adicionado à raiz do site. Todas as páginas incluem comentários para explicar seções do código para clareza e depuração.

---

## Estrutura de Arquivos
```
/
├── index.html
├── problema.html
├── solucoes.html
├── estatisticas.html
├── acoes.html
├── styles.css (arquivo CSS principal)
├── favicon.ico
└── images/ (pasta para imagens locais, se necessário)
```

---

## Mudanças Globais e Melhores Práticas

### Estrutura HTML Base
Cada página começará com:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <link rel="stylesheet" href="styles.css">
    <title>[Título Específico da Página]</title>
</head>
<body>
    <!-- Conteúdo da Página -->
</body>
</html>
```

### Menu de Navegação (Comum a Todas as Páginas)
```html
<!-- Início da navegação -->
<nav class="main-nav">
    <ul class="nav-list">
        <li><a href="index.html" class="nav-link">Início</a></li>
        <li><a href="problema.html" class="nav-link">Problemas</a></li>
        <li><a href="solucoes.html" class="nav-link">Soluções</a></li>
        <li><a href="estatisticas.html" class="nav-link">Estatísticas</a></li>
        <li><a href="acoes.html" class="nav-link">Ações</a></li>
    </ul>
</nav>
<!-- Fim da navegação -->
```

---

## Arquivo CSS (styles.css)

### Estilos Globais
- Reset básico e tipografia
- Estilos para navegação
- Classes utilitárias (cores, espaçamentos, etc.)
- Estilos responsivos

### Classes Específicas
- `.main-nav` - Navegação principal
- `.nav-list` - Lista de navegação
- `.nav-link` - Links de navegação
- `.hero-section` - Seção principal
- `.problem-list` - Lista de problemas
- `.solution-table` - Tabela de soluções
- `.stats-container` - Container de estatísticas
- `.contact-form` - Formulário de contato
- `.highlight-text` - Texto destacado
- `.quote-section` - Seção de citações

---

## Mudanças Arquivo por Arquivo

### index.html
**Head & Title:**
- `<title>Consumo Consciente e Economia Sustentável - Início</title>`

**Body:**
- Navegação comum no topo
- Header com `<h1>` introduzindo o tema
- Seção hero com classe `.hero-section`
- Parágrafo introdutório usando `<strong>`, `<em>`, e `<u>` para ênfase
- Imagem principal:
```html
<img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/223edcf9-18d5-40d5-a455-1ef629a55b16.png"
     alt="Banner representando economia sustentável e consumo consciente com design minimalista moderno"
     class="hero-image"
     onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0c6b6ac2-4817-45f8-be13-4e431a48887f.png';">
```
- Footer com informações de copyright

---

### problema.html
**Head & Title:**
- `<title>Problemas do Consumo e Sustentabilidade</title>`

**Body:**
- Navegação comum
- Seção explicando questões principais usando `<ul class="problem-list">`
- Lista de problemas: "Excesso de consumo", "Desperdício de recursos", "Impacto ambiental negativo"
- `<blockquote class="quote-section">` com citação de especialista
- Spans com classes para destacar problemas: `<span class="highlight-danger">`
- Footer com comentários inline

---

### solucoes.html
**Head & Title:**
- `<title>Soluções para Economia Sustentável</title>`

**Body:**
- Navegação comum
- Tabela comparativa com classe `.solution-table`:
```html
<table class="solution-table">
    <thead>
        <tr>
            <th>Solução</th>
            <th>Benefícios</th>
            <th>Desafios</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Uso de Energias Renováveis</td>
            <td>Redução de emissões</td>
            <td>Investimento inicial</td>
        </tr>
        <!-- Mais linhas conforme necessário -->
    </tbody>
</table>
```
- Containers `<div>` com classes (ex: `class="solution-section"`)
- Links externos com `target="_blank"` e `rel="noopener"`

---

### estatisticas.html
**Head & Title:**
- `<title>Estatísticas sobre Consumo e Economia</title>`

**Body:**
- Navegação comum
- Container principal com classe `.stats-container`
- Imagem de gráfico:
```html
<img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d1d33f17-aa07-4052-a0a1-d6e9646dd39f.png"
     alt="Gráfico detalhado demonstrando estatísticas de consumo consciente e economia sustentável com design limpo"
     class="stats-chart"
     onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/71b1e61c-a56f-48e8-915f-fd9d69693a33.png';">
```
- Iframe para visualização de dados:
```html
<iframe src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e7bd7eed-aa0e-49b8-9c02-2d190c3f0ae6.png"
        title="Iframe exibindo visualização de dados de economia sustentável"
        class="data-iframe">
</iframe>
```
- Seções marcadas com IDs (ex: `<div id="dados-estatisticos">`)

---

### acoes.html
**Head & Title:**
- `<title>Ações Práticas e Contato</title>`

**Body:**
- Navegação comum
- Formulário de contato com classe `.contact-form`:
```html
<form method="post" action="#" class="contact-form">
    <div class="form-group">
        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" required>
    </div>
    
    <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
    </div>
    
    <div class="form-group">
        <label for="mensagem">Mensagem:</label>
        <textarea id="mensagem" name="mensagem" required></textarea>
    </div>
    
    <button type="submit" class="submit-btn">Enviar</button>
</form>
```
- Div com informações de contato adicionais com classe `.contact-info`
- Footer

---

## Tratamento de Erros e Testes

### Imagens
- Cada tag `<img>` usa atributo `onerror` para carregar imagem de fallback
- Alt text descritivo para acessibilidade

### Formulário
- Atributos `required` nos campos do formulário
- Validação HTML5 básica

### Validação
- Validar cada arquivo HTML com validador padrão
- Verificar CSS com validador CSS

### Testes Cross-browser
- Testar todos os links de navegação
- Verificar design responsivo em diferentes dispositivos
- Testar funcionalidade em principais navegadores

---

## Resumo de Entregáveis

### Arquivos HTML (5)
- `index.html` - Página inicial com introdução
- `problema.html` - Explicação dos problemas
- `solucoes.html` - Soluções propostas
- `estatisticas.html` - Dados e estatísticas
- `acoes.html` - Ações práticas e contato

### Arquivo CSS (1)
- `styles.css` - Estilos centralizados para todo o site

### Recursos Adicionais
- `favicon.ico` - Ícone do site
- Imagens placeholder com fallbacks apropriados

### Características Técnicas Implementadas
- Estrutura HTML5 semântica
- CSS externo separado do HTML
- Navegação consistente entre páginas
- Elementos de formulário com validação
- Tabelas para organização de dados
- Listas ordenadas e não ordenadas
- Elementos de bloco e inline
- Classes e IDs para estilização
- Iframes para conteúdo externo
- Tratamento de erros em imagens
- Design responsivo
- Comentários HTML explicativos

---

Após a aprovação do plano, criarei um rastreador (TODO.md) para acompanhar a execução das etapas do plano, atualizando-o a cada passo concluído.
