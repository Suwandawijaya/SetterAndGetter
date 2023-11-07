# SetterAndGetter
## Repository ini di buat untuk memenuhi tugas pertemuan 6 Pemprograman Orientasi Objek

Nama: Suwanda Wijaya <br>
NIM:312210028<br>
Kelas: TI.22.B1<br>

### Latihan Setter dan Getter
Source Code:
```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Tugas6
{
    public class Pegawai
    {
        

        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {
           
        private double tunjangan;

        public void setTunjangan(double tunjangan){this.tunjangan = tunjangan;}
        public double getTunjangan(){return this.tunjangan;}

        public new void cetakinfo()
        {
            
            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);
            
        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);
            
            
        }
        
    }
    class program
    {
        static void Main(string[] args) 
        {
            Console.WriteLine("==== PEGAWAI ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Suwanda Wijaya");
            pegawai.setGajiPokok(4500000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER ====");
            manager Manager = new manager();
            Manager.setNama("Suwanda Wijaya");
            Manager.setGajiPokok(6500000);
            Manager.setTunjangan(50000000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER ====");
            Programmer programer = new Programmer();
            programer.setNama("Suwanda Wijaya");
            programer.setGajiPokok(5000000);
            programer.setBonus(100000000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}
```


Hasil Latihan :
![SetterGetter.jpg](SetterGetter.jpg)