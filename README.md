# Social Media IG Audit EV

Skill para auditoria pública de Instagram e Social Media, com alinhamento de escopo antes da execução, coleta de evidências públicas, fallback com Apify, diagnóstico de perfil/bio/feed/Reels/copy, jornada do usuário, calendário editorial e HTML consolidado.

## O que a skill entrega

- Solicitação inicial de informações, links e objetivo da auditoria.
- Pedido/verificação do `APIFY_API_TOKEN` antes do mapeamento.
- Proposta de escopo para aprovação antes de coletar dados.
- Auditoria da jornada do usuário a partir de IG/FB/outros canais.
- Raio-X da bio com pontos bons, pontos a melhorar, boas práticas e ajustes sugeridos.
- Análise de engajamento público, feed, Reels, copy, formatos e funil orgânico.
- Guia de formatos de conteúdo com função, público, momento de uso e boas práticas.
- Plano de mídia e calendário editorial de 30 dias.
- Plano de ação com checklist de melhorias para 0-30 e 31-60 dias.
- HTML final consolidado e autocontido, com evidências embutidas quando disponíveis.

## Como instalar

Copie a pasta da skill para o diretório de skills do seu agente:

```text
.agents/skills/social-media-IG-AuditEV/
```

A estrutura esperada é:

```text
social-media-IG-AuditEV/
  SKILL.md
  agents/
    openai.yaml
```

Depois, invoque a skill pelo nome:

```text
$social-media-IG-AuditEV
```

## Compatibilidade

O arquivo principal é o `SKILL.md`. Ele foi escrito para funcionar como instrução autossuficiente em qualquer IDE, agente ou modelo de IA que consiga ler Markdown.

O arquivo `agents/openai.yaml` é apenas um metadado opcional para ambientes compatíveis com esse formato. Quem usa outro agente, IDE ou modelo pode ignorar esse arquivo e usar somente o `SKILL.md`.

## Dependências

A skill não depende de nenhuma outra skill.

Ferramentas como Apify, AppSorteos, Firecrawl, SimilarWeb, Ubersuggest, navegador público ou busca web são apoios opcionais para coleta de dados e evidências. Se alguma delas não estiver disponível, o agente deve usar uma alternativa pública equivalente, pedir arquivos/prints ao usuário ou registrar a limitação no relatório.

## Como usar

Informe ao agente que deseja auditar um perfil de Instagram ou Social Media. A skill deve primeiro pedir:

- Nome do cliente.
- Nicho, mercado, cidade/região e público-alvo.
- Links do Instagram, Facebook, TikTok, LinkedIn ou outros canais.
- Site, landing page, WhatsApp, catálogo ou link principal de conversão.
- Objetivo principal da auditoria.
- Concorrentes ou benchmarks, se houver.
- Pasta de saída desejada.
- Chave `APIFY_API_TOKEN`, caso queira capturas e dados públicos via Apify.

A execução só deve começar depois da aprovação do escopo.

## Requisitos

- Um agente compatível com skills em formato `SKILL.md`.
- Acesso público aos perfis e links auditados.
- `APIFY_API_TOKEN` opcional, mas recomendado para coleta de dados e evidências visuais do Instagram.

## Segurança e limitações

- Não inclua chaves de API dentro deste repositório.
- A skill trabalha com dados públicos, salvo autorização explícita para sessão logada.
- Métricas privadas como alcance, impressões, salvamentos, cliques, retenção, GA4, Search Console e CRM devem ser tratadas como próxima camada de análise quando não houver acesso.
