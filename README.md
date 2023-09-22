# ProgramC_TLS23
Nicholas Shane Pangihutan Siahaan_Freedman
#include <iostream>
#include <cmath>

int main() {
	
    int JumlahSiswa;
    std::cout<<"Masukkan Jumlah Siswa: ";
    std::cin>>JumlahSiswa;
    double JumlahNilai = 0.0;
    double NilaiKurangRatarata = 0;
    double ratarata = 0.0;
    double nilai[JumlahSiswa];

    for (int i = 0; i < JumlahSiswa; i++) { 
        std::cout << "Masukkan nilai siswa " << i + 1 << " :";
        std::cin >> nilai[i];
        JumlahNilai += nilai[i];
    }

    ratarata = JumlahNilai / JumlahSiswa;

    for (int i = 0; i < JumlahSiswa; i++) { 
        NilaiKurangRatarata += pow(nilai[i] - ratarata, 2);
    }
	//Rata rata
    std::cout << "Rata-rata siswa adalah " << ratarata << std::endl;
    double varian = NilaiKurangRatarata / JumlahSiswa;
    
	//Varian
    std::cout << "Variannya adalah " << varian << std::endl;
    double simpangan = sqrt(varian);
    //Simpangan
    std::cout << "Simpangannya adalah " << simpangan << std::endl;

    return 0;
}
