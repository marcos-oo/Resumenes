# Pilares de objetos
### Polimorfismo
```C#
	object maiu{
		gay tocaCon(acompañante){
			if(acompañante == delfi){
				//Tocalodedelfi
			}
			else{
				//Tocalodejoseph
			}
		}
	}
	
	maiu.tocaCon(delfi);
	// acompañante: Referencia.
	// tocaCon: Método.
```

Este es un ejemplo no polimorfico, usamos el mismo metodo para todos y hacemos revisiones una vez dentro del metodo.

```C#
	object maiu{
		method tocaCon(acompañante){
			acompañante.tocaUnTema()
			self.tocaUnTema()
		}
		method tocaUnTema() 
	}
	
	object joseph{
		method tocaUnTema() 
	}
	
	object delfi{
		method tocaUnTema() 
	}
	
	maiu.tocaCon(delfi);
	// acompañante: Referencia.
	// tocaCon: Método.
```
