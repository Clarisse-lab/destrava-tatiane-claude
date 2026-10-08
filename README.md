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
  INSTALLMENT: "R$XX,XX"   // valor da parcela em "Ou 12x de ..."
};
```

- Com `CHECKOUT_URL` vazio, todos os botões rolam até a oferta. Quando estiver preenchido, todos levam ao checkout e repassam os parâmetros da URL (UTMs etc.).
- **Teste A/B do topo:** a página abre com a Seção 1 A. Acesse com `?v=b` para exibir a Seção 1 B.

## Estrutura
- `index.html`: página completa (estilos e scripts embutidos)
- `assets/fonts/`: DM Sans (fonte da identidade visual, hospedada localmente; licença OFL)
- `assets/img/`: prints de prova social
- `assets/maphel-icone.svg`, `assets/favicon.svg`: símbolo da marca
