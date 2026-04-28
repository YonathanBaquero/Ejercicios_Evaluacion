Algoritmo Registro_Transporte

    Definir codigo, totalGastado, totalViajes Como Entero
    
    totalGastado <- 0
    totalViajes <- 0
    codigo <- -1 
    
    Mientras codigo <> 0 Hacer
        Escribir "--------------------------------"
        Escribir "Seleccione una opcion segun el tipo de transporte usado:"
        Escribir "1 - Bus ($3000)"
        Escribir "2 - Metro ($3500)"
        Escribir "3 - Taxi ($8000)"
        Escribir "0 - Finalizar registro"
        Escribir "--------------------------------"
        Escribir "Por favor ingrese la opcion:"
        Leer codigo
        
        Segun codigo Hacer
            1:
				Escribir "Usted a selecionado Bus"
                totalGastado <- totalGastado + 3000
                totalViajes <- totalViajes + 1
            2:
				Escribir "Usted a selecionado Metro"
                totalGastado <- totalGastado + 3500
                totalViajes <- totalViajes + 1
            3:
				Escribir "Usted a selecionado Taxi"
                totalGastado <- totalGastado + 8000
                totalViajes <- totalViajes + 1
            0:
                Escribir "Registro finalizado."
            De Otro Modo:
                Escribir "Código inválido. Por favor ingrese nuevamente el codigo"
        FinSegun
    FinMientras
    
    Escribir "--------------------------------"
    Escribir "RESUMEN DE SU REGISTRO"
    Escribir "Total de viajes registrados: ", totalViajes
    Escribir "Usted gasto en transporte: $ ", totalGastado
    Escribir "--------------------------------"
FinAlgoritmo