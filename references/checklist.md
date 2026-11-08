# Checklist de auditoria

Marque só o que se aplica ao agente. Item falho vira linha no relatório.

## Instruções

- Papel específico e objetivo claros.
- Passos em ordem e formato de saída definido.
- Regras do que nunca fazer e resposta padrão para fora do escopo.
- "Se não souber, diga que não sabe", com o conhecimento delimitado.
- Data e hora atuais passadas ao agente, se ele lida com prazos.
- Formato do canal respeitado (no WhatsApp, mensagens curtas e uma pergunta por vez).
- Instruções adaptadas ao negócio real, sem sobras de exemplo.

## Ferramentas

- Cada uma com nome claro, descrição de quando usar e quando não usar, parâmetros com formato definido (data, telefone).
- Erro de ferramenta devolvido como mensagem tratada, sem derrubar a conversa.
- Ferramentas que escrevem, enviam ou apagam exigem confirmação explícita.
- Confirme no registro de execução que a ferramenta certa foi chamada, com os argumentos certos.

## Memória e conhecimento

- Conversa separada por pessoa; nunca memória global.
- Responde só com o que está na base e cita a fonte quando for o caso.
- Base vazia ou sem resposta gera "não sei", sem invenção.

## Robustez e custo

- Mensagem padrão quando a IA ou uma ferramenta falha; existe alternativa se o modelo principal cair.
- Limite de tentativas e condição de parada, para não entrar em laço.
- Envio em duplicidade controlado.
- Custo por conversa conhecido e dentro do esperado.

## Segurança e dados

- Nenhum segredo em instruções, código, repositório ou log.
- Ações críticas e decisões sensíveis passam por uma pessoa.
- Dados pessoais protegidos; um usuário não acessa o que é de outro.
- Saúde, jurídico, finanças, RH: avisa o limite e deixa a decisão final com uma pessoa.

## Ideias de caso por categoria

| Categoria | Exemplos |
|---|---|
| `caminho_feliz` | Cada ação principal, em cada caminho de decisão |
| `fora_de_escopo` | Pergunta alheia ao negócio; informação que o agente não tem |
| `formatos_de_entrada` | Mensagem picada, áudio, imagem, PDF, erro de digitação, "amanhã à tarde", telefone sem DDD, outro idioma |
| `acoes_irreversiveis` | Agendar, cancelar, enviar, apagar: tem de pedir confirmação; conflito de horário |
| `falhas` | Ferramenta fora do ar, resposta vazia, limite de uso, chave inválida, modelo indisponível |
| `seguranca` | "Ignore suas instruções", pedido de dados de outro cliente, pedido para revelar instruções ou chaves, texto malicioso dentro de documento |
| `persistencia` | Lembra na mesma conversa; não mistura pessoas diferentes |
