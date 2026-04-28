Funcion puntos <- Calcular_Puntos(kilos)
    puntos <- kilos * 5
FinFuncion

Algoritmo Puntos_Reciclaje
    Definir num_Estudiantes, contador Como Entero
    Definir nombre Como Caracter
    Definir kilos, puntos Como Entero
    
    
    num_Estudiantes <- 0
	
    Mientras num_Estudiantes <= 0 Hacer
        Escribir "Ingrese la cantidad de estudiantes a registrar:"
        Leer num_Estudiantes
        Si num_Estudiantes <= 0 Entonces
            Escribir "Debe ingresar al menos un estudiante."
        FinSi
    FinMientras
    
    contador <- 1
    Mientras contador <= num_Estudiantes Hacer
        Escribir "--------------------------------"
        Escribir "Estudiante # ", contador
        Escribir "Ingrese el nombre:"
        Leer nombre
        
        kilos <- -1
        Mientras kilos < 0 O kilos > 30 Hacer
            Escribir "Ingrese los kilos reciclados :"
            Leer kilos
            Si kilos < 0 O kilos > 30 Entonces
                Escribir " Valor fuera de rango deben de estar entre 0 y 30. Intente nuevamente."
            FinSi
        FinMientras
        
        puntos <- Calcular_Puntos(kilos)
      
        Escribir "Estudiante: ", nombre
        Escribir "Puntos obtenidos: ", puntos
        
        Si puntos >= 50 Entonces
            Escribir "Resultado: Reconocimiento ganado"
        Sino
            Escribir "Resultado: Debe reciclar mas"
        FinSi
        
        contador <- contador + 1
    FinMientras
    
    Escribir "--------------------------------"
    Escribir "Proceso finalizado."
FinAlgoritmo