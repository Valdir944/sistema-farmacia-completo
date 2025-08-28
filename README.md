Sistema de Farmácia XYZ - Protótipo

Descrição

O Sistema de Farmácia XYZ é um protótipo web para gerenciamento de vendas, estoque e relatórios de uma farmácia. Desenvolvido em PHP com MySQL e suporte a PDF via LaTeX, o sistema oferece uma interface simples e responsiva para gerenciar produtos, registrar vendas e gerar relatórios detalhados. O protótipo suporta modo claro/escuro e é projetado para ser fácil de configurar e testar.

Funcionalidades





Gerenciamento de Vendas (index.php):





Busca incremental de produtos por nome ou código de barras via AJAX.



Adição de produtos a uma tabela de vendas com validação de quantidade (limitada pelo estoque).



Cálculo automático do total da venda.



Finalização de vendas com registro no banco de dados.



Exibição de mensagens de sucesso (ex.: após exclusão de produto em estoque.php).



Gerenciamento de Estoque (estoque.php):





Adição, atualização e exclusão de produtos.



Validação de entradas (nome, preço, quantidade).



Notificação de produtos com estoque esgotado.



Coluna de status ("Disponível" ou "Esgotado") na tabela de produtos.



Redirecionamento para index.php após exclusão de produto.



Relatórios de Vendas (relatorios.php):





Filtro de vendas por período (data de início e fim).



Relatórios detalhados por dia, semana, mês e ano (quantidade vendida e total).



Lista de produtos vendidos com quantidade e subtotal.



Exportação de relatórios para PDF usando LaTeX.



Visualização de itens de cada venda via AJAX.



Interface:





Estilização consistente com modo claro/escuro (via css/estilo.css).



Responsividade para telas menores (máximo 768px).



Mensagens de feedback (ex.: sucesso ou erro) com estilização.

Estrutura do Projeto

farmacia-xyz/
├── app/
│   └── funcoes_db.php      # Funções de acesso ao banco de dados
├── css/
│   └── estilo.css          # Estilos CSS (modo claro/escuro, responsividade)
├── js/
│   ├── main.js             # Lógica do modo escuro
│   └── vendas.js           # Lógica de busca e vendas (AJAX)
├── api/
│   └── buscar_produto.php  # API para busca incremental de produtos
├── index.php               # Página de vendas
├── estoque.php             # Página de gerenciamento de estoque
├── relatorios.php          # Página de relatórios
├── erros.log               # Log de erros
└── README.md               # Este arquivo
