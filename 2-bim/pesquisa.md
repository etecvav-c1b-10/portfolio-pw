# definicao de CSS

## CSS significa Cascading Style Sheets (Folhas de Estilo em Cascata). É uma linguagem usada para definir a aparência e o layout de páginas web.

## Enquanto o HTML estrutura o conteúdo (texto, imagens, botões), o CSS controla como esse conteúdo será exibido — por exemplo:

- Cores (texto, fundo)
- Fontes e tamanhos de texto
- Espaçamento e margens
- Posicionamento de elementos
- Layouts (como grids e flexbox)

## Exemplo simples:

p {
  color: blue;
  font-size: 16px;
}

## Nesse exemplo, todos os parágrafos (p) ficarão com texto azul e tamanho de 16 pixels.

## Por que “cascata”?

## O termo “cascading” (cascata) se refere à forma como o CSS decide qual estilo aplicar quando há múltiplas regras — ele segue uma ordem de prioridade.

# formato do CSS

## O formato do CSS segue uma estrutura bem definida chamada de regra CSS. Ela é composta basicamente por seletor + declaração.

## Estrutura básica:

 seletor {
  propriedade: valor;
}

## Exemplo:

 h1 {
  color: red;
  font-size: 24px;
}

## Nesse caso:

- h1 = seletor (define qual elemento será estilizado)
- color e font-size = propriedades
- red e 24px = valores

## Partes do CSS
- Seletor → indica o elemento (ex: p, h1, .classe, #id)
- Propriedade → o que você quer mudar (ex: color, margin)
- Valor → como vai mudar (ex: blue, 10px)

/* seletor de elemento */
p {
  color: blue;
}

/* classe */
.minha-classe {
  background-color: yellow;
}

/* id */
#meu-id {
  font-size: 20px;
}

## Regras importantes
- Sempre usar { } para abrir e fechar o bloco
- Cada propriedade termina com ;
- CSS não usa = (usa :)

# tipos de CSS

## in-line

## in-folder

## external