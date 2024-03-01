public partial class Form1 : Form
    {
        int[,] dizi;
        int satirSayısı;
        int sutunSayısı;

        public Form1()
        {
            InitializeComponent();
        }

        private void btnOlustur_Click(object sender, EventArgs e)
        {
            int rastgeleMin = int.Parse(txtRasgeleMin.Text);
            int rastgeleMax = int.Parse(txtRasgeleMax.Text);
            satirSayısı = int.Parse(txtSatir.Text);
            sutunSayısı = int.Parse(txtSutunSayısı.Text);
            dizi = new int[satirSayısı,sutunSayısı];
            Random rastgele = new Random();
            for (int i = 0; i < satirSayısı; i++)
            {
                for (int k = 0; k < sutunSayısı; k++)
                {
                    dizi[i, k] = rastgele.Next(rastgeleMin, rastgeleMax);
                }

            }



        }

        private void btnListele_Click(object sender, EventArgs e)
        {
            for (int i = 0; i < satirSayısı; i++)
            {
                for (int k = 0; k < sutunSayısı; k++)
                {
                    listeDizi.Items.Add(i + "," + k + "=>" + dizi[i, k]);
                }
            }
        }
    }

