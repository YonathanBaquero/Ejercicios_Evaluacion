Algoritmo Reporte_Panaderia
    
    Definir dia, panes, total_Panes, dias_Bajo_Meta, dia_Mayor, mayor_Produccion Como Entero
    Definir prom Como Real
    

    dia <- 1
    total_Panes <- 0
    dias_Bajo_Meta <- 0
    mayor_Produccion <- -1 
	
    Mientras dia <= 7 Hacer
        panes <- -1
		
        Mientras panes < 0 Hacer
            Escribir "Ingrese la produccion de panes del día ", dia, ":"
            Leer panes
            Si panes < 0 Entonces
				Escribir "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
                Escribir "Error en ingreso de produccion. Por favor ingresar nuevamente los valores"
				Escribir "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
            FinSi
        FinMientras
        
        Si panes < 120 Entonces
            Escribir "Resultado: Producción BAJA"
        Sino
            Si panes <= 180 Entonces
                Escribir "Resultado: Producción ADECUADA"
            Sino
                Escribir "Resultado: Producción SOBRESALIENTE"
            FinSi
        FinSi
        
             total_Panes <- total_Panes + panes
        
        Si panes > mayor_Produccion Entonces
            mayor_Produccion <- panes
            dia_Mayor <- dia
        FinSi
        
       
        Si panes < 150 Entonces
            dias_Bajo_Meta <- dias_Bajo_Meta + 1
        FinSi
        
        dia <- dia + 1
    FinMientras
    
    
    prom <- total_Panes / 7
    
    Escribir "**************************************************************************"
    Escribir "SU PRODUCCION SEMANAL ES LA SIGUIENTE: "
	Escribir "**************************************************************************"
    Escribir "Total de panes: ", total_Panes
    Escribir "Promedio diario: ", prom
    Escribir "El día con mayor producción fue el dia ", dia_Mayor, ", con ", mayor_Produccion, " panes"
    
    Si dias_Bajo_Meta = 1 Entonces
        Escribir "Cantidad de días debajo de la meta (150): ", dias_Bajo_Meta, " dia"
    Sino
        Escribir "Cantidad de días debajo de la meta de los 150 panes : ", dias_Bajo_Meta, " dias"
    FinSi
	Escribir "**************************************************************************"
	Escribir "**************************************************************************"
FinAlgoritmo