#include <stdio.h>

// Conversor de monedas a elegir.
Prerrequisitos:
-VisualStudioCode
-BuildTools
-Github
-Ejecutar el programa en el compilador.
Menu Ejecutar, Ctrl+F10 en Windows,
LINUX:
Guardar el programa con .c.
Usando el compilador gcc, compilar el programa: gcc -o mi_programa.c
Ejecutar el archivo: mi_programa.c


Convertir de GTQ a 2 monedas

double convertirAMonedas(double cantidad, char aMoneda) {
    double cantidadConvertida = 0.0;

    switch (aMoneda) {
        case 'E':
            cantidadConvertida = cantidad * 8.55; // Tasa de cambio GTQ a EUR
            break;
        case 'U':
            cantidadConvertida = cantidad * 7.80; // Tasa de cambio GTQ a USD
            break;
        default:
            printf("Código de moneda no válido. Códigos admitidos: E (EUR), U (USD)\n");
            break;
    }

    return cantidadConvertida;
}

int main() {
    double cantidadGTQ;
    char aMoneda;

    printf("Ingresa la cantidad en GTQ: ");
    scanf("%lf", &cantidadGTQ);

    printf("Ingresa la moneda a la que deseas convertir (E para EUR, U para USD): ");
    scanf(" %c", &aMoneda);

    double cantidadConvertida = convertirAMonedas(cantidadGTQ, aMoneda);

    if (cantidadConvertida > 0.0) {
        printf("%.2lf GTQ es equivalente a %.2lf en la moneda seleccionada.\n", cantidadUSD, cantidadConvertida);
    }

    return 0;
}
