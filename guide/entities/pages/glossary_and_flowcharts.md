
---  
uid: Guides.Entities.Glossary  
title: Glossario & Diagramas
---

# Tipo de Entidades  
Uma lista de todas as entidades Discord.Net suas propriedades e para quais outras elas podem ser convertidas  

> [!NOTE]
> Todas as interfaces têm a mesma árvore de herança para entidades `Socket` e `Rest`.  
> As entidades marcadas em vermelho são exclusivas do projeto de origem.


## Canais 
![IChannelChart]
<img style="background-color: #FFFFFF;" src="https://raw.githubusercontent.com/Edaurodo/d-net-doc-translation-pt-BR/main/guide/entities/diagrams/Channels.svg">  

### Canais de mensagem
* Canal de **Texto** ([ITextChannel]) Representa um canal de texto de uma Guilda.
* Canal de **Tópico** ([IThreadChannel]) Representa um canal de Tópico de uma Guilda.
* Canal de **Anúncio** ([INewsChannel]) Representa um canal de Anúncio de uma Guilda.
* Canal de **DM** ([IDMChannel]) Representa um de DM.
* Canal em **Grupo** ([IGroupChannel]) Representa um canal de DM em grupo e implementa **IPrivateChannel**.  
  - Raramente é usado pois os Bots não conseguem acessar.
* Canal **Privado** ([IPrivateChannel]) Representa um canal de DM ou Grupo; 
* Canal de **Mensagem** ([IMessageChannel]) Pode ser quais quer dos canais a cima.  

### Canais diversos  
* Canal de **Guilda** ([IGuildChannel]) Representa um canal genérico de uma Guilda.
* Canal de **Voz** ([IVoiceChannel]) Representa um canal de vóz de uma Guilda.
* Canal de **Palco** ([IStageChannel]) Representa um canal de palco de uma Guilda.
* Canal de **Categoria** ([ICategoryChannel]) Representa uma categoria de uma Guilda.
* Canal **Aninhado** ([INestedChannel]) Representa uma canal que (esta ligado/pode existir) em uma categoria de uma Guilda.  
* Canan **Canal** ([IChannel]) Pode ser qualquer um citado a cima

[ITextChannel]: xref:Discord.ITextChannel
[IThreadChannel]: xref:Discord.IThreadChannel
[INewsChannel]: xref:Discord.INewsChannel
[IDMChannel]: xref:Discord.IDMChannel
[IGroupChannel]: xref:Discord.IGroupChannel
[IPrivateChannel]: xref:Discord.IPrivateChannel
[IMessageChannel]: xref:Discord.IMessageChannel

[IGuildChannel]: xref:Discord.IGuildChannel
[IVoiceChannel]: xref:Discord.IVoiceChannel
[IStageChannel]: xref:Discord.IStageChannel
[ICategoryChannel]: xref:Discord.ICategoryChannel
[INestedChannel]: xref:Discord.INestedChannel
[IChannel]: xref:Discord.IChannel

## Mensagens
![IMessageChart]  
<img style="background-color: #FFFFFF;" src="https://raw.githubusercontent.com/Edaurodo/d-net-doc-translation-pt-BR/main/guide/entities/diagrams/Messages.svg">  

* A **Rest Followup Message** ([RestFollowupMessage]) É uma mensagem retorna pelo acompanhamento da interação.
* A **Rest Interaction Message** ([RestInteractionMessage]) É uma mensagem retornada pela resposta original da interação.
* A **Rest User Message** ([RestUserMessage]) É uma mensagem enviada por REST; pode ser qualquer uma das opções acima.
* A **User Message** ([IUserMessage])  É uma mensagem enviada por uma usuário.
* A **System Message** ([ISystemMessage]) É uma mensagem enviada pelo proprio Discord.
* A **Message** ([IMessage]) Pode ser qualquer uma citada a cima.

[RestFollowupMessage]: xref:Discord.Rest.RestFollowupMessage
[RestInteractionMessage]: xref:Discord.Rest.RestInteractionMessage
[RestUserMEssage]: xref:Discord.Rest.RestUserMessage
[IUserMessage]: xref:Discord.IUserMessage
[ISystemMessage]: xref:Discord.ISystemMessage
[IMessage]: xref:Discord.IMessage

