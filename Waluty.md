# Projekt---waluty.
Przelicznik walut.



using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Waluty
{
    public partial class Form1 : Form
    {
        Double PLN = 1;
        Double Euro = 4.23;
        Double Dolar_Amerykanski = 3.65;
        Double Frank_Szwajcarski = 3.64;
        Double Funt = 4.81;
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            cmbWaluty.Text = "Wybierz walute";
            cmbWaluty.Items.Add("Euro");
            cmbWaluty.Items.Add("Funt");
            cmbWaluty.Items.Add("Frank Szwajcarski");
            cmbWaluty.Items.Add("Dolar Amerykanski");
        }

        private void button1_Click(object sender, EventArgs e)
        {
            Double Polski_Zloty = Double.Parse(textBox1.Text);
            if (cmbWaluty.Text == "Euro")
            {
                label1.Text = System.Convert.ToString(Polski_Zloty * Euro +"PLN");
            }

            if (cmbWaluty.Text == "Funt")
            {

                label1.Text = System.Convert.ToString(Polski_Zloty * Funt +"PLN");
            }

            if (cmbWaluty.Text == "Frank Szwajcarski")
            {
                label1.Text = System.Convert.ToString(Polski_Zloty * Frank_Szwajcarski + "PLN");

            }

            if (cmbWaluty.Text == "Dolar Amerykanski")
                {
                label1.Text = System.Convert.ToString(Polski_Zloty * Dolar_Amerykanski + "PLN");
            }
        }
    }
}
