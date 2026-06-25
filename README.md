# Marco Braida · Case File QA Sênior

Currículo visual de página única — um **dossiê** que demonstra, com evidências, a
operação no nível **QA Sênior**, usando IA como multiplicador sob supervisão humana.

> 100% estático · single-file · sem backend · sem rastreamento · gratuito para sempre.

🔗 **Demo:** `https://<seu-usuario>.github.io/` (após publicar — ver abaixo)

---

## Stack

- **HTML + CSS + JavaScript puro.** Zero framework, zero build, zero CDN de JS.
- **Gráficos nativos:** globo de partículas em `<canvas>` 2D + radar em SVG desenhado em runtime.
- **Fontes:** Space Grotesk + Instrument Serif + JetBrains Mono via **Google Fonts**
  (única dependência externa).
- **Acessibilidade:** foco visível por teclado, `prefers-reduced-motion` respeitado,
  contraste adequado.
- **Impressão:** `Ctrl+P` / botão "Salvar como PDF" geram um CV+dossiê com o tema
  escuro preservado (HUD, nav e globo são ocultados na impressão).

Tudo vive em um único arquivo: **`index.html`**.

---

## Rodar localmente

Basta abrir `index.html` no navegador. Para servir com um servidor local (recomendado
para testar fontes/print sem avisos de `file://`):

```bash
# Python 3
python -m http.server 8080
# depois acesse http://localhost:8080
```

---

## Publicar grátis no GitHub Pages

1. Crie um repositório **público** — para URL raiz, use o nome `seu-usuario.github.io`.
2. Suba os arquivos versionados na raiz (`index.html`, `LICENSE`, `.nojekyll`, etc.).
3. **Settings → Pages → Source:** branch `main`, pasta `/ (root)`.
4. Em ~1 min o site fica no ar em `https://seu-usuario.github.io/`.
5. (Opcional) Domínio próprio: aponte um CNAME no provedor e configure em Pages.

O arquivo `.nojekyll` evita que o GitHub Pages processe o site com Jekyll.

### Alternativas igualmente gratuitas (sem build)

| Serviço | Como | Limite free relevante |
|---|---|---|
| **Cloudflare Pages** | Conecta o repo, deploy a cada push | Builds/mês generosos; banda ilimitada |
| **Netlify** | Conecta o repo ou _drag-and-drop_ | 100 GB banda/mês |
| **Vercel** | Importa o repo (Hobby) | Uso pessoal/não-comercial |
| **GitLab Pages** | `.gitlab-ci.yml` mínimo | Cota free do GitLab |

Como é um único arquivo estático leve, **qualquer host estático gratuito** atende com
folga — sem risco de estourar limites de plano free.

---

## 🔒 Segurança por curadoria

Este repositório é **open-source**, então a estratégia de segurança é **não ter segredos**
(PRD §4.1): sem backend, sem API, sem token, sem variável de ambiente. O que não pode
ser público simplesmente **não existe no código**.

**Nunca versione** (já bloqueado em `.gitignore`):

- PRD-fonte e bundle de design (`PRD-*.md`, `*_offline_.html`) — contêm nomes internos.
- Relatórios internos detalhados, IDs de chamado, detalhes de vulnerabilidades.
- Estratégia pessoal de negociação salarial.
- Qualquer `.env`, chave, token ou credencial.

Materiais sensíveis ficam em **`_private/`** (ignorada pelo Git) e são levados *em
particular* à conversa de promoção — nunca para o site nem para o histórico do Git.

> Antes de cada commit: `git status` não deve mostrar nada de `_private/` nem dos
> arquivos-fonte sensíveis.

---

## Estrutura

```
.
├── index.html      # o site inteiro (conteúdo + estilos + scripts)
├── README.md       # este arquivo
├── LICENSE         # MIT
├── .gitignore      # curadoria de segurança — bloqueia o que é sensível
├── .nojekyll       # GitHub Pages sem Jekyll
└── _private/       # NÃO versionado — docs internos/sensíveis
```

---

## Personalização rápida

- **Contato:** botão "Falar comigo" usa `mailto:marcovdbraida@gmail.com`; botão
  **LinkedIn** aponta para `https://www.linkedin.com/in/marco-braida-465b6a96/`.
- **Cor de acento:** variável `--accent` no `<style>` (e `ACCENT` no script).
- **Conteúdo:** seções, métricas, casos e dossiê estão diretamente no `index.html`.

## Licença

[MIT](LICENSE) © 2026 Marco Braida.
