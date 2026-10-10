# Plano Destrava Empresa — Landing page

Página de vendas do **Plano Destrava Empresa** (Maphel · Tatiane Resende), em HTML/CSS/JS estático e sem build. Pronta para o Netlify.

## Deploy no Netlify
1. Netlify → *Add new site* → *Import an existing project* → selecione este repositório.
2. Build command: deixe em branco. Publish directory: `.` (já definido em `netlify.toml`).

## O que editar antes de publicar
No final do `index.html`, no bloco `CONFIG`:

```js
var CONFIG = {
  CHECKOUT_URL: "",        // link do checkout (Hotmart, Kiwify, Eduzz...)
  INSTALLMENT: "",         // valor da parcela, ex.: "R$30,72" (vazio = linha "Ou 12x de" oculta)
  INSTAGRAM: "",           // perfil oficial sem @, ex.: "maphel" (vazio = não aparece no rodapé)
  PRIVACY_URL: "",         // link da Política de Privacidade
  TERMS_URL: ""            // link dos Termos de Uso
};
```

- Com `CHECKOUT_URL` vazio, todos os botões rolam até a oferta. Quando estiver preenchido, todos levam ao checkout e repassam os parâmetros da URL (UTMs etc.).
- **Teste A/B do topo:** a página abre com a Seção 1 A. Acesse com `?v=b` para exibir a Seção 1 B.

## Estrutura
- `index.html`: página completa (estilos e scripts embutidos)
- `assets/fonts/`: DM Sans (fonte da identidade visual, hospedada localmente; licença OFL)
- `assets/img/`: foto da Tatiane e prints de prova social
- `assets/favicon.svg`: ícone da aba do navegador (letra "m" do nome maphel)
