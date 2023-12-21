#include <stdio.h>

void diziToplam(int satir, int sutun, int dizi1[satir][sutun], int dizi2[satir][sutun], int sonuc[satir][sutun]) {
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            sonuc[i][j] = dizi1[i][j] + dizi2[i][j];
        }
    }
}

int main() {
    int satir, sutun;

    printf("Lutfen dizilerin satir sayisini girin: ");
    scanf("%d", &satir);

    printf("Lutfen dizilerin sutun sayisini girin: ");
    scanf("%d", &sutun);

    int dizi1[satir][sutun], dizi2[satir][sutun], sonuc[satir][sutun];

    printf("Ilk dizinin elemanlarini girin:\n");
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            printf("dizi1'in[%d][%d].elemani: ", i, j);
            scanf("%d", &dizi1[i][j]);
        }
    }

    printf("Ikinci dizinin elemanlarini girin:\n");
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            printf("dizi2'in[%d][%d].elemani: ", i, j);
            scanf("%d", &dizi2[i][j]);
        }
    }

    diziToplam(satir, sutun, dizi1, dizi2, sonuc);

    printf("Toplam sonucu olan dizi:\n");
    for (int i = 0; i < satir; i++) {
        for (int j = 0; j < sutun; j++) {
            printf("%d ", sonuc[i][j]);
        }
        printf("\n");
    }

    return 0;
}
