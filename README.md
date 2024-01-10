# hugchat-twitchtv-integration

Simples integração entre o HugginChat (IA Generativa) e a plataforma de livestreaming Twitch TV

# Como usar
## Configurando o browser
- Baixe o Google Chrome, crie um perfil no navegador e guarde seu ID, achado em 'Caminho de perfil' em 'chrome://version/'. A intenção é salvar os cookies para usar no código
  - Exemplo: C:\Users\User\AppData\Local\Google\Chrome\User Data\Profile 4 | o Id é 'Profile 4'
- Vá até https://www.twitch.tv , crie um perfil dedicado ao bot e outro para você caso não tenha. De preferência verifique email e senha

## Configurando o código
- coloque o ID do perfil (no exemplo 'Profile 4') em > pipeline.ipynb > classe Utils (segundo bloco) > variável 'profile_name'
- configure os parâmetros da classe Chatbot:
  - botIdName = nome de usuário do bot
  - botName = nome de interpretação do bot
  - fileName = arquivo de texto da engenharia de prompt
  - streamId = nome de usuário da livestream/chat a ser utilizada
  - pronouns = gênero do bot (não utilizado atualmente)
  - mainUser = usuário que controlará o bot
  - email = seu email no site da HuggingFace
  - first_use = a senha só é necessária no primeiro uso, depois serão utilizado cookies
  - password = sua senha no site da HuggingFace
 
## Engenharia de prompt
- Existem 3 exemplos de engenharia de prompt em ./Utils/characters:
  - butler.txt = personalidade de mordomo
  - helto_hater.txt = interpreta alguém que desgosta do streamer Helto
  - hinata.txt = interpreta a personagem Hinata de Naruto
 
## Conversando com o bot
- Vá até o chat do usuário colocado em streamId
- Converse com o bot utilizando @{botIdName} para referir-se à ele
  - exemplo:
  - input: Olá @HinataBot1
  - output: Olá! sou Hinata Hyuga! Como posso ajudar?
- Vídeo de demonstração: https://www.youtube.com/watch?v=NNnyIk61I5g

## Próximos passos
- Resolver problemas de condordância e principalmente de gênero
- Mudança de linguagem abrupta
- Versão com ChatGPT