## Usuários  
![IUserChart]  
<img style="background-color: #FFFFFF;" src="https://raw.githubusercontent.com/Edaurodo/d-net-doc-translation-pt-BR/main/guide/entities/diagrams/Users.svg">

* O **Guild User** ([IGuildUser]) É um usuário disponivél dentro de uma Guilda.
* O **Group User** ([IGroupUser]) É um usuário disponivél dentro de uma Grupo
	- Isto é raramente usado ja que Bots não conseguem entrar em grupos.
* O **Self User** ([ISelfUser]) É o usuário do próprio Bot o qual o client esta logado no momento.
* O **User** ([IUser]) Quais quer um dos citados a cima.

[IGuildUser]: xref:Discord.IGuildUser
[IGroupUser]: xref:Discord.IGroupUser
[ISelfUser]: xref:Discord.ISelfUser
[IUser]: xref:Discord.IUser

## Interacões
![IInteractionChart]  
<img style="background-color: #FFFFFF;" src="https://raw.githubusercontent.com/Edaurodo/d-net-doc-translation-pt-BR/main/guide/entities/diagrams/Interactions.svg">

* O **Slash command** ([ISlashCommandInteraction]) É um commando de aplicativo ("/") que é executado na caixa de texto, com parametros.
* A **Message Command** ([IMessageCommandInteraction]) É um commando de aplicativo direcionado a uma mensagem.
* O **User Command** ([IUserCommandInteraction]) iÉ um commando de aplicativo direcionado a um usuário.
* O **Application Command** ([IApplicationCommandInteraction]) Quais quer uma das citadas a cima.
* A **Message component** ([IMessageComponent]) É uma interação com um botão/dropmenu quando é clicado\selecionado.
* O **Autocomplete Interaction** ([IAutocompleteinteraction]) iÉ uma interação que é concluida automaticamente.
* A **Interaction** ([IDiscordInteraction]) Quais quer uma das citadas a cima.

[ISlashCommandInteraction]: xref:Discord.ISlashCommandInteraction
[IMessageCommandInteraction]: xref:Discord.IMessageCommandInteraction
[IUserCommandInteraction]: xref:Discord.IUserCommandInteraction
[IApplicationCommandInteraction]: xref:Discord.IApplicationCommandInteraction
[IMessageComponent]: xref:Discord.IMessageComponent
[IAutocompleteinteraction]: xref:Discord.IAutocompleteInteraction
[IDiscordInteraction]: xref:Discord.IDiscordInteraction

## Outros tipos:
### Emoji

* O **Emote** ([Emote]) É um emoji personalizado de uma Guilda.
	- Exemplo: `<:dotnet:232902710280716288>`
* O **Emoji** ([Emoji]) É um emoji Unicode.
	- Exemplo: `👍`

[Emote]: xref:Discord.Emote
[Emoji]: xref:Discord.Emoji

### Stickers
* O **Sticker** ([ISticker]) iÉ um sticker padrão do Disocrd.
* O **Custom Sticker** ([ICustomSticker]) É um sticker personalizado de uma Guilda.

[ISticker]: xref:Discord.ISticker
[ICustomSticker]: xref:Discord.ICustomSticker

### Atividade
* O **Game** ([Game]) Se refere a atividade **jogando** de um usuário.
* A **Rich Presence** ([RichGame]) Se refere atividade **jogando** detalhado do **Game**
	- Visite [Rich Presence Intro] na documentação do Discord para mais informações.
* A **Streaming Status** ([StreamingGame]) Se refere a atividade do usuário quando esta stremando na twitch.
* A **Spotify Status** ([SpotifyGame]) (V2.0+) Se refere a atividade do usuario que esta escutando uma música no **Spotify**
activity for listening to a song on Spotify.

[Game]: xref:Discord.Game
[RichGame]: xref:Discord.RichGame
[StreamingGame]: xref:Discord.StreamingGame
[SpotifyGame]: xref:Discord.SpotifyGame
[Rich Presence Intro]: https://discord.com/developers/docs/rich-presence/best-practices