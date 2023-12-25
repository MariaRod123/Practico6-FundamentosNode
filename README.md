# Fundamentos NodeJs
1- Crear un servicio para buscar productos de un array en memoria según código y/o nombre a través de un POST.  
  El resultado esperado es el siguiente:
  

                {
                	"response": {
                		"nombre":"Manzana",
                		"precio":100,
                		"stock":15000,
                		"moneda":"\$"
                	}
                }
                
                
  En el caso de error, crear una respuesta lógica con lo siguiente: 
  
                
                {
                	"error": {
                		"mensaje":"Producto no encontrado"
                	}
                }

2- Crear un servicio para buscar un usuario de un array en memoria según documento y/o id a través de un GET. El resultado esperado es el siguiente:

                {
                	"response": {
                		"nombre":"Alex",
                		"apellido":"Casadevall"
                		"documento":5100836,
                		"edad":28,
                	}
                }

  En el caso de error, crear una respuesta lógica con lo siguiente: 

                {
                	"error": {
                		"mensaje":"Usuario no encontrado"
                	}
                }

3- Crear un servicio de un chatbot para devolver respuestas según las intenciones de un usuario a través de un POST. El objeto enviado por POST sería el siguiente:

              {
              	"mensaje":"Hola cómo estás?"
              }

  La respuesta esperada es del siguiente formato: 

            {
            	"response": {
            		"type":"bot",
            		"message":"Bien, en que te puedo ayudar?"
            	}
            }

  Recordar: Normalizar las intenciones que llegan al servicio del bot y dividir en términos. Caso no se encuentre respuesta para la intención, desplegar lo siguiente: 

            {
            	"error": {
            		"message":"No te entendí."
            	}
            }

4- Crear un servicio de procesamiento matemático para una calculadora básica con cuatro operaciones: suma, resta, multiplicación y división. A través de un POST. Donde el objeto enviado por POST es el siguiente: 

          {
          	"operacion":"suma",
          	"a":1500,
          	"b":10
          }
          
          La respuesta esperada es del siguiente formato: 
          
          {
          	"response": {
          		"resultado":1510
          	}
          }


  Caso no sea una operación soportada por el servicio o algún error de cálculo, enviar un error: 

      {
      "error": { "message":"Error de operación y/o cálculo." }
      }


5- Crear un servicio de procesamiento geométrico para una calculadora básica con cuatro operaciones: área cuadrado, área círculo, área rectángulo y área triángulo. A través de un POST. Donde el objeto enviado por POST es el siguiente: 

    {
    	"area":"triangulo",
    	"base":10,
    	"altura":10
    }

  La respuesta esperada es del siguiente formato: 

    {
    	"response": {
    		"resultado":50,
    		“unidad”:”metros cuadrados”
    	}
    }

  Caso en que no sea una operación soportada por el servicio o algún error de cálculo, enviar un error: 

    {
    "error": { "message":"Error de operación y/o cálculo." }
    }

6-  Crear un algoritmo (servicio) para decidir si una mano es “buena” o “mala” en el juego Black Jack. A través de un POST. Donde el objeto enviado por POST es el siguiente:

    {
    	"cartas":["J",8]
    }

  La respuesta esperada es del siguiente formato:

    {
    	"response": {
    		"probabilidad":85,
    		“recomendacion”:”no pedir”
    	}
    }





                
