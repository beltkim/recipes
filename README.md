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

## Receitas (161)

- Almôndegas com Batata Assada e Queijo
- Ameixas Recheadas
- Arroz Doce
- Baba de Moca
- Bacalhau ao Forno
- Batatas "Fritas" no Forno
- Batida de Abacaxi
- Beirute de Palmito
- Berinjela para Comer com Pao
- Berinjela Recheada
- Biscoito Quebra-quebra
- Bolacha da Mae
- Bolinho de Chuchu Delicioso e Leve
- Bolinho de Mandioca Frito
- Bolinho de Polvilho e Fuba
- Bolinhos de Laranja
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
- Bolo de Fubá com Goiabada
- Bolo de Fubá Cremoso I
- Bolo de Fubá Cremoso II
- Bolo de Fubá (Simples)
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
- Bolo Low Carb de Banana e Ameixa
- Bolo mousse coco (Sandra)
- Bolo Pao de Lo
- Bolo Prestígio
- Bolo Queijadinha Cremosa
- Bolo Regina Barroso
- Bolo Surpresa de Carne
- Bolos de Arroz
- Bombocado de Fuba
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
- Chantilly Diet
- Chantininho Resistente para Decoração de Bolos
- Cheesecake
- Chester Recheado com Frutas Secas e Nozes
- Cobertura de Marshmallow
- Creme da Tonha
- Creme de Papaia Light
- Crepes de Queijo Fresco com Tomates
- Cuca de Banana (Batedeira)
- Cueca Virada
- Cuque de Uva
- Donuts
- Farofa de Cenoura, Bacon e Azeitona
- Farofa Fria
- Farofa de Queijo Coalho, Banana-da-Terra e Calabresa
- Farofa Fria de Tomates e Azeitonas
- Fatias Húngaras de Coco e Leite Condensado
- Feijão Branco
- Frango Assado Recheado com Farofa
- Ganache de Chocolate
- Ganache Low Carb
- Geleia de Jabuticaba
- Gruste
- Lagarto Temperado
- Lombo Recheado de Palmito
- Legumes ao Queijo
- Maria Mole
- Massa de Pao
- Massa de Pizza Caseira Perfeita
- Massa de Pizza na Chapa
- Massa Podre para Torta Doce
- Molho Basico de Tomates
- Molho Bechamel
- Mousse de Maracuja
- Nhoque Suíço com Palmito e Alho-Poró
- Omelete ao Forno
- Pamonha de Colher
- Pernil Caramelizado
- Peru Especial de Ceia
- Pancakes de Banana sem Gluten
- Panetone Light
- Panetone Salgado com Calabresa
- Panetone Salgado com Presunto e Queijo
- Panqueca de Aveia
- Pao de Banana
- Pao de Queijo Light
- Pao Italiano
- Pao Liquidificador
- Pão Low Carb com Farinha de Amêndoas
- Pão Recheado de Carne Moída
- Paoziho de Leite
- Pasta de Alho (3 versoes)
- Pate de Tomate Seco
- Pave Rapido de Limao
- Pe-de-moleque
- Pizza Mineira
- Pizza Rapida
- Pudim de Leite Condensado da Vovo
- Pudim de Leite Condensado MOÇA
- Pudim de Sorvete
- Pudim FIT sem Açúcar
- Pudim Mesclado de Chocolate e Ninho
- Quindim
- Rabanada
- Receita de Massa para Empada, Empadao e Tortas Salgadas
- Rosca da Vo Tonha
- Rosquinha de Queijo
- Salada de Macarrao e Atum
- Salpicao Dona Eloat
- Sanduiche Natural
- Strogonoff de Berinjelas
- Surpresa de Atum
- Tabulé de Feijão Branco
- Tender com Molho de Laranja e Gengibre
- Tomates Recheados
- Torta de Banana
- Torta de Carne Moída com Farinha de Amêndoas (Low Carb)
- Torta de Frango Low Carb (Alessandra)
- Torta de Frango Low Carb (Fernanda)
- Torta de Goiabada
- Torta de Morango
- Torta de Ricota
- Wafer Mae
