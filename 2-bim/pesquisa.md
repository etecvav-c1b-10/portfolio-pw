# Definição de CSS

CSS significa Cascading Style Sheets (Folhas de Estilo em Cascata). É uma linguagem usada para definir a aparência e o layout de páginas web.

Enquanto o HTML estrutura o conteúdo (texto, imagens, botões), o CSS controla como esse conteúdo será exibido — por exemplo:

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

Nesse exemplo, todos os parágrafos (p) ficarão com texto azul e tamanho de 16 pixels.

## Por que “cascata”?

O termo “cascading” (cascata) se refere à forma como o CSS decide qual estilo aplicar quando há múltiplas regras — ele segue uma ordem de prioridade.

# formato do CSS

O formato do CSS segue uma estrutura bem definida chamada de regra CSS. Ela é composta basicamente por seletor + declaração.

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

Existem 3 tipos principais de CSS, que diferem pela forma como você aplica o estilo na página:

## 1. CSS Inline (na própria linha) - É aplicado diretamente na tag HTML.

<p style="color: red;">Texto vermelho</p>

## Características:

- Atua só naquele elemento
- Não é reutilizável
- Não é recomendado para projetos grandes

## 2. CSS Interno (dentro do HTML) - Fica dentro da tag <style> no <head> da página.

<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>

## Características:

- Vale para toda a página
- Melhor que inline
- Ainda não é ideal para vários arquivos

## 3. CSS Externo (arquivo separado) - Você cria um arquivo .css e conecta ao HTML.

<head>
  <link rel="stylesheet" href="style.css">
</head>

## Arquivo style.css:

p {
  color: green;
}

## Características:

- Mais organizado
- Reutilizável
- Melhor prática (usado em projetos reais)

| Tipo        | Onde Fica      | Indicado? |
|-------------|----------------|-----------|
| Inline      | Na tag HTML    | Não       |
| Interno     | Dentro do HTML | Médio     |
| Externo     | Arquivo .css   | Sim       |



# In-line

O CSS inline é um tipo de CSS aplicado diretamente dentro da tag HTML, usando o atributo style.

## Exemplo:

<p style="color: red; font-size: 18px;">
  Texto em vermelho
</p>

## Como funciona:

- O estilo é escrito dentro da própria tag
- Cada propriedade usa : e termina com ;
- Pode colocar várias propriedades no mesmo style

## Vantagens:

- Rápido para testes
- Fácil de aplicar em um único elemento
- Útil para ajustes pontuais

## Desvantagens:

- Difícil de manter
- Não reutilizável
- Mistura HTML com estilo (não é boa prática)
- Pode deixar o código bagunçado

## Importante:

O CSS inline tem alta prioridade, ou seja: Ele geralmente sobrescreve CSS interno e externo

## Quando usar?

- Pequenos ajustes rápidos
- Testes
- Situações específicas

Em projetos reais, o ideal é usar CSS externo.

# In-folder

É o CSS escrito dentro do HTML, na seção <head>.

## Exemplo:

<!DOCTYPE html>
<html>
<head>
  <style>
    h1 {
      color: green;
    }

    p {
      font-size: 16px;
    }
  </style>
</head>

<body>
  <h1>Título</h1>
  <p>Parágrafo</p>
</body>
</html>

## Como funciona:

- O CSS fica dentro da tag <style>
- Afeta todos os elementos daquela página
- Não precisa criar arquivo .css

## Vantagens:

- Mais organizado que inline
- Permite reutilizar estilos dentro da mesma página
- Fácil de testar

## Desvantagens:

- Não reutilizável em outras páginas
- Pode deixar o HTML muito grande
- Não é ideal para projetos grandes

## Prioridade

- Menor que o inline
- Pode sobrescrever o externo dependendo da ordem

## Quando usar?

- Projetos simples
- Exercícios
- Testes rápidos


# External

#É o CSS que fica em um arquivo separado (.css), ligado ao HTML.

## Exemplo:

<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="style.css">
</head>

<body>
  <h1>Título</h1>
  <p>Parágrafo</p>
</body>
</html>

## CSS (style.css):

h1 {
  color: purple;
}

p {
  font-size: 18px;
}

## Como funciona:

- O CSS fica em outro arquivo
- O HTML “puxa” esse arquivo com <link>
- Pode ser usado em várias páginas

## Vantagens:

- Código organizado
- Reutilizável em vários arquivos
- Facilita manutenção
- Padrão usado em projetos profissionais

## Desvantagens:

- Precisa criar arquivo separado
- Depende do caminho correto (href)
- Pode não carregar se o arquivo estiver no lugar errado

## Prioridade

- Menor prioridade comparado ao inline e interno
- Pode ser sobrescrito por eles

## Quando usar?

Sempre que possível — é a melhor prática.

## Resumo geral dos 3

| Tipo       z | Onde Fica      | Recomendado? |
|-------------|---------------- |--------------|
| Inline      | Na tag HTML     | Não          |    
| Interno     | Dentro do HTML  | Médio        |
| Externo     | Arquivo .CSS    | Sim          |