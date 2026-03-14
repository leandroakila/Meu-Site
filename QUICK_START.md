# 🚀 Guia Rápido - LN Sistemas

## Como começar

1. **Abrir o site localmente:**
   - Abra o arquivo `index.html` no seu navegador
   - Ou use Live Server (VS Code) para melhor experiência

2. **Configurar WhatsApp:**
   - Abra `js/main.js`
   - Linha 98: Altere `5562999999999` para seu número real

3. **Personalizar conteúdo:**
   - Edite os arquivos `.html` para alterar textos
   - Os ícones são do Font Awesome (já incluído)

## 📞 Importante: Número do WhatsApp

⚠️ **ATENÇÃO:** Atualize o número do WhatsApp no arquivo `js/main.js`:

```javascript
// Linha 98
const whatsappNumber = '5562999999999'; // ← Altere aqui
```

Formato do número: `55` (código BR) + `62` (DDD) + `999999999` (número)

## 🎨 Alterar Cores

Edite o arquivo `css/style.css` (linhas 14-18):

```css
:root {
    --color-primary: #0A2540;      /* Azul escuro principal */
    --color-secondary: #1E90FF;    /* Azul tecnológico */
    --color-white: #FFFFFF;        /* Branco */
    --color-light-gray: #F8F9FA;   /* Cinza claro de fundo */
}
```

## 📱 Testar Responsividade

No navegador:
- Pressione `F12` para abrir DevTools
- Clique no ícone de dispositivo móvel
- Teste diferentes resoluções

## 🌐 Publicar o Site

### Opção 1: GitHub Pages (Grátis)
1. Crie conta no GitHub
2. Crie repositório novo
3. Faça upload dos arquivos
4. Ative GitHub Pages em Settings

### Opção 2: Netlify (Grátis)
1. Acesse netlify.com
2. Arraste a pasta do projeto
3. Site publicado instantaneamente!

### Opção 3: Vercel (Grátis)
1. Acesse vercel.com
2. Conecte seu GitHub
3. Deploy automático

## ✅ Checklist Antes de Publicar

- [ ] Atualizei o número do WhatsApp
- [ ] Revisei todos os textos
- [ ] Testei em mobile
- [ ] Testei o formulário de contato
- [ ] Verifiquei todos os links
- [ ] Email correto em todas as páginas

## 📄 Arquivos do Projeto

```
📁 Projeto LN Sistemas
├── 📄 index.html          → Página inicial
├── 📄 servicos.html       → Página de serviços
├── 📄 solucoes.html      → Página de soluções
├── 📄 sobre.html         → Página sobre
├── 📄 contato.html       → Página de contato
├── 📁 css/
│   └── 📄 style.css      → Todos os estilos
├── 📁 js/
│   └── 📄 main.js        → JavaScript (interatividade)
├── 📄 README.md          → Documentação completa
└── 📄 QUICK_START.md     → Este arquivo
```

## 🎯 Principais Funcionalidades

✨ **Menu responsivo** - Funciona em celular, tablet e desktop
✨ **Formulário de contato** - Envia mensagem direto pelo WhatsApp
✨ **Animações suaves** - Elementos aparecem ao rolar a página
✨ **Botão voltar ao topo** - Aparece ao rolar para baixo
✨ **Máscara de telefone** - Formata automaticamente
✨ **Design moderno** - Visual profissional e limpo

## 💡 Dicas

1. **Adicionar imagens reais:**
   - Crie pasta `images/`
   - Adicione suas imagens
   - Substitua os ícones por `<img src="images/sua-imagem.jpg">`

2. **Alterar logo:**
   - Crie um logo em PNG
   - Salve como `images/logo.png`
   - Substitua o ícone no navbar

3. **Google Analytics:**
   - Crie conta no Google Analytics
   - Adicione o código antes do `</head>` em todas as páginas

## 🐛 Problemas Comuns

**Menu mobile não abre?**
- Verifique se `js/main.js` está carregando
- Abra F12 e veja se há erros no Console

**Formulário não envia?**
- Verifique o número do WhatsApp
- Teste em dispositivo real (não funciona bem em alguns simuladores)

**Estilos não aplicados?**
- Verifique o caminho do CSS
- Certifique-se que `css/style.css` existe

## 📞 Suporte

Precisa de ajuda? Revise o arquivo `README.md` para documentação completa.

---

**Sucesso com seu site! 🚀**

LN Sistemas - Soluções inteligentes em sistemas e automação de processos
