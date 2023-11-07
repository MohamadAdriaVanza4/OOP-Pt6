# Repository ini dibuat untuk memenuhi tugas Pemrograman Orientasi Objek 

 Kita akan buat program dengan menggunakan codingan sebagai berikut :
            
            using System;
            
            namespace TugasPt6{
            
                public class Pegawai{
                    private string _nama;
            
                    private double _gajiPokok;
                    public void setNama(string paramNama){
                        _nama = paramNama;
                    }
            
                    public string getNama(){
                        return _nama;
                    }
            
            
                    public void setGajiPokok(double paramGaji){
                        _gajiPokok = paramGaji;
                    }
                    public double getGajiPokok(){
                        return _gajiPokok;
                    }
            
                    public virtual void cetakInfo(){
                        Console.WriteLine( "Pegawai : " + getNama());
                        Console.WriteLine( "Gaji Pokok : " + getGajiPokok());
                    }
                }
                public class Manager : Pegawai{
                    private double _tunjangan;
            
                    public void setTunjangan(double paramTunjangan){
                        _tunjangan = paramTunjangan;
                    }
                    public double getTunjangan(){
                    return _tunjangan;
                    }
            
                    public void cetakTunjangan(){
                        Console.WriteLine( "Tunjangan Anda : " + getTunjangan());
                    }
                    public virtual void cetakInfo(){
                        Console.WriteLine( "Pegawai : " + getNama());
                        Console.WriteLine( "Posisi anda : Manager");
                        Console.WriteLine( "Gaji Pokok Anda : " +  getGajiPokok());
                    }
                }   
                public class Programmer : Pegawai{
                    private double _bonus;
                    public void setBonus(double paramBonus){
                        _bonus = paramBonus;
                    }
                    public double getBonus(){
                        return _bonus;
            
                    }
                    public void cetakBonus(){
                        Console.WriteLine("Bonus Anda : " + getBonus());
                    }
                    public virtual void cetakInfo(){
                    Console.WriteLine( "Pegawai : " + getNama());
                    Console.WriteLine( "Posisi : Programmer" );
                    Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
                    }
                }
                class Program{
            
                    static void Main(string[] args){
                        Console.WriteLine( "===========Pegawai Class===========");
                        Pegawai pegawai = new Pegawai();
                        pegawai.setNama ("Vanza Pegawai");
                        pegawai.setGajiPokok(1500000);
                        pegawai.cetakInfo();
            
                        Console.WriteLine("============Manager Class===========");
                        Manager manager = new Manager();
                        manager.setNama( "Vanza Manager");
                        manager.setGajiPokok(25000000);
                        manager.setTunjangan (2000000);
                        manager.cetakInfo();
                        manager.cetakTunjangan();
            
                        Console.WriteLine("============Programer Class==========");
                        Programmer programmer = new Programmer();
                        programmer.setNama( "Vanza Programer");
                        programmer.setGajiPokok (20000000);
                        programmer.setBonus(1200000);
                        programmer.cetakInfo();
                        programmer.cetakBonus();
                    }
                }
            
            }


Dan untuk hasilnya akan seperti ini :

![OOP](https://github.com/MohamadAdriaVanza4/OOP-Pt7/assets/115931631/f98c23d8-b702-44a6-b435-efb20268a47d)
