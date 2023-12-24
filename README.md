# Birder: Sua Rede Social de Compartilhamento de Fotos 📸

Birder é uma plataforma de mídia social inspirada no Twitter, projetada para permitir que os usuários compartilhem fotos e socializem com outros entusiastas. Desenvolvida utilizando as tecnologias MongoDB, Express.js, React e Node.js (MERN stack), o Birder oferece uma experiência interativa e envolvente para os amantes de fotografias.

## Principais funcionalidades
Compartilhamento de Fotos: Publique suas fotos favoritas para que outros usuários possam apreciá-las e interagir.

Feed Personalizado: Personalize seu feed de acordo com suas preferências, seguindo outros usuários e recebendo atualizações de suas postagens.

Interação em Tempo Real: Curta, comente e compartilhe fotos em tempo real, proporcionando uma experiência social dinâmica.

Exploração de Conteúdo: Descubra novas fotos e perfis interessantes por meio da seção de exploração, mantendo-se conectado com a comunidade Birder.

## Tecnologias Utilizadas
O Birder foi desenvolvido utilizando a stack MERN (MongoDB, Express.js, React e Node.js), proporcionando uma base sólida e eficiente para a construção de uma aplicação web moderna e escalável.

# Rotas (backend)
CREATE USER
```
POST http://localhost:3001/auth/register

Ex: Body - Raw - JSON
{
    "firstName": "exemplo",
    "lastName": "teste",
    "email": "exemploteste@email.com",
    "password": "123456",
    "picturePath": "p6.jpeg",
    "friends": [],
    "location": "Cidade",
    "occupation": "Profissao"
}
```
LOGIN USER
```
POST http://localhost:3001/auth/login

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: Body - Raw - JSON
{
    "email": "exemploteste@email.com",
    "password": "123456"
}
```
CREATE POST
```
POST http://localhost:3001/posts/<userId>/post
obs: substitua <userId> pelo Id do usuário desejado para realizar novo post

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: Body - Raw - JSON
{
    "picturePath": "p6.jpeg",
    "description":"testeNovo"
}
```
GET POSTS
```
GET http://localhost:3001/posts

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: None
```
GET USER POSTS
```
GET http://localhost:3001/posts/<userId>/posts
obs: substitua <userId> pelo Id do usuário desejado para realizar novo post

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: None
```
DELETE POSTS
```
DELETE http://localhost:3001/posts/<postId>
obs: substitua <postId> pelo Id desejado para deletar post

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: None
```
GET USER
```
GET http://localhost:3001/users/<userId>
obs: substitua <userId> pelo Id do usuário desejado para realizar novo post

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: None
```
GET USER FRIENDS
```
GET http://localhost:3001/users/<userId>/friends
obs: substitua <userId> pelo Id do usuário desejado para realizar novo post

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: None
```
ADD & REMOVE FRIENDS
```
PATCH http://localhost:3001/users/<userId>/<friendId>
obs: substitua <userId> pelo Id do usuário desejado para realizar novo post e <friendId> pelo Id do usuário que deseja adicionar como amigo

obs: insira o token gerado no registro dentro de 'Authorization' 'type: Bearer token' no Postman

Ex: Body - Raw - JSON
{
  "action": "add"
}
or
{
  "action": "remove"
}
```
# FrontEnd

Desenvolvi um frontEnd com React. Nele organizei a estrutura usando componentes e widgtes para melhor organização e reaproveitamento de códigos.
Fiz uso do multer para trabalhar com imagens e jogar no banco de dados. 
Conexão com o backend com endpoints e salvando tudo no mongoDB.
Save de usuario em local Storage.
Estilização inspirada em redes sociais ja existentes.

