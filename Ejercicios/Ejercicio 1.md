Algoritmo Uso_Celular
	
	Definir dia,minutos,total_min,dias_alto Como Entero
	Definir prom Como Real
	
	dia <- 1
	total_min <- 0
	dias_alto <- 0
	
	Mientras dia <= 4 Hacer
		minutos <- -1
		
		Mientras minutos < 0 o minutos > 240 Hacer
			Escribir "Ingrese cuantos minutos usa el celular en el dia " , dia
			Leer minutos
			
			si minutos < 0 o minutos > 240 Entonces
				Escribir "*****************************************************************************"
				Escribir "El valor debe de estar entre 0 y 240 minutos, digite nuevamente los minutos"
				Escribir "*****************************************************************************"
				Escribir "Ingrese cuantos minutos usa el celular en el dia " , dia
				leer minutos
				
			FinSi
		FinMientras
		total_min <- total_min + minutos
		
		si minutos > 120 Entonces
			Escribir "El uso del celular en el dia " , dia , " es ALTO"
			dias_alto <- dias_alto +1
		SiNo
			Escribir "El uso del celular en el dia " , dia , " es NORMAL"
		FinSi
		dia <- dia + 1
	FinMientras
	
	prom <- total_min /4
	
	Escribir "*****************************************************************************"
	Escribir "RESUMEN DEL USO DEL CELULAR"
	Escribir "El total de minutos usados en los 4 dias es de : ", total_min " minutos"
	Escribir "El promedio de minutos usados al dia es: " , prom " minutos"
	
	si dias_alto = 1 Entonces
		Escribir "La cantidad de dias con uso alto es de : ", dias_alto " dia"
	SiNo
		Escribir "La cantidad de dias con uso alto es de : ", dias_alto " dias"
	
	Escribir "*****************************************************************************"
	
	FinSi
FinAlgoritmo
