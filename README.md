# atv-4
#include <stdio.h>
#include <stdlib.h>

// Variáveis globais para armazenar membros da classe
int* ptr1;
int* ptr2;

// Função para atribuir memória aos membros da classe
void alocarMemoria() {
    ptr1 = (int*)malloc(sizeof(int));
    ptr2 = (int*)malloc(sizeof(int));
}

// Função para desalocar memória para membros da classe
void deslocarMemoria() {
    free(ptr1);
    free(ptr2);
}

// Função equivalente a allocateHist
void alocarHist() {
    //lógica para alocarHist()
    printf("Método alocarHist chamado.\n");
}

// Função equivalente a registrarRegInHist
void registrarRegInHist() {
    // Logica para registrarRegInHist
    printf("Método registrarRegInHist chamado.\n");
}

int main() {
    // Atribuir memória aos membros da classe
    alocarMemoria();

    // usando os membros da classe
    alocarHist();
    registrarRegInHist();

    // Desalocar a memória para os membros da classe
    deslocarMemoria();

    return 0;
}
