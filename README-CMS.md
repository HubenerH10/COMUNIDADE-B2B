# Comunidade B2B · Grupo José Alves — site editável

Site no GitHub Pages com painel de edição. Quem edita não mexe em código:
abre o painel, preenche, publica — e grava no seu GitHub sozinho.

Recomendado: **Pages CMS** (painel hospedado, o jeito mais fácil de gerir).

## Estrutura dos arquivos

```
index.html             → o site (layout). Quase nunca muda.
.pages.yml             → o que o painel deixa editar (já pronto).
content/
  noticias.json        → notícias / últimas atualizações  (editável)
  empresas.json        → status das 3 empresas            (editável)
  indicadores.json     → report mensal, os números        (editável)
  relatorios.json      → lista de relatórios para download (editável)
  uploads/             → imagens enviadas pelo painel
  arquivos/            → relatórios (Excel/PDF) enviados pelo painel
admin/                 → (opcional) painel alternativo Sveltia — pode ignorar
```

## Como colocar no ar (mais fácil) — Pages CMS

1. **Subir no GitHub.** Crie um repositório (ex.: `comunidade-b2b`) e suba todos estes arquivos, mantendo as pastas.
2. **Ligar o GitHub Pages.** No repositório: Settings → Pages → Source: branch `main` → Save. Em ~1 min o site fica no ar.
3. **Abrir o painel.** Acesse `https://app.pagescms.org`, entre com sua conta GitHub e instale o app no seu repositório (pode liberar só esse repo).
4. **Editar.** O Pages CMS lê o `.pages.yml` e já mostra os formulários: Notícias, Status das empresas, Report mensal e Relatórios. Edite, clique em salvar — ele faz o commit e o site atualiza sozinho.

Não precisa de servidor nem de configuração técnica. O login é o do próprio GitHub.

## O que dá para editar
- **Notícias e atualizações** — título, categoria, data e imagem (arrastar-e-soltar).
- **Status das empresas** — número, estágio, barra, responsáveis, data.
- **Report mensal (números)** — os valores da tabela de indicadores, por empresa.
- **Relatórios mensais (arquivos)** — suba o Excel/PDF do mês; aparece como download no site.

## Quem pode postar
Só quem você liberar no Pages CMS / como colaborador do repositório no GitHub.
O controle de quem publica é o próprio GitHub — exatamente o que você queria.

## Observações
- Abrir o `index.html` com duplo-clique mostra o conteúdo de exemplo; os dados reais carregam quando o site está publicado.
- A pasta `admin/` traz uma alternativa (Sveltia CMS) caso um dia queira um painel próprio no domínio — para começar, ignore.
- Migrar para SharePoint/Power Pages depois é tranquilo: o conteúdo já está separado em `content/`.
