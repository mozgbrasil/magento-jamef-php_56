[checkmark]: https://raw.githubusercontent.com/mozgbrasil/mozgbrasil.github.io/master/assets/images/logos/logo_32_32.png "MOZG"
![valid XHTML][checkmark]

[url-method]: http://www.jamef.com.br/
[requerimentos]: http://mozgbrasil.github.io/requerimentos/
[contact-jamef]: http://www.jamef.com.br/jamef/ecp/comunidade.do?app=portal&pg=20004&view=faleconosco
[tickets]: https://cerebrum.freshdesk.com/support/tickets/new
[preco]: http://www.cerebrum.com.br/preco/
[github-boxpacker]: https://github.com/mozgbrasil/magento-boxpacker-php_56#mozgboxpacker
[getcomposer]: https://getcomposer.org/
[uninstall-mods]: https://getcomposer.org/doc/03-cli.md#remove
[artigo-composer]: http://mozg.com.br/ubuntu/composer
[ioncube-loader]: http://www.ioncube.com/loaders.php
[acordo]: http://mozg.com.br/acordo-licenca-usuario-final/

# Mozg\Jamef

## Sinopse

Integração a [Jamef][url-method]

## Demonstração

[![Clique para visualizar o vídeo](https://img.youtube.com/vi/WGgI_QpSctE/0.jpg)](https://youtu.be/WGgI_QpSctE "Clique para visualizar o vídeo")

## Motivação

Atender o mercado de módulos para Magento oferecendo melhorias e um excelente suporte

## Suporte / Dúvidas

Para obter o devido suporte [Clique aqui][tickets], relatando o motivo da ocorrência o mais detalhado possível e anexe o print da tela para nosso entendimento

## Preço

[Clique aqui][preco]

## Recursos do módulo

- [✓] Cálculo do frete
- [✓] Rastreamento

## Característica técnica

Atualmente diversos módulos de terceiros relativo a métodos de entrega sempre soma o peso e dimensões dos produtos gerando falha na requisição a transportadora devido não terem um sistema que separa os produtos em sua devida embalagem distribuindo seu peso.

O nosso módulo foi desenvolvido visando total transparência dos processos executados, para efeito de análise visualize os processos armazenado em log.

A extensão permite você definir as dimensões de seus produtos, as dimensões, peso e valor de sua Embalagem/Caixa e regras de como empacotar diferentes combinações de produtos em conjunto como por exemplo embalar os produtos separadamente ou combinar os produtos na mesma Embalagem/Caixa.

A extensão escolhe qual embalagem será utilizado para embalar os produtos para o pedido.

A extensão pode distribuir os produtos em diversas embalagens até o peso máximo suportado para a embalagem.

Como será cadastrado a embalagem com as dimensões e peso suportado pelas transportadoras não deve ocorrer falha relativa as dimensões ou peso.

A primeira coisa a se levar em consideração no uso do módulo é o [Gerenciamento de Embalagem/Caixa][github-boxpacker], como já vem alguns registros pré inseridos certifique se de atualizar os registros conforme sua necessidade.

Certifique se ter cadastrado as devidas dimensões para os produtos.

Para cada embalagem é feito uma requisição a transportadora onde é passado os devidos parâmetros

O módulo possui armazenamento de cache

Na finalização do pedido é armazenado no histórico do pedido um comentário contendo um identificador único que poderá ser usado para consulta no arquivo de log a discriminação dos pacotes seus itens e a visualização de cada pacote com seus itens em 3D

Sempre confira as informações de frete antes de processar cada pedido, caso algo esteja inconsistente será necessário cancelar o pedido até a correção da ocorrência

Para o rastreamento do pacote é feito acesso ao WebService onde é passado os devidos parâmetros e exibido o devido retorno

## Testando na Heroku

Gostaria de apresentar o aplicativo que disponibilizei para a plataforma Heroku

Com apenas 1 clique, o aplicativo cria sua loja virtual usando a plataforma de comércio eletrônico Magento e instala os módulos da MOZG

[https://github.com/mozgbrasil/heroku-magento#descrição](https://github.com/mozgbrasil/heroku-magento#descrição)

## Instalação - Atualização - Desinstalação - Desativação

--

Sugiro "printar" as telas com todos os procedimentos executados

Envie para nós as imagens das telas na eventualidade de quaisquer dificuldades

--

Este módulo destina-se a ser instalado usando o [Composer][getcomposer]

Execute o seguinte comando no terminal, para visualizar a existencia do Composer e sua versão

	composer --version

Caso não tenha o Composer em seu ambiente, sugiro ler o seguinte artigo [Clique aqui][artigo-composer]

--

É necessário que o servidor tenha o suporte a extensão [ionCube PHP Loader][ioncube-loader]

Execute o seguinte comando no terminal, para visualizar a existencia da extensão nesse ambiente denominado PHP CLI

	php -v

Para visualizar se essa extensão está ativa em seu servidor no ambiente denominado PHP WEB

Certique se da presença do arquivo phpinfo.php na raiz do seu projeto

	<?php phpinfo(); ?>

Caso não exista o arquivo phpinfo.php na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

Acesse o arquivo pelo browser

Em seguida pesquise pelo termo "ionCube PHP Loader"

Caso o seu servidor não tenha o suporte a extensão, entre em contato com sua empresa de hospedagem e peça para que eles ativem a extensão

Caso tenha a permissão e queira ativar a extensão, [Clique aqui][ioncube-loader]

Em "Loader Downloads API", efetue download do pacote compatível com o seu servidor

Descompacte o pacote e faça upload do arquivo "loader-wizard.php" para seu servidor, onde será demonstrado o passo a passo para a ativação da extensão

[Clique aqui](https://youtu.be/GZ2J6MLkko4) para ver os processos executados

--

Na presença do "ionCube PHP Loader" efetue o download do seguinte arquivo e coloque na raiz do seu servidor e acesse, se funcionar quer dizer que o "ionCube" está lendo esse tipo de encriptação

https://raw.githubusercontent.com/mozgbrasil/heroku-magento/master/phpinfo-ioncube-encoder10-x86-64-php_56.php

--

Para utilizar o(s) módulo(s) da MOZG é necessário aceitar o [Acordo de licença do usuário final][acordo]

--

Sugiro manter um ambiente de testes para efeito de testes e somente após os devidos testes aplicar os devidos procedimento no ambiente de produção

--

Sugiro efetuar backup da plataforma Magento e do banco de dados

--

Antes de efetuar qualquer atualização no Magento sempre mantenha o Compiler e o Cache desativado

--

Certique se da presença do arquivo composer.json na raiz do seu projeto Magento e que o mesmo tenha os parâmetros semelhantes ao modelo JSON abaixo

	{
	  "minimum-stability": "dev",
	  "prefer-stable": true,
	  "license": [
	    "proprietary"
	  ],
	  "repositories": [
	    {
	      "type": "composer",
	      "url": "https://packages.firegento.com"
	    }
	  ],
	  "extra": {
	    "magento-root-dir": "./",
	    "magento-deploystrategy": "copy",
	    "magento-force": true
	  }
	}

Caso não exista o arquivo composer.json na raiz do projeto Magento, crie o mesmo adicionado o conteúdo acima

### Para instalar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer require mozgbrasil/magento-jamef-php_56:dev-master

Você pode verificar se o módulo está instalado, indo ao backend em:

	STORES -> Configuration -> ADVANCED/Advanced -> Disable Modules Output

--

### Para atualizar o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

Antes de efetuar qualquer processo que envolva atualização no Magento é recomendado manter o Compiler e Cache desativado

	composer update

Na ocorrência de erro, renomeie a pasta /vendor/mozgbrasil e execute novamente

Para checar a data do módulo execute o seguinte comando

	grep -ri --include=*.json 'time": "' ./vendor/mozgbrasil

--

### Para [desinstalar][uninstall-mods] o módulo execute o comando a seguir no terminal do seu servidor no diretório do seu projeto

	composer remove mozgbrasil/magento-jamef-php_56

--

### Para desativar o módulo

1. Antes de efetuar qualquer processo que envolva atualização sobre o Magento é necessário manter o Compiler e Cache desativado

2. Caso queira desativar os módulos da MOZG renomeie a seguinte pasta app/code/local/Mozg

A desativação do módulo pode ser usado para detectar se determinada ocorrência tem relação com o módulo

## Como configurar o método de entrega

Antes de configurar o módulo você deve cadastrar o CEP de origem, indo ao backend em:

	STORES -> Configuration -> Sales/Shipping Settings -> Origin

Para configurar o método de entrega, acesse no backend em:

	STORES -> Configuration -> Sales/Shipping Methods -> Jamef (powered by MOZG)

Você terá os campos a seguir

### • **Ativar**

Para "ativar" ou "desativar" o uso do método

### • **Ordem de exibição**

É a ordem apresentada em métodos de entrega no passo de fechamento de pedido

### • **Título**

Nome do método que deve ser exibido

### • **Serviços**

Selecione os serviços desejado, para selecionar mais de um, segure a tecla "Ctrl" e clique nos serviços

### • **Serviço Para Entrega Gratuita**

Quando houver um desconto de frete grátis, esse serviço terá o valor zero

### • **Calcular taxa de manuseio**

Podendo ser fixo ou percentual

### • **Taxa de Manuseio**

Será adicionado o valor ao frete

### • **Mostrar método se não aplicável**

Quando configurado como "Não", caso seja retornado algum serviço com erro, não será exibido o método de entrega

### • **Debug**

Deve ser armazenado os processos do módulo em var/log/

O arquivo

DATE_mozg.log

se trata de log do módulo sendo um log mais detalhado contendo todos os processos inclusive das execuções realizadas pelas bibliotecas externas do módulo

O arquivo

shipping_METHOD.log

se trata de log nativo do magento relativo ao método de entrega

### • **Identificador do atributo largura dos produtos**

Permite definir o nome do atributo de largura dos produtos usado no projeto

### • **Identificador do atributo comprimento dos produtos**

Permite definir o nome do atributo de comprimento dos produtos usado no projeto

### • **Identificador do atributo altura dos produtos**

Permite definir o nome do atributo de altura dos produtos usado no projeto

### • **Unidade de medida**

Sendo o padrão do peso do produto como kilo

Caso esteja usando a unidade de massa em gramas, tanto os produtos como as embalagens devem respeitar o mesmo padrão

Ao informar na configuração do método o uso da unidade de massa em gramas é feito a conversão do peso de grama para kilo

1 Kg no formato "Kilo" será "1.000", já em "Gramas" será "1000.000"

### • **Exibir Prazo de Entrega**

Se será ou não mostrado o prazo de entrega para seu cliente

### • **Mensagem que Exibe o Prazo de Entrega**

Se será ou não mostrado o prazo de entrega para seu cliente

### • **Adicionar (dias) ao prazo de entrega**

Quantidade de dias que será adicionado ao prazo

### • **Mostrar serviço com retorno de erro**

Quando configurado como "Não", caso seja retornado algum serviço com erro, o mesmo não deve ser exibido no método de entrega

### • **Tipo de Produto a ser transportado**

Tipo de Produto a ser transportado

### • **CPF ou CNPJ do cliente que será responsável pelo pagamento**

Preencha nesse campo o número do CPF ou CNPJ vinculado ao contrato com a Jamef

### • **Filial da Jamef que irá efetuar a coleta da mercadoria e emitir o CTRC do cliente.**

Filial da Jamef que irá efetuar a coleta da mercadoria e emitir o CTRC do cliente.

### • **Nome do Município de origem da Mercadoria. Mesmo Município do Cliente Responsável**

Nome do Município de origem da Mercadoria. Mesmo Município do Cliente Responsável.

Não informar acentos

### • **Sigla do Estado de origem**

Sigla do Estado de origem

## Perguntas mais frequentes "FAQ"

### Como conferir os valores dos fretes junto a transportada

Você pode visualizar no log os parâmetros enviado a transportada

Quando finalizado o pedido é armazenado no historico as dimensões da caixa que foi usada para o obter o frete

#### Simulação da requisição do preço

Ao efetuar o calculo do frete do produto

As dimensões do produto é "(LxCxA): 49 x 49 x 8 cm"

As dimensões da embalagem é "(LxCxA) 91 x 101 x 143 cm" e será armazenado 10kg

É usado as dimensões da embalagem para cálculo do peso cúbico

A formula do peso cúbico é "(largura_embalagem/100)×(comprimento_embalagem/100)×(altura_embalagem/100)" ou seja

METRO3 = (91/100)×(101/100)×(143/100) = 1.314313

Temos o devido retorno ao processar a seguinte requisição

	curl --header 'Content-Type: text/xml;charset=UTF-8' --header 'SOAPAction:JAMW0520_03' --data '<?xml version="1.0" encoding="UTF-8"?>
	<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns1="http://www.jamef.com.br/">
	    <SOAP-ENV:Body>
	        <ns1:JAMW0520_03>
	            <ns1:TIPTRA>1</ns1:TIPTRA>
	            <ns1:CNPJCPF>00000000000000</ns1:CNPJCPF>
	            <ns1:MUNORI>Belo Horizonte</ns1:MUNORI>
	            <ns1:ESTORI>MG</ns1:ESTORI>
	            <ns1:SEGPROD>000004</ns1:SEGPROD>
	            <ns1:QTDVOL>1</ns1:QTDVOL>
	            <ns1:PESO>10</ns1:PESO>
	            <ns1:VALMER>730</ns1:VALMER>
	            <ns1:METRO3>1.314313</ns1:METRO3>
	            <ns1:CNPJDES />
	            <ns1:FILCOT>02</ns1:FILCOT>
	            <ns1:CEPDES>08250580</ns1:CEPDES>
	        </ns1:JAMW0520_03>
	    </SOAP-ENV:Body>
	</SOAP-ENV:Envelope>' http://www.jamef.com.br/webservice/JAMW0520.apw

ou

	http://wsdlbrowser.com/soapclient?wsdl_url=http%3A%2F%2Fwww.jamef.com.br%2Fwebservice%2FJAMW0520.apw%3Fwsdl&function_name=JAMW0520_03

#### Simulação da Previsão de Entrega

curl --header 'Content-Type: text/xml;charset=UTF-8' --header 'SOAPAction:JAMW0520_02' --data '<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns1="http://www.jamef.com.br/">
  <SOAP-ENV:Body>
    <ns1:JAMW0520_02>
      <ns1:TIPTRA>1</ns1:TIPTRA>
      <ns1:MUNORI>Belo Horizonte</ns1:MUNORI>
      <ns1:ESTORI>MG</ns1:ESTORI>
      <ns1:MUNDES>São Paulo</ns1:MUNDES>
      <ns1:ESTDES>SP</ns1:ESTDES>
      <ns1:CNPJCPF>00000000000000</ns1:CNPJCPF>
      <ns1:CDATINI>05/02/2018</ns1:CDATINI>
      <ns1:CHORINI>13:09</ns1:CHORINI>
    </ns1:JAMW0520_02>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>' http://www.jamef.com.br/webservice/JAMW0520.apw

#### Simulação da requisição da consulta

Temos o devido retorno ao processar a seguinte requisição

	http://www.jamef.com.br/e-commerce/RastreamentoCargaServlet?CIC_RESP_PGTO=17325279000186&CIC_DEST=48787285401&COD_REGN_ORIG=12&NUM_NF=472&SERIE_NF=&SAIDA=XML

### Como aplicar o Frete Grátis

Na configuração do módulo para o método de entrega é possível definir o "Serviço Para Entrega Gratuita" recurso que deve ser aplicado quando definido a ação de "Frete Grátis" nas "Regras da Promoção"

No Backend do Magento, acesse o menu: Promoções -> Regras de Promoção -> Criar regra -> Crie uma regra e defina na aba "Ações" o uso do Frete Grátis

Dessa forma na exibição do cálculo do frete será exibido para o serviço escolhido o valor zerado

Esse recurso se trata de regra nativa do Magento caso tenha algum problema sugiro desativar todas as regras de promoção e ativar uma de cada vez até encontrar o motivo da ocorrência

### Dados de contato - Jamef

Comercial - Jamef <comercial.bhz@bhz.jamef.com.br>

Entre em contato com o setor comercial da JAMEF  
Solicite a habilitação da sua conta como cliente para acesso ao webservice da JAMEF  
Fone: (31) 2102-8808  
Fax: (31) 2102-8803

TI - Jamef

Em caso de dúvidas, favor entrar em contato com a equipe de TI da Jamef através do telefone

Tel.: (31) 2102-8904 - Suporte TI

brunoferreira@bhz.jamef.com.br - Suporte TI

ou acesse

Para entrar em contato com a [Jamef][contact-jamef]

## Manual

http://www.jamef.com.br/jamef/ecp/comunidade.do?evento=portlet&pIdPlc=ecpTaxonomiaMenuPortal&app=portal&tax=21381&lang=pt_BR&pg=20004&taxn=20035&taxp=0&

## Contribuintes

Equipe Mozg

## License

[Comercial License](LICENSE.txt)

## Badges

[![Join the chat at https://gitter.im/mozgbrasil](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mozgbrasil/)
[![Latest Stable Version](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/v/stable)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![Total Downloads](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/downloads)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![Latest Unstable Version](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/v/unstable)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![License](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/license)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![Monthly Downloads](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/d/monthly)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![Daily Downloads](https://poser.pugx.org/mozgbrasil/magento-jamef-php_56/d/daily)](https://packagist.org/packages/mozgbrasil/magento-jamef-php_56)
[![Reference Status](https://www.versioneye.com/php/mozgbrasil:magento-jamef-php_56/reference_badge.svg?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-jamef-php_56/references)
[![Dependency Status](https://www.versioneye.com/php/mozgbrasil:magento-jamef-php_56/1.0.0/badge?style=flat-square)](https://www.versioneye.com/php/mozgbrasil:magento-jamef-php_56/1.0.0)

:cat2:
