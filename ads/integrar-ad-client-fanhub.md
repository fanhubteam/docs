# Como integrar o ad-client da FanHub em meu site
 
O objetivo desse documento é auxiliar os nossos parceiros de negócios a instalar o ad-client da FanHub em suas páginas.
 
# Antes de começarmos
 
Para cada parceiro comercial é feito um cadastro especifico para tamanhos de imagens que compoeem a vitrine de display, entre em contato com a area de engenharia da FanHub para receber as informacoes de `parceiros` e dos `tipos de anuncios` disponiveis para o seu site.
 
# Código para parceiros
 
Adicione o código abaixo antos do fechamento da tag `</body>` do seu site
 
```
<script>
   !function (e, n) {
   (n = e.createElement("script")).type = "text/javascript", n.async = !0, n.onload = function () {
       ethicalads.wait.then(n)
   }, n.src = "https://script.fanhub.com.br/inject.min.js", e.getElementsByTagName("head")[0].appendChild(n), setTimeout(() => {
       (console.log("undefined" == typeof fanhub), "undefined" == typeof fanhub) && document.querySelectorAll("[data-fanhub-publisher]").forEach(function (e, n) {
       e.innerHTML = "Por favor, desative o seu Ad Block!"
       })
   }, 1e3)
   }(document);
</script>
```

Esse script é responsavel por verificar quais `tipos de anuncios` estão disponiveis em seu site, e fazer a entrega nos locais demarcados
 
# Tipos de anúncios
 
Os tipos de anúncios especificam os parâmetros de um anúncio para determinar como um anúncio é renderizado, se ele tem uma imagem ou o tamanho do texto.
 
Os tipos de anúncios são registrados previamente com o time de Engenharia da FanHub. Entre em contato conosco para saber quais tipos de anúncios estão disponíveis para o seu site.
 
Depois de inserir o `código para parceiros` nas paginas onde serão exibidos anúncios da rede de display da FanHub, use o exemplo abaixo para adicionar o HTML de demarcação de cada bloco de `tipo de anuncio` disponível para o seu site.
 
Tomando como exemplo que você é o parceiro `parceiro-teste` e que você recebeu os tipos de anuncios `site-square-banner` e `site-full-banner` para adicionar na sua pagina, os seus blocos de demarcação em HTML ficariam como abaixo:
 
```
<div data-fanhub-publisher="parceiro-teste" data-fanhub-type="site-square-banner"></div>
```
``` 
<div data-fanhub-publisher="parceiro-teste" data-fanhub-type="site-full-banner"></div>
```

Veja um exemplo de uma pagina integrada com o ad-cliente [clicando aqui](https://github.com/fanhubteam/docs/blob/master/ads/exemplo-integrar-ad-client.html)
 
# O que acontece quando um anuncio é veiculado para um visitante do meu site?
 
Sempre que um anúncio é entregue para um visitante do seu site, as ações abaixo são executadas:
 
## Quando o visitante visualizar o anúncio
 
1. Sera registrado em nosso servidor uma acao de `visualização de anuncio`.
2. será renderizado o anúncio para o visitante, no caso de um anúncio do tipo imagem, será renderizado uma imagem com as dimensões pré-definidas no navegador ao cliente, no espaço previamente determinado.
 
## Quando o visitante clica no anúncio
 
1. Será registrado em nosso servidor uma ação de `click de anúncio`.
2. O visitante é redirecionado a página de destino do anúncio.


# Estou com dúvida, com quem falo?

Entre em contato com a area de engenharia da FanHub, para marcarmos uma call e fazermos a 4 mãos.
