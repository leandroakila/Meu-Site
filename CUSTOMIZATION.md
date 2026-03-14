# 🎨 Guia de Customização - LN Sistemas

Este guia explica como personalizar o site da LN Sistemas de acordo com suas necessidades.

---

## 1️⃣ Alterar Cores do Site

### Localização: `css/style.css` (linhas 14-22)

```css
:root {
    --color-primary: #0A2540;      /* Azul escuro - cor principal */
    --color-secondary: #1E90FF;    /* Azul tecnológico - destaques */
    --color-white: #FFFFFF;        /* Branco */
    --color-light-gray: #F8F9FA;   /* Cinza claro - fundos */
    --color-gray: #6C757D;         /* Cinza - textos secundários */
    --color-dark-gray: #343A40;    /* Cinza escuro - textos */
    --color-success: #28A745;      /* Verde - sucesso */
    --color-whatsapp: #25D366;     /* Verde WhatsApp */
}
```

### Como usar:
- Altere os valores hexadecimais (#0A2540) pelas suas cores
- As cores serão aplicadas automaticamente em todo o site

### Exemplos de paletas:

**Paleta Azul/Laranja:**
```css
--color-primary: #003366;
--color-secondary: #FF6B35;
```

**Paleta Verde:**
```css
--color-primary: #0D3B2E;
--color-secondary: #10B981;
```

**Paleta Roxo:**
```css
--color-primary: #3B0764;
--color-secondary: #A855F7;
```

---

## 2️⃣ Alterar Fonte (Tipografia)

### Localização: Todas as páginas HTML (linha 10)

**Fonte atual:** Inter

**Para alterar:**

1. Escolha uma fonte no [Google Fonts](https://fonts.google.com/)
2. Copie o link de importação
3. Substitua em todas as páginas HTML:

```html
<!-- Exemplo: Trocar para Roboto -->
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
```

4. No `css/style.css`, altere:
```css
--font-main: 'Roboto', sans-serif;
```

**Fontes recomendadas:**
- **Poppins** - Moderna e arredondada
- **Montserrat** - Elegante e profissional
- **Open Sans** - Limpa e legível
- **Raleway** - Sofisticada

---

## 3️⃣ Adicionar Logo da Empresa

### Opção 1: Substituir o ícone do cubo

Em todas as páginas HTML, localize:
```html
<div class="nav-brand">
    <i class="fas fa-cube"></i>
    <span>LN Sistemas</span>
</div>
```

Substitua por:
```html
<div class="nav-brand">
    <img src="images/logo.png" alt="LN Sistemas" style="height: 40px;">
    <span>LN Sistemas</span>
</div>
```

### Opção 2: Logo completo (sem texto)

```html
<div class="nav-brand">
    <img src="images/logo-completo.png" alt="LN Sistemas" style="height: 45px;">
</div>
```

---

## 4️⃣ Personalizar Conteúdo dos Serviços

### Localização: `servicos.html`

Para adicionar/remover/editar serviços:

```html
<div class="service-item">
    <div class="service-icon">
        <i class="fas fa-ICONE-AQUI"></i> <!-- Altere o ícone -->
    </div>
    <div class="service-content">
        <h2>Título do Serviço</h2>
        <p>Descrição do serviço...</p>
        <ul class="service-list">
            <li><i class="fas fa-check"></i> Item 1</li>
            <li><i class="fas fa-check"></i> Item 2</li>
        </ul>
    </div>
</div>
```

**Encontrar ícones:** [Font Awesome Icons](https://fontawesome.com/icons)

---

## 5️⃣ Personalizar Soluções

### Localização: `solucoes.html`

Para adicionar nova solução:

```html
<div class="solution-card">
    <div class="solution-icon">
        <i class="fas fa-SEU-ICONE"></i>
    </div>
    <h3>Nome da Solução</h3>
    <p>Descrição da solução...</p>
</div>
```

---

## 6️⃣ Alterar Informações de Contato

### Email
Busque e substitua em todos os arquivos:
- `contato@lnsistemas.com` → seu email

### WhatsApp
**Arquivo:** `js/main.js` (linha 98)
```javascript
const whatsappNumber = '5562999999999';
```

**Formato:** `55` (Brasil) + `DDD` + `Número`

**Exemplos:**
- São Paulo: `5511987654321`
- Rio: `5521987654321`
- Goiânia: `5562987654321`

### Localização
Busque e substitua:
- `Goiânia - GO - Brasil` → sua cidade

---

## 7️⃣ Adicionar Redes Sociais no Rodapé

### Localização: Rodapé em todas as páginas

Adicione após `<div class="footer-about">`:

```html
<div class="footer-social">
    <h4>Redes Sociais</h4>
    <div style="display: flex; gap: 1rem; font-size: 1.5rem;">
        <a href="https://facebook.com/suapagina" target="_blank" style="color: #1E90FF;">
            <i class="fab fa-facebook"></i>
        </a>
        <a href="https://instagram.com/suapagina" target="_blank" style="color: #1E90FF;">
            <i class="fab fa-instagram"></i>
        </a>
        <a href="https://linkedin.com/company/suaempresa" target="_blank" style="color: #1E90FF;">
            <i class="fab fa-linkedin"></i>
        </a>
    </div>
</div>
```

---

## 8️⃣ Personalizar Mensagem do Hero Banner

### Localização: `index.html` (linhas 35-38)

```html
<h1 class="hero-title">Seu novo título aqui</h1>
<p class="hero-subtitle">Seu novo subtítulo aqui</p>
```

**Dicas para um bom título:**
- Seja direto e claro
- Foque no benefício para o cliente
- Use verbos de ação
- Máximo 10-12 palavras

---

## 9️⃣ Adicionar Google Analytics

### Passo 1: Criar conta
1. Acesse [analytics.google.com](https://analytics.google.com)
2. Crie uma propriedade para seu site
3. Copie o código de medição

### Passo 2: Adicionar em todas as páginas
Cole antes do `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🔟 Adicionar Imagens Reais

### Passo 1: Criar pasta
```
projeto/
├── images/
│   ├── hero-background.jpg
│   ├── sobre.jpg
│   ├── servico-1.jpg
│   └── logo.png
```

### Passo 2: Usar no HTML
```html
<img src="images/sua-imagem.jpg" alt="Descrição">
```

### Passo 3: Otimizar imagens
- **Tamanho máximo:** 1920px largura
- **Formato:** JPG (fotos) ou PNG (logos)
- **Peso:** < 200KB por imagem
- **Ferramentas:** TinyPNG, Squoosh

---

## 1️⃣1️⃣ Alterar Vantagens (Cards)

### Localização: `index.html` - seção advantages

```html
<div class="advantage-card">
    <div class="advantage-icon">
        <i class="fas fa-SEU-ICONE"></i>
    </div>
    <h3>Título da Vantagem</h3>
    <p>Descrição da vantagem...</p>
</div>
```

---

## 1️⃣2️⃣ Personalizar Processo (Passos)

### Localização: `index.html` - seção process

Para adicionar/remover passos:

```html
<div class="process-step">
    <div class="step-number">5</div>
    <h3>Título do Passo</h3>
    <p>Descrição do passo...</p>
</div>
```

---

## 1️⃣3️⃣ Adicionar Depoimentos de Clientes

### Criar nova seção após "Vantagens"

```html
<section class="testimonials-section">
    <div class="container">
        <h2>O que nossos clientes dizem</h2>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <p>"Excelente trabalho! O sistema transformou nossa empresa."</p>
                <h4>João Silva</h4>
                <span>Empresa XYZ</span>
            </div>
            <!-- Mais depoimentos -->
        </div>
    </div>
</section>
```

### Adicionar CSS

```css
.testimonials-section {
    background-color: var(--color-light-gray);
    padding: 80px 0;
}

.testimonials-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
}

.testimonial-card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.08);
}

.testimonial-card p {
    font-style: italic;
    color: var(--color-gray);
    margin-bottom: 1.5rem;
}

.testimonial-card h4 {
    color: var(--color-primary);
    margin-bottom: 0.25rem;
}

.testimonial-card span {
    color: var(--color-gray);
    font-size: 0.9rem;
}
```

---

## 📱 Testar Alterações

Após qualquer customização:

1. **Salve os arquivos**
2. **Atualize o navegador** (Ctrl+F5 ou Cmd+Shift+R)
3. **Teste em mobile** (F12 → modo responsivo)
4. **Verifique no console** (F12) se há erros

---

## 🆘 Precisa de Ajuda?

Se algo não funcionar após customizar:

1. Desfaça a última alteração
2. Salve e teste novamente
3. Verifique o console do navegador (F12)
4. Certifique-se de fechar todas as tags HTML corretamente

---

**Boas customizações! 🎨**
