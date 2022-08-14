# Encapsulation-
namespace encapsulation
{
    class program
    {
        static void Main(string[] args)
        {
            Ogrenci ogrenci1=new Ogrenci("melike","tutkun",585,1);
            ogrenci1.sinifdüşür();
            ogrenci1.ogrencibilgileri();
        }
    }
    class Ogrenci
    {
        private string isim;
        private string soyisim;
        private int no;
        private int sinif;

        public string Isim {
             get {return isim;}  
             set {isim = value;} 
              }
        public string Soyisim { get => soyisim; set => soyisim = value; }
        public int No { get => no; set => no = value; }
        public int Sinif 
        { 
            get => sinif; 
            set
            {
                if(value<1)
                {
                    Console.WriteLine("sınıf düşürülemez");
                     sinif=1;
                } 
                else
                {
                    sinif = value; 
                }
           
            }
        }
        public Ogrenci(string ısim = null, string soyisim = null, int no = 0, int sinif = 0)
        {
            Isim = ısim;
            Soyisim = soyisim;
            No = no;
            Sinif = sinif;
        }
        public Ogrenci(){}
        public void ogrencibilgileri()
        {
            Console.WriteLine("ad:"+this.Isim);
            Console.WriteLine("Soyisim:"+this.Soyisim);
            Console.WriteLine("No:"+this.No);
            Console.WriteLine("Sinif:"+this.Sinif);
        }
        public void sinifatlat()
        {
            this.sinif+=1;
        }
            public void sinifdüşür()
        {
            this.sinif-=1;
        }
    }
}
