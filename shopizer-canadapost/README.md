# shopizer-shipping-canadapost-module 2.2.0

Uses canada post shipping rate system calculator for Shopizer.

1- Signup for an account on www.canadapost.ca

2- Create a developer account on Canadapost developer web site

3- Retain you Canadapost CPC number and your API keys for their sandbox and production environment

A CPC identifier and API key look like this

		CPC Identifier : CPC_YOUR_BUISINES
		API key : a6d1ba721909c95f : 446636bt2561fb15b7dc2d93

4- Edit src/test/resources/spring/spring-context-test.xml and use the development key

		<util:properties id="canadapost-properties">
    			<prop key="username">a6d1ba721909c95f</prop>
    			<prop key="password">446636bt2561fb15b7dc2d93</prop>
    			<prop key="mailBy">CPC_YOUR_BUISINES</prop>
              </util:properties>
       
5- Run ShippingCanadaPostTestCase unit test

##Running this module from shopizer

Select this module as a shipping method from shopizer/admin - Shipping - shipping methods

You will ba esked to put your username, password and mailBy (CPC identifier)

Canadapost uses basic authentication and provides a token for using with their API. The token is in the following format X0X0X0:0X0X0X

The username corresponds to the first part before semi-column (:) and the password is the sequence following the semi-column


