#include <stdio.h>

int main() {
    int jenis, jam, total, bayar, tambahan;

    printf("=== PEMBAYARAN PARKIR ===\n");
    printf("1. Motor (Rp2000/jam)\n");
    printf("2. Mobil (Rp5000/jam)\n");

    printf("Pilih kendaraan: ");
    scanf("%d", &jenis);

    printf("Lama parkir (jam): ");
    scanf("%d", &jam);

    if (jenis == 1) {
        total = jam * 2000;
    } else if (jenis == 2) {
        total = jam * 5000;
    } else {
        printf("Pilihan tidak valid!\n");
        return 0;
    }

    tambahan = 1000;
    total = total + tambahan;

    printf("Biaya tambahan: Rp%d\n", tambahan);
    printf("Total bayar: Rp%d\n", total);

    printf("Uang bayar: Rp");
    scanf("%d", &bayar);

    if (bayar >= total) {
        printf("Kembalian: Rp%d\n", bayar - total);
        printf("Terima kasih!\n");
    } else {
        printf("Uang tidak cukup!\n");
    }

    return 0;
}
