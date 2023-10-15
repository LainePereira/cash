#include <stdio.h>

int main() {
    // Valores das moedas disponíveis
    float moedas[] = {1.0, 0.5, 0.25, 0.1, 0.05};

    // Número de moedas disponíveis
    int num_moedas = sizeof(moedas) / sizeof(moedas[0]);

    // Valor total da compra e valor pago
    float valor_compra, valor_pago;
    printf("Informe o valor da compra: ");
    scanf("%f", &valor_compra);
    printf("Informe o valor pago: ");
    scanf("%f", &valor_pago);

    // Calcula o troco
    float troco = valor_pago - valor_compra;

    if (troco < 0) {
        printf("Valor pago insuficiente.\n");
        return 1;
    }

    printf("Troco: %.2f\n", troco);

    // Calcula as moedas do troco usando o algoritmo guloso
    printf("Moedas do troco:\n");
    for (int i = 0; i < num_moedas; i++) {
        int quantidade_moedas = troco / moedas[i];
        if (quantidade_moedas > 0) {
            printf("%.2f: %d moeda(s)\n", moedas[i], quantidade_moedas);
            troco -= quantidade_moedas * moedas[i];
        }
    }

    return 0;
}
