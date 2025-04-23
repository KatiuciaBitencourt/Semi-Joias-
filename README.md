# Semi-Joias-
"Beleza que transcende o tempo: nossas semi joias foram feitas para iluminar seu estilo e destacar a sua essência."
<!DOCTYPE html><html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Katiucia Bitencourt - Semi Joias e Personalizados</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #fff8f0;
      color: #333;
    }
    header, footer {
      background-color: #d4a373;
      color: white;
      text-align: center;
      padding: 1em;
    }
    nav {
      background-color: #f3d2b7;
      display: flex;
      justify-content: center;
      gap: 1em;
      padding: 1em;
    }
    nav a {
      color: #333;
      text-decoration: none;
      font-weight: bold;
    }
    main {
      padding: 2em;
    }
    section {
      margin-bottom: 2em;
    }
    .produto {
      border: 1px solid #ccc;
      padding: 1em;
      margin: 1em 0;
      border-radius: 8px;
    }
    button {
      background-color: #d4a373;
      color: white;
      border: none;
      padding: 0.5em 1em;
      border-radius: 5px;
      cursor: pointer;
    }
    #carrinho {
      border: 1px solid #ccc;
      padding: 1em;
      margin-top: 2em;
      border-radius: 8px;
      background-color: #fafafa;
    }
  </style>
</head>
<body>
  <header>
    <h1>Katiucia Bitencourt</h1>
    <p>Semi Joias e Personalizados</p>
  </header>
  <nav>
    <a href="#home">Início</a>
    <a href="#produtos">Produtos</a>
    <a href="#sobre">Sobre</a>
    <a href="#contato">Contato</a>
  </nav>
  <main>
    <section id="home">
      <h2>Bem-vindo à nossa loja!</h2>
      <p>Descubra semi joias exclusivas e itens personalizados feitos com carinho e atenção aos detalhes. Aqui, cada peça conta uma história.</p>
    </section><section id="produtos">
  <h2>Nossos Produtos</h2>
  <div class="produto">
    <h3>Correntepersonalizada</h3>
    <p>R$ 79,90</p>
    <button onclick="adicionarAoCarrinho('Produto Exemplo', 99)">Comprar</button>
  </div>
  <div class="produto">
    <h3>Produto Teste</h3>
    <p>R$ 120,00</p>
    <button onclick="adicionarAoCarrinho('Produto Teste', 120)">Comprar</button>
  </div>

  <div id="carrinho">
    <h3>Carrinho</h3>
    <ul id="itensCarrinho"></ul>
    <p><strong>Total: R$ <span id="totalCarrinho">0.00</span></strong></p>
  </div>
</section>

<section id="sobre">
  <h2>Sobre Katiucia Bitencourt</h2>
  <p>Com amor por design e dedicação à beleza única de cada detalhe, Katiucia Bitencourt criou esta loja para compartilhar sua paixão por semi joias e personalização.</p>
</section>

<section id="contato">
  <h2>Fale Conosco</h2>
  <p>Entre em contato pelo Instagram ou WhatsApp para fazer seu pedido ou tirar dúvidas. Estamos sempre prontos para te atender com carinho!</p>
  <p><a href="https://wa.me/5517981931636" target="_blank"><button>WhatsApp</button></a></p>
  <p><a href="https://instagram.com/katiuciabitencourt" target="_blank"><button>Instagram</button></a></p>
</section>

  </main>
  <footer>
    <p>&copy; 2025 Katiucia Bitencourt. Todos os direitos reservados.</p>
  </footer>  <script>
    let carrinho = [];

    function adicionarAoCarrinho(nome, preco) {
      carrinho.push({ nome, preco });
      atualizarCarrinho();
    }

    function atualizarCarrinho() {
      const lista = document.getElementById('itensCarrinho');
      const totalSpan = document.getElementById('totalCarrinho');
      lista.innerHTML = '';
      let total = 0;
      carrinho.forEach(item => {
        const li = document.createElement('li');
        li.textContent = `${item.nome} - R$ ${item.preco.toFixed(2)}`;
        lista.appendChild(li);
        total += item.preco;
      });
      totalSpan.textContent = total.toFixed(2);
    }
  </script></body>
</html>
