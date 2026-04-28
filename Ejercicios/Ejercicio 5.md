Funcion precio <- Obtener_Precio(cod)
    Segun cod Hacer
        1: precio <- 2000
        2: precio <- 2500
        3: precio <- 4000
        De Otro Modo: precio <- 0
    FinSegun
FinFuncion

Algoritmo Venta_Cafeteria
    Definir codigo, cantidad, total_General, sub_total, precio_Producto Como Entero
    
    total_General <- 0
    codigo <- 1 
    
    Mientras codigo <> 0 Hacer
		Escribir "--------------------------------"
		Escribir "Seleccione el producto:"
        Escribir "--------------------------------"
        Escribir "1 - Agua $2000"
        Escribir "2 - Galleta $2500"
        Escribir "3 - Jugo $4000"
        Escribir "0 - Terminar registro"
        Escribir "--------------------------------"
        Leer codigo
        
        Si codigo = 0 Entonces
            Escribir "Registro finalizado."
        Sino
            Si codigo >= 1 Y codigo <= 3 Entonces
                
                cantidad <- 0
                Mientras cantidad <= 0 Hacer
                    Escribir "Ingrese cantidad:"
                    Leer cantidad
                    Si cantidad <= 0 Entonces
                        Escribir "Error: La cantidad debe ser mayor a 0."
                    FinSi
                FinMientras
                
             
                precio_Producto <- Obtener_Precio(codigo)
                sub_total <- precio_Producto * cantidad
                total_General <- total_General + sub_total
                
                Escribir "Total de esta compra: $", sub_total
            Sino
                Escribir "El Código es inválido. Por favor vuelva a digitar el codigo"
            FinSi
        FinSi
    FinMientras
    
    Escribir "--------------------------------"
    Escribir "VENTA TOTAL DEL DÍA: $", total_General
    Escribir "--------------------------------"
FinAlgoritmo