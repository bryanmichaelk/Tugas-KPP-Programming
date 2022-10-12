# Tugas-KPP-Programming
// NAMA		:Bryan Michael Kurniawan
// NRP		:5026221025
// Jurusan	:Sistem Informasi

#include <iostream>
#include <cmath>

#define GRAVITASI 10 
#define START_PENGUKURAN 1 
#define SUDUT 45
int speed_dgn_loss(int kecepatanTangensial)
{
    int losses, kecepatanAwal;
	if (kecepatanTangensial >= 1 && kecepatanTangensial <= 10){
        losses = 1;
        kecepatanAwal = kecepatanTangensial - losses;
    }else if (kecepatanTangensial >= 11 && kecepatanTangensial <= 20){
        losses = 3;
        kecepatanAwal = kecepatanTangensial - losses;
    }else if (kecepatanTangensial >= 21 && kecepatanTangensial <= 30){
        losses = 5;
        kecepatanAwal = kecepatanTangensial - losses;
    }
    return kecepatanAwal;
}

int main() {
    int kecepatanTangensial, sudut = 45, gravitasi = 10, kecepatanLoss, losses, jarak;
    float kecepatanAwal, kecepatanTangensialR, kecepatanAwallLosses;
    std::cin >> kecepatanTangensial;
    kecepatanLoss = speed_dgn_loss(kecepatanTangensial); 
    if (sudut = 45){
        jarak = (pow(kecepatanLoss, 2))/gravitasi;
        kecepatanAwal = sqrt(jarak*gravitasi);
    }
    if (kecepatanTangensial >= 1 && kecepatanTangensial <= 10){
        losses = 1;
    }else if (kecepatanTangensial >= 11 && kecepatanTangensial <= 20){
        losses = 3;
    }else if (kecepatanTangensial >= 21 && kecepatanTangensial <= 30){
        losses = 5;
    }
    kecepatanTangensialR = kecepatanAwal + losses;
    std::cout << jarak<< " "<< kecepatanTangensialR <<std::endl;
    return 0;
}
