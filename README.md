# msMediaQuery
> Permite executar uma ação de acordo com a resolução de tela do usuário.

msMediaQuery é um Objeto User Control [Genexus](https://www.genexus.com/pt/) que até o momento identifica um conjunto limitado de padrões de tela [iPhone-Retina, Extra-Small, Small, Medium e Large]. Implementações futuras poderão permitir a tratativa de [Orientação] e types especializados tais como [print, braille, etc...]. 


## Nota
A sintaxe utilizada no Objeto UC poderia se adequar melhor aos recursos atuais providos pela linguagem e práticas de desenvolvimento, porém foi propositalmente escrito desta forma afim de facilitar a compreensão daqueles que não desenvolvem em JavaScript.

## Instalação

Genexus 16 ou Superior:

```sh
1 - Na IDE Genexus, navegue em Knowledge Manager / Import.
2 - Selecione o Arquivo msMediaQuery.xml ** Note que é preciso alterar o filtro da caixa de seleção para XML.
** Para geradores Java, verifique o caminho no qual o Objeto File [msMediaQueryJS] esta sendo extraído.
```

## Exemplo de uso

```sh
Event msMediaQueryAPI.OnChange(&MediaQuery)
	
	Do Case
		
		Case &MediaQuery = !'Extra-Small'
			//Minha Ação		
			
		Case &MediaQuery = !'Small'
			//Minha Ação
			
		Case &MediaQuery = !'Medium'
			//Minha Ação
			
		Case &MediaQuery = !'Large'
			//Minha Ação
			
	EndCase
	
EndEvent
```

## Informações para Desenvolvimento do Objeto User Control

Preciso de um valor que não esta no UC, e agora?
```sh
1 - Defina uma nova Media Query na aba Screen Template do Objeto User Control.
2 - Crie uma condicional [IF] para cada novo valor inserido no passo 1.
** Tome como exemplo os valores já existentes.
```
## Histórico de lançamentos

* 0.1.0
    * Primeira versão funcional [@gtorrezani](https://github.com/gtorrezani)


## Meta

Gustavo Torrezani Matias – [@instagram](https://www.instagram.com/matiassolucoes/)

Distribuído sob a licença [MIT](https://choosealicense.com/licenses/mit/).
