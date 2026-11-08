# omnx-ia-auditar-agente

Guia visual: abra o `COMO-FUNCIONA.html` desta pasta (dois cliques; funciona sem internet).

Testa um agente, chatbot ou automação com IA já construído: revisa as instruções, monta casos de teste (fora de escopo, falha de ferramenta, manipulação, ação irreversível, memória), roda ou conduz os testes e entrega relatório com taxa de acerto, problemas priorizados e veredito.

## O que ela não faz

- Só aponta os problemas: não altera o agente.
- Construir, corrigir ou publicar o agente é com o agente **Agenor**.
- Quando só existe o texto das instruções, o teste é simulado e não libera o agente para ir ao ar.

## Como instalar

**Direto do GitHub:** no Claude Code, diga: "Instale a skill a partir de https://github.com/Empire-Business/omnx-ia-auditar-agente". Para atualizar, diga: "Atualize a skill a partir de https://github.com/Empire-Business/omnx-ia-auditar-agente". A IA baixa e copia os arquivos.

Se você já baixou esta pasta:

1. Abra o Claude Code (no aplicativo do Claude, aba **Code**, ambiente **Local**).
2. Escreva: **"Instale a skill que está nesta pasta: `<caminho desta pasta>`"**.
3. Você vai ver a IA copiando os arquivos. Não precisa digitar comando nenhum.
4. Abra uma conversa nova e faça um pedido, como nos exemplos abaixo.

### Instalar à mão

- **Mac ou Linux:** rode `bash install.sh` a partir desta pasta. A skill é copiada para `~/.claude/skills/omnx-ia-auditar-agente`.
- **Windows:** copie esta pasta para `%USERPROFILE%\.claude\skills\omnx-ia-auditar-agente`, ou peça para a IA fazer isso. O `install.sh` não é usado no Windows.
- **Outra ferramenta (Codex e outras):** ainda **não foi testada no Codex**. Peça para a IA da ferramenta seguir a seção "Outra ferramenta (Codex e outras)" do `SKILL.md` e contar o que funcionou.

Precisa de Python 3 para rodar o script. Se não tiver, a skill avisa e segue pela leitura, sem contagem automática. Testada só no Mac até agora.

## Como pedir

- "Testa meu agente antes de eu colocar no ar."
- "Tenta quebrar esse bot da minha loja."
- "Faz o QA deste assistente: (arquivo de instruções)"

## O que tem na pasta

| Arquivo | Para que serve |
|---|---|
| `SKILL.md` | o passo a passo que a IA segue |
| `references/checklist.md` | o que olhar nas instruções e ideias de caso de teste |
| `scripts/consolidar_testes.py` | calcula taxas e sugere o veredito; só lê |
| `COMO-FUNCIONA.html` | guia visual |
| `install.sh` | instalação no Mac ou Linux |

## Versões

- 1.0 (08/11/2026): primeira versão.
