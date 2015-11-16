/**
 * $Id: uc_pagseguro.module,v 1.6.2.00 (BETA) 24/11/2009 21:04
 * 
 * Módulo de conexão com o Ubercart para pagamento dos produtos no pagseguro
 * Este módulo possui a licenca LGPLv3.
 * Este módulo foi modificado do módulo 2Checkout para a versão do drupal 6.x-2.2 
 * 
 * Leiame com instrucoes de instalação
 * 
 * Autor: André Eppinghaus
 * Site de teste: www.avaliacao@kinghost.net/loja_virtual
 * Email: andreeppinghaus@gmail.com
 * Alterações, sugestões, dúvidas sobre instalação me mande um email.
 * 
 */

Facilidades do modulo
======================

1) Nao precisa do modulo dos correios da versao 5 ou qualquer outro para calcular o frete, pois sera calculado pelo pagseguro
basta configurar o modo frete por peso e colocar o peso do produto por kilo.

2) Aceita acentuacao

3) Nao e necessario configurar os campos que aparecem para o envio do produto e fatura como nome, telefone, etc. Pois os campos que sobrarem 
o pagseguro irá perguntar. É bom voce, ter estes campos para o cadastro da loja.

4) O comprador não precisa ter cadastro no pagseguro.

5) Configure a cara da sua loja no pagseguro para o seu cliente ter confianca na sua loja.

 https://pagseguro.uol.com.br/data/viewBusinessData.jhtml para 


 Instrucoes para criar um perfil de vendedor
============================================

1) Vá no site do Pagseguro: https://pagseguro.uol.com.br/index.jhtml
2) Crie uma conta e altere seu perfil para vendedor ou conta empresarial : https://pagseguro.uol.com.br/account/viewDetails.jhtml
3) Vá em preferencias e configure o retorno automatico : 
         
    https://pagseguro.uol.com.br/preferences/automaticReturn.jhtml
4) Clique para ativar o retorno automático e configure a url de retorno para:

http://www.seu_site.com.br/cart/pagseguro/retorno

5) Gere um TOKEN de SEGURANCA que deverá ser cadastrado na configuracao do módulo pagseguro

exemplo de TOKEN:  88B8A99999888E6B46743D7B1

6) Defina o campo frete por peso, é necessário cadastrar um peso (Kilo) para cada produto.

https://pagseguro.uol.com.br/seller/sellerConfigFreight.jhtml

Instrucoes de instalacao
========================

1) Copie o módulo para o diretorio de instalacao do Ubercart localizado em:

  sites/all/modules/ubercart/payment

2) Instale o módulo pelo drupal: 

     /admin/build/modules

3) vá no modo de administracao da loja em configuracaod e pagamentos:

      /admin/store/settings/payment

4) Clique em editar métodos de pagamentos:

   /admin/store/settings/payment/edit/methods

5) Clique no Link  definicoes de PagSeguro

6) Acrescente o email de vendedor (email de login do pagseguro)

7) Acrescente seu TOKEN de seguranca

8) Salve e Agora é só vender, NÃO PRECISA CONFIGURAR MAIS NADA !!!!!!!!!!!!

9) Caso falte alguma informacao o PagSeguro se encarregara de perguntar.

10) O modulo esta enviando email para o cliente. Para que o cliente visualise as proprias compras deve ativar a permissao abaixo:

admin/user/permissions

view own orders para usuarios autenticados

11) Acrescentei a traducao do ubercart que estou usando na minha loja virtual basta importar.

ubercart.pt.po

