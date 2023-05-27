# Tipo de Entidades  
Uma lista de todas as entidades Discord.Net suas propriedades e para quais outras elas podem ser convertidas  

> Todas as interfaces têm a mesma árvore de herança para entidades `Socket` e `Rest`.  
As entidades marcadas em vermelho são exclusivas do projeto de origem.

## Canais  

### Canais de mensagem

* Canal de **Texto** ([ITextChannel](https://discordnet.dev/api/Discord.ITextChannel.html)) Representa um canal de texto de uma Guilda.
* Canal de **Tópico** ([IThreadChannel](https://discordnet.dev/api/Discord.IThreadChannel.html)) Representa um canal de Tópico de uma Guilda.
* Canal de **Anúncio** ([INewsChannel](https://discordnet.dev/api/Discord.INewsChannel.html)) Representa um canal de Anúncio de uma Guilda.
* Canal de **DM** ([IDMChannel](https://discordnet.dev/api/Discord.IDMChannel.html)) Representa um de DM.
* Canal em **Grupo** ([IGroupChannel](https://discordnet.dev/api/Discord.IGroupChannel.html)) Representa um canal de DM em grupo e implementa **IPrivateChannel**.  
 * Raramente é usado pois os Bots não conseguem acessar.
* Canal **Privado** ([IPrivateChannel](https://discordnet.dev/api/Discord.IPrivateChannel.html)) Representa um canal de DM ou Grupo; 
* Canal de **Mensagem** ([IMessageChannel](https://discordnet.dev/api/Discord.IMessageChannel.html)) Pode ser quais quer dos canais a cima.

### Canais diversos

* Canal de **Guilda** ([IGuildChannel]()) Representa um canal genérico de uma Guilda.
* Canal de **Voz** ([IVoiceChannel]()) Representa um canal de vóz de uma Guilda.
* Canal de **Palco** ([IStageChannel]()) Representa um canal de palco de uma Guilda.
* Canal de **Categoria** ([ICategoryChannel]()) Representa uma categoria de uma Guilda.
* Canal **Aninhado** ([INestedChannel]()) Representa uma canal que (esta ligado/pode existir) em uma categoria de uma Guilda.
