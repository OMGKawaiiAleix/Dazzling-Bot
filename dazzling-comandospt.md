# 🩷 Dazzling - Comandos e funcionalidades atuais

## `/embed` - Criar e administrar embeds personalizados

- `/embed create` - cria um embed novo (nome + pasta opcional)
- `/embed list` - lista seus embeds salvos, agrupados por pasta
- `/embed list-all` - lista os embeds de todos os usuários do servidor
- `/embed edit` - abre o editor visual de um dos seus embeds
- `/embed edit-other` *(somente Administradores)* - edita o embed de outra pessoa
- `/embed delete` - apaga um embed (com confirmação)
- `/embed rename` - renomeia um embed (atualiza automaticamente botões/vínculos/Boas-vindas/Boost/Despedida que o usassem)
- `/embed folder` - move um embed para uma pasta
- `/embed transfer` - transfere um dos seus embeds (ou uma pasta inteira) para outro usuário
- `/embed transfer-other` *(somente Administradores)* - força a transferência do embed de outra pessoa, sem que ela precise fazer nada

### Editor visual (botões)

Editar (título/descrição/cor), Texto (fora do embed), Autor, Footer, Imagens, Botões (de link ou que mostram outros embeds), Vincular embed, Renomear, Prévia, Enviar aqui, Outro canal, Webhook (nome/avatar personalizado), Cancelar.

### Placeholders disponíveis

- `{{user.mention}}`, `{{user.name}}`, `{{user.tag}}`, `{{user.id}}`, `{{user.avatar}}`, `{{user.memberNumber}}`
- `{{server.name}}`, `{{server.members}}`, `{{server.icon}}`, `{{server.boosts}}`
- `{{partner.name}}`, `{{partner.icon}}`, `{{partner.members}}`, `{{partner.link}}`, `{{partner.count}}`

---

## `/config` - Mensagens automáticas do servidor

- `/config welcome` - mensagem de boas-vindas (embed + canal)
- `/config boost` - mensagem de quando alguém dá boost
- `/config goodbye` - mensagem de quando alguém sai do servidor
- `/config disable` - desativa uma das três

---

## `/partner` - Alianças com outros servidores

- `/partner channel` - canal onde são detectados automaticamente os links de convite do Discord
- `/partner message` - seu próprio embed de resposta (ou o padrão, se você não configurar nenhum)
- Mantém a contagem de quantas alianças cada pessoa já fez (`{{partner.count}}`)

---

## `/autorole` - Atribuição automática de cargo por texto

Um único comando, tudo opcional (deixe vazio para ver o estado atual):

- `channel`, `text`, `give_role`, `remove_role` - canal, texto gatilho exato, cargo atribuído, cargo removido (opcional)
- `confirm_text` / `confirm_embed` / `confirm_disabled` - como é confirmado (texto próprio, um embed salvo, ou nada)
- `delay` - segundos até a confirmação se apagar sozinha (0 = nunca)
- `delete_trigger` - se também apaga a mensagem de quem escreveu o texto
- `disable` - desativa tudo

Mostra um embed de status tipo painel (✅/❌ para cada campo).

---

## `/language` - Idioma das respostas

Espanhol ou Português - afeta tudo o que o bot diz (confirmações, erros, `/help`), exceto nomes de comandos e placeholders, que sempre ficam em inglês.

---

## `/help` - Ajuda categorizada

Menu suspenso com: Embeds, Configuração do servidor, Partner, Auto-Cargo.

---

## Proteções e comportamento em segundo plano

- **Permissões:** todos os comandos (exceto `/help`) exigem "Gerenciar Servidor". `/embed edit-other` e `/embed transfer-other` exigem Administrador completo.
- **Cooldowns:** 3 segundos entre usos do mesmo comando por pessoa; 4 segundos por servidor para a detecção de Partner.
- **Isolamento de dados:** cada servidor tem suas informações completamente separadas.
- **Exclusão automática:** se a Dazzling for removida de um servidor, todos os dados desse servidor são apagados na hora (embeds, configurações, Partner, Auto-Cargo).
- **Privacidade:** não guarda conteúdo de mensagens fora do canal de Partner, nem dados de webhooks (são criados pelo Discord, a Dazzling não os armazena).
