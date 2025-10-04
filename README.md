#🍔 QuickBite – Aplicativo de Lanchonete em Flutter

🧩 Visão Geral

O QuickBite é um aplicativo mobile desenvolvido em Flutter, criado como projeto escolar por nosso grupo para simular o funcionamento de uma lanchonete digital.

O app permite:

Fazer login;

Ver o cardápio com produtos, preços e imagens;

Pesquisar itens pelo nome;

Favoritar produtos;

Adicionar ao carrinho e finalizar o pedido.

Nosso foco foi criar uma interface moderna, funcional e bonita, usando conceitos essenciais de Flutter como widgets, navegação, estados e listas dinâmicas.

👥 Equipe

(Aqui vocês podem colocar os nomes e funções de cada um)
Exemplo:

Ana Lima — Interface, organização do projeto e lógica principal

João Silva — Estrutura das páginas e integração das rotas

Maria Souza — Documentação, testes e refinamento do design

🏗️ Estrutura do Projeto
lib/
├── main.dart                 → Arquivo principal e rotas
├── models/
│   └── product.dart          → Modelo de dados (produto)
├── pages/
│   ├── login_page.dart       → Tela de login
│   ├── home_page.dart        → Tela inicial (lista e pesquisa)
│   ├── cart_page.dart        → Tela do carrinho
│   ├── favorites_page.dart   → Tela de favoritos
├── widgets/
│   └── product_tile.dart     → Componente visual de produto

💡 O que Aprendemos

Durante o desenvolvimento, cada parte do app foi uma oportunidade de aprender algo novo sobre Flutter e desenvolvimento mobile:

Tema	O que aprendemos	Onde aplicamos
Widgets	Diferença entre StatelessWidget e StatefulWidget	Login, Home e Cards de produtos
Gerenciamento de Estado	Atualizar a tela com setState()	Favoritos, pesquisa e carrinho
Navegação	Usar Navigator.pushNamed e rotas nomeadas	Login → Home → Carrinho/Favoritos
Layouts	Organizar elementos com Column, Row, ListView	Interface do cardápio
Modelos de Dados	Criar classes para representar objetos	Arquivo product.dart
Design Moderno	Usar Material 3 e Google Fonts	Tema visual do app
AlertDialog	Criar pop-ups de confirmação	Finalização do pedido
Funções Lambda e Map/Fold	Manipular listas de forma elegante	Soma do total do carrinho
🧠 Explicando Nossas Funções
🏁 main.dart

Criamos a função main() como ponto de entrada do app:

void main() => runApp(const QuickBiteApp());


E dentro do QuickBiteApp, configuramos:

O tema do app com ThemeData;

As rotas para navegação entre telas;

O uso da fonte Poppins via Google Fonts.

🔐 login_page.dart

Foi a primeira tela feita.
Usamos TextField para capturar email e senha e um ElevatedButton que leva o usuário para a Home com:

Navigator.pushReplacementNamed(context, '/home');


Aprendemos que o pushReplacementNamed substitui a tela atual — útil pra que o usuário não volte ao login com o botão “voltar”.

🏠 home_page.dart

Aqui aprendemos bastante sobre estado e listas dinâmicas:

Mantivemos uma lista de produtos;

Filtramos essa lista em tempo real conforme o usuário digitava na barra de pesquisa;

Adicionamos lógica de favoritos e carrinho com setState().

🛍️ product_tile.dart

Criamos um widget reutilizável para exibir produtos com imagem, nome, preço e botões:

Um botão de coração ❤️ para favoritos;

Um botão de carrinho 🛒 para adicionar ao pedido.

Aprendemos a reaproveitar código e a passar dados entre widgets com parâmetros.

🛒 cart_page.dart

Implementamos a soma do total com:

double total = cart.fold(0, (sum, item) => sum + item.price);


Aprendemos sobre a função fold, que acumula valores dentro de uma lista — bem útil para cálculos sem loops manuais.

❤️ favorites_page.dart

Filtramos produtos com:

final favorites = products.where((p) => p.isFavorite).toList();


Aqui aprendemos sobre métodos de filtragem e listas no Dart.

🎨 Design e Estilo

Usamos Material 3 e Google Fonts (Poppins);

Adotamos uma paleta amarela e branca, inspirada em fast-foods;

Mantivemos espaçamento e sombras suaves para dar um ar moderno.

🚀 Como Executar o Projeto

Certifique-se de ter o Flutter instalado (flutter doctor).

Clone este repositório:

git clone https://github.com/teu-usuario/quickbite.git


Acesse a pasta:

cd quickbite


Instale as dependências:

flutter pub get


Execute no emulador ou celular Android:

flutter run

🧭 Próximos Passos

Nosso grupo pretende aprimorar o app adicionando:

Login com Firebase 🔥

Persistência de dados locais (shared_preferences);

Tela de perfil e histórico de pedidos;

Splash screen animada com o logo do QuickBite 🍔.

💬 Conclusão

Esse projeto nos ensinou muito sobre trabalho em equipe, lógica de programação e design de interfaces.
Construímos o QuickBite do zero, testamos funções novas, erramos bastante 😅 e aprendemos o suficiente pra entender como um app real de delivery funciona por dentro.
