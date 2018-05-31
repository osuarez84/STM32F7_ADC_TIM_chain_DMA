Este proyecto es para utilizar como template de un proyecto para utilizar el ADC integrado en el
STM32F769NI (STM32F768NI-DISCO1). Se configura el disparo para controlarlo mediante un temporizador
avanzado (TIM1) trabajando con One-Pulse Mode y con un Repetition Counter configurado a 10 para
dispararse diez veces. TIM1 se dispara a trav�s de TIM3, que controla cada cu�nto debemos de tomar
esos 10 samples. TIM1 por tanto controla el tiempo entre cada sample. A su vez la gesti�n de los datos
la realiza la DMA que los pasa directamente al buffer.

Este proyecto es funcional y se ha comprobado utilizando un analizador l�gico
para medir las se�ales de finalizaci�n de la conversi�n ADC (finaliza la recogida de 
los 10 samples) y los disparos de cada sample por TIM1.
