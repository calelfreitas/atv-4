# atv-4
#include <stdio.h>
#include <stdlib.h>

// Variáveis globais para armazenar membros da classe
int* ptr1;
int* ptr2;

// Função para atribuir memória aos membros da classe
void alocarMemoria(){
    ptr1 = (int*)malloc(sizeof(int));
    ptr2 = (int*)malloc(sizeof(int));
}

// Função para desalocar memória para membros da classe
void deslocarMemoria(){
    free(ptr1);
    free(ptr2);
}

// Função equivalente a allocateHist
void alocarHist(){
    //lógica para alocarHist()
    printf("Método alocarHist chamado.\n");
}

// Função equivalente a registrarRegInHist
void registrarRegInHist(){
    // Logica para registrarRegInHist
    printf("Método registrarRegInHist chamado.\n");
}
// Set para ptr1
void setPtr1(int value){
    *ptr1 = value;
}

// Get para ptr1
int getPtr1() {
    return *ptr1;
}

// Set para ptr2
void setPtr2(int valor){
    *ptr2 = valor;
}

// Get para ptr2
int getPtr2() {
    return *ptr2;
}
int main(){
    // Atribuir memória aos membros da classe
    alocarMemoria();

    // usando os membros da classe
    alocarHist();
    registrarRegInHist();
    
    setPtr1(42); // Set ptr1 para 42
    setPtr2(100); // Set ptr2 para 100

    // Obtenha os valores dos membros da classe e mostra eles
    int valor1 = getPtr1();
    int valor2 = getPtr2();
    printf("\n ptr1: %d \n ptr2: %d\n", valor1, valor2);

    // Desalocar a memória para os membros da classe
    deslocarMemoria();

    return 0;
}
