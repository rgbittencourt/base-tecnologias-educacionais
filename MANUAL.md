# Manual — Tecnologias Educacionais

## Identificação

- **Nome da aplicação:** Tecnologias Educacionais
- **Nome do repositório:** `base-tecnologias-educacionais`
- **Site público:** <https://rgbittencourt.github.io/base-tecnologias-educacionais/>
- **Repositório:** <https://github.com/rgbittencourt/base-tecnologias-educacionais>
- **Branch de publicação:** `v5`

## Para que serve

Esta aplicação é uma base pública de conhecimento sobre tecnologias educacionais. Ela reúne conceitos, termos, metodologias, plataformas, aplicações, recursos, pesquisas, referências e orientações de governança.

O site é produzido com Quartz a partir de arquivos Markdown e publicado automaticamente pelo GitHub Pages.

## Onde ficam os conteúdos

Todo conteúdo editorial está na pasta `content/`:

- `content/aplicacoes/`: aplicações práticas;
- `content/conceitos/`: conceitos fundamentais;
- `content/governanca/`: avaliação, acessibilidade, privacidade e contribuição;
- `content/mapas/`: mapas temáticos e trilhas de navegação;
- `content/pesquisas/`: panoramas e sínteses de evidências;
- `content/plataformas/`: plataformas e ferramentas;
- `content/recursos/`: produção e uso de recursos educacionais;
- `content/referencias/`: fontes, artigos e orientações de acesso;
- `content/tecnologias/`: tecnologias específicas;
- `content/termos/`: glossário de padrões e termos técnicos.

A página inicial é `content/index.md`.

## Como acrescentar um artigo ou material

1. Escolha a pasta temática adequada dentro de `content/`.
2. Crie um arquivo com extensão `.md` e nome curto, sem espaços. Exemplo: `avaliacao-formativa-digital.md`.
3. Comece o arquivo com metadados:

   ```yaml
   ---
   title: Avaliação formativa digital
   description: Síntese do tema e de suas aplicações educacionais.
   tags:
     - avaliacao
     - tecnologia-educacional
   ---
   ```

4. Organize o texto com títulos Markdown (`#`, `##`, `###`).
5. Inclua as referências reais e seus links ao final do texto.
6. Relacione o novo material às páginas existentes usando links internos. Exemplo: `[[conceitos/tecnologia-educacional|Tecnologia educacional]]`.
7. Revise autoria, data, acessibilidade, direitos de uso e funcionamento dos links.

## Como visualizar localmente

Na pasta do projeto, instale as dependências e inicie o servidor:

```bash
npm install
npx quartz build --serve
```

Depois, acesse o endereço exibido no terminal, normalmente <http://localhost:8080/>.

## Como publicar uma atualização

Depois de editar ou acrescentar materiais:

```bash
git add -A
git commit -m "conteudo: descrever a atualização"
git push origin v5
```

O fluxo `.github/workflows/deploy-pages.yaml` constrói o site e o publica automaticamente no GitHub Pages. A atualização costuma aparecer alguns minutos depois do envio.

## Como verificar a publicação

1. Abra a aba **Actions** do repositório.
2. Selecione **Publicar Quartz no GitHub Pages**.
3. Confirme que os trabalhos `build` e `deploy` foram concluídos com sucesso.
4. Acesse <https://rgbittencourt.github.io/base-tecnologias-educacionais/> e teste a página nova, a pesquisa e os links.

## Arquivos técnicos importantes

- `quartz.config.yaml`: nome, idioma, endereço e aparência do site;
- `quartz.ts`: composição e layout do Quartz;
- `package.json`: dependências e comandos;
- `pnpm-lock.yaml` e `package-lock.json`: versões reproduzíveis das dependências;
- `.github/workflows/deploy-pages.yaml`: publicação automática;
- `docs/`: documentação técnica do Quartz;
- `README.md`: apresentação e referência geral do projeto-base.

## O que não é armazenado no Git

As seguintes pastas são geradas automaticamente e não contêm conteúdo editorial original:

- `node_modules/`: dependências instaladas;
- `public/`: site compilado, recriado pelo GitHub Actions;
- `.quartz-cache/`: cache temporário da compilação;
- arquivos privados e configurações locais ignorados por `.gitignore`.

Essa exclusão mantém o repositório seguro, leve e reproduzível. O GitHub Pages conserva e publica o resultado compilado de cada implantação.

## Cuidados editoriais

- Use sempre **Design**, nunca “Desenho”, quando o conceito original for Design.
- Verifique se artigos, plataformas e casos citados existem de fato.
- Priorize fontes oficiais, artigos científicos e documentos institucionais.
- Não copie textos protegidos integralmente; faça sínteses e mantenha a referência.
- Não publique dados pessoais, senhas, tokens ou materiais sem autorização.
- Informe limitações, contexto e data de verificação das informações.

