
## Definições Gerais

- Todo órgão terá um ponto focal para ser o contato com o ED,  preferencialmente, quem for o responsável pela área de dados no órgão.
- Este ponto focal será o Administrador da Pasta e/ou do Projeto.
- O ponto focal será responsável pelo compartilhamento dos dados, quando solicitado por algum ator interno ou externo.
- Ele indicará os usuários conforme o nível de permissão de acesso (Editor ou Leitor).
- O ponto focal também será responsável por conceder o nível de acesso.
- O papel de editor será responsável pela edição necessária nas tabelas que o leitor (analista) julgar pertinente.

## Definição dos papéis de acesso

- Trata-se do nível de permissão concedida aos usuários, divididos em três níveis:administrador, editor, leitor e base.

O papel base foi criado para visualização da existência das bases de dados. Com ele, pode-se listar as bases existentes, mas não pode consultar, ler os dados.
O ponto focal, automaticamente, terá seu acesso definido como __Administrador__. Portanto, definirá qual papel os técnicos de seu órgão poderão exercer.

## Compartimentação do projeto e definindo acesso aos dados

Em caso de órgãos que contenham unidades administrativas (sub-órgãos) com bases de dados próprias, projetos específicos, e independência relativa à gestão de dados, o acesso, assim como a divisão do Projeto na GCP ocorrerá da seguinte maneira:

O acesso será por grupos distintos, restringindo acesso apenas ao sub-órgão pertinente do usuário. A inserção do usuário ao sub-grupo acontecerá no momento da concessão da credencial de acesso ao Datalake.

__Ex.:__

__Projeto:__ SMFP

__Dataset’s:__  RH e EGP

__Acesso:__ Grupo Leitor RH e Grupo Leitor EGP