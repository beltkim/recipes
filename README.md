# Livro de Receitas da Família

Static site served via GitHub Pages.

## Structure

```
gh-pages/
├── index.html                  ← main cookbook page (password: receitas2024)
├── .nojekyll                   ← disables Jekyll so filenames with _ work
├── README.md
└── assets/
    └── original_recipes/       ← recipe photos (123 images, ~13 MB)
```

## Deploy

```bash
# First time
git init
git checkout -b gh-pages
git add .
git commit -m "deploy cookbook"
git remote add origin https://github.com/YOUR_USER/YOUR_REPO.git
git push -u origin gh-pages

# Updates
git add .
git commit -m "update cookbook"
git push
```

Then in GitHub → repo Settings → Pages → Branch: **gh-pages** / folder: **/ (root)**.

Your site will be live at `https://YOUR_USER.github.io/YOUR_REPO/`

## Changing the password

Run this in any browser console to get the hash for your new password:

```js
crypto.subtle.digest('SHA-256', new TextEncoder().encode('yourpassword'))
  .then(b => console.log(Array.from(new Uint8Array(b)).map(x=>x.toString(16).padStart(2,'0')).join('')))
```

Then replace `PASS_HASH` near the bottom of `index.html` with the output.

## Receitas (226)

- Almôndegas ao Molho de Tomate
- Almôndegas com Batata Assada e Queijo
- Ameixas Recheadas
- Arroz Doce
- Aspargo com Vinagrete de Tomate
- Baba de Moca
- Babbalucci (Caracóis Sicilianos com Tomate e Ervas)
- Bacalhau ao Forno
- Barrinhas de Mirtilo com Estragão e Farofa
- Batata Frita Gratinada com Bacon
- Batatas "Fritas" no Forno
- Batida de Abacaxi
- Beirute de Palmito
- Berinjela para Comer com Pao
- Berinjela Recheada
- Bibimbap Caseiro
- Biscoito Quebra-quebra
- Biscoitos Caseiros Folhados
- Biscoitos de Aveia com Manteiga de Amendoim (Sem Ovos)
- Bolacha da Mae
- Bolinho de Chuchu Delicioso e Leve
- Bolinho de Mandioca Frito
- Bolinho de Polvilho e Fuba
- Bolinhos de Laranja
- Bolinhos de Legumes com Molho Ranch de Ervas
- Bolo Assado com Recheio de Doce de Leite
- Bolo Bem-Casado
- Bolo da Felicidade
- Bolo de 150 Gramas
- Bolo de Abacaxi com Hortelã
- Bolo de Abobrinha
- Bolo de Banana
- Bolo de Banana com Aveia
- Bolo de Banana e Canela
- Bolo de Café
- Bolo de Cenoura
- Bolo de Chocolate com Recheio e Cobertura
- Bolo de Chocolate de Ana Valeria
- Bolo de Coco com Ameixa
- Bolo de Cream Cheese Sem Ovos com Farofa Crocante
- Bolo de Fubá (Simples)
- Bolo de Fubá com Goiabada
- Bolo de Fubá Cremoso I
- Bolo de Fubá Cremoso II
- Bolo de Fubá Inglês Sem Ovos
- Bolo de Laranja
- Bolo de Laranja com Casca
- Bolo de Laranja Fofinho e Molhadinho
- Bolo de Laranjinha
- Bolo de Maçã
- Bolo de Maçã com Castanha, Nozes e Canela
- Bolo de Merengue de Limão
- Bolo de Milho com Coco
- Bolo de Milho da Tonha
- Bolo de Milho Super Cremoso
- Bolo de Noz de Abacaxi Cremoso
- Bolo de Nozes
- Bolo de Paçoca
- Bolo de Tapioca
- Bolo Delícia de Chocolate
- Bolo Doce de Leite
- Bolo Encanto
- Bolo Floresta Negra (Black Forest Cake)
- Bolo Fofinho
- Bolo Formigueiro
- Bolo Gelado
- Bolo Gelado Coco
- Bolo Gelado de Abacaxi
- Bolo Gelado de Coco
- Bolo Gelado de Pêssego com Chantilly Ácido e Pistaches
- Bolo Low Carb de Banana e Ameixa
- Bolo mousse coco (Sandra)
- Bolo Pao de Lo
- Bolo Prestígio
- Bolo Queijadinha Cremosa
- Bolo Regina Barroso
- Bolo Surpresa de Carne
- Bolos de Arroz
- Bombocado de Fuba
- Bowls de Frango Grego
- Brigadeiro
- Brigadeiro Dietetico
- Brigadeiros Gourmet — 9 Sabores
- Broa de Amendoim
- Broa de Fuba
- Brownie de Chocolate
- Cacarola Italiana
- Canoricole (Tia Helenice)
- Canoricole (Vo Cina)
- Casquinhas — Amendoim Doce
- Ceviche de Camarão Vermelho com Abacate e Milho
- Chantilly Diet
- Chantininho Resistente para Decoração de Bolos
- Cheesecake
- Chester Recheado com Frutas Secas e Nozes
- Chá com Espuma de Cream Cheese
- Chè Chuối (Sobremesa Vietnamita de Banana, Tapioca e Leite de Coco)
- Cobertura de Marshmallow
- Cookies S'mores Sem Ovos (Grossos, Cremosos e Estilo Confeitaria)
- Costeletas de Porco na Frigideira com Funcho e Maçã
- Coxas de Frango Crocantes com Espinafre e Molho de Mostarda
- Creme da Tonha
- Creme de Papaia Light
- Crepes de Queijo Fresco com Tomates
- Croquembouche
- Crostini de Manga com Redução de Balsâmico
- Crème Brûlée de Café com Especiarias
- Cuca de Banana (Batedeira)
- Cueca Virada
- Cupcakes de Aniversário Sem Ovos (Com Surpresa Dentro!)
- Cuque de Uva
- Donuts
- Efo Riro (Refogado Nigeriano de Folhas Verdes)
- Ensopado de Carne Nigeriano
- Escargots à la Bourguignonne (Caracóis com Manteiga de Ervas)
- Espaguete Gratinado ao Forno
- Falsa 'Nduja
- Farofa de Cenoura, Bacon e Azeitona
- Farofa de Queijo Coalho, Banana-da-Terra e Calabresa
- Farofa Fria
- Farofa Fria de Tomates e Azeitonas
- Fatias Húngaras de Coco e Leite Condensado
- Feijão Branco
- Frango Assado Recheado com Farofa
- Frango à Francesa Sem Ovos
- Frappuccino de Baunilha Caseiro
- Ganache de Chocolate
- Ganache Low Carb
- Geleia de Jabuticaba
- Gruste
- Ka'ak al Quds (Pão de Gergelim de Jerusalém)
- Khorovats (Espetinhos Armênios)
- Lagarto Temperado
- Legumes ao Queijo
- Lombo Recheado de Palmito
- Losh Kebab (Hambúrgueres Grelhados Armênios)
- Madeleines
- Malloreddus alla Campidanese (Massa Sarda Canelada com Açafrão e Ragù de Porco)
- Mansaf (Cordeiro Palestino com Arroz e Molho de Iogurte)
- Margarita de Melancia
- Maria Mole
- Massa Cremosa de Limão com Aspargos
- Massa de Pao
- Massa de Pizza Caseira Perfeita
- Massa de Pizza na Chapa
- Massa Podre para Torta Doce
- Moin Moin (Bolinho de Feijão Cozido no Vapor à Nigeriana)
- Molho Basico de Tomates
- Molho Bechamel
- Molho de Tomate Cru
- Molho Shack
- Mousse de Maracuja
- Muffins de Morango com Farinha Integral e Streusel
- Nhoque Suíço com Palmito e Alho-Poró
- Nós de Babka de Chocolate Sovados à Mão
- Omelete ao Forno
- Pamonha de Colher
- Pancakes de Banana sem Gluten
- Panetone Light
- Panetone Salgado com Calabresa
- Panetone Salgado com Presunto e Queijo
- Panqueca de Aveia
- Pao de Banana
- Pao de Queijo Light
- Pao Italiano
- Pao Liquidificador
- Paoziho de Leite
- Papelón com Limão (Limonada Venezuelana)
- Pasta de Alho (3 versoes)
- Pate de Tomate Seco
- Pave Rapido de Limao
- Pe-de-moleque
- Pernil Caramelizado
- Peru Especial de Ceia
- Pizza Mineira
- Pizza Rapida
- Pudim de Leite Condensado da Vovo
- Pudim de Leite Condensado MOÇA
- Pudim de Sorvete
- Pudim FIT sem Açúcar
- Pudim Mesclado de Chocolate e Ninho
- Puntarelle à Romana (Salada de Puntarelle com Molho de Anchova e Alho)
- Pão de Pêssego e Cenoura com Especiarias
- Pão Low Carb com Farinha de Amêndoas
- Pão Recheado de Carne Moída
- Quindim
- Rabanada
- Receita de Massa para Empada, Empadao e Tortas Salgadas
- Refresco de Abacaxi com Hortelã
- Rosa di Parma (Filé de Porco Recheado com Presunto Cru)
- Rosca da Vo Tonha
- Rosquinha de Queijo
- Salada Caprese
- Salada Caprese Clássica
- Salada de Burrata com Morango
- Salada de Couve com Molho de Limão
- Salada de Feijão Marbella
- Salada de Macarrao e Atum
- Salada de Massa Caesar com Frango
- Salada Sanduíche de Presunto
- Salada Verde com Vinagrete de Framboesa e Mel
- Salpicao Dona Eloat
- Sanduiche Natural
- Schnitzel de Tofu com Gergelim
- Shawarma de Frango
- Smoothie de Melancia de Verão
- Sopa de Feijão com Cinco Ingredientes
- Sopa de Tomate Fresco com Manjericão e Lagostins
- Sorvete de Aveia com Manteiga de Amendoim
- Strogonoff de Berinjelas
- Surpresa de Atum
- Tabulé de Feijão Branco
- Tender com Molho de Laranja e Gengibre
- Tepache (Bebida Mexicana Fermentada de Abacaxi)
- Tomates Recheados
- Torta de Banana
- Torta de Carne Moída com Farinha de Amêndoas (Low Carb)
- Torta de Frango Low Carb (Alessandra)
- Torta de Frango Low Carb (Fernanda)
- Torta de Goiabada
- Torta de Morango
- Torta de Ricota
- Torta Fritta (Bolinhos de Massa Frita)
- Tortelli d'Erbetta
- Trifle de Frutas Vermelhas
- Wafer Mae
