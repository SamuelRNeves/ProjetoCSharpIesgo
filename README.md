# ProjetoCSharpIesgo
repositório destinado ao projeto de sistemas de vendas completo em c# 
using System.Xml.Linq;

namespace Calculadora01
{
    public partial class Form1 : Form
    {
        public decimal Resultado { get; set; }
        public decimal Valor { get; set; }

        private Operacao OperacaoSelecionada { get; set; }
        private enum Operacao
        {
            Soma,
            Subtracao,
            Multiplicacao,
            Divisao
        }
        public Form1()
        {
            InitializeComponent();
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void btnZero_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "0";
        }

        private void btnUm_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "1";
        }

        private void btnDois_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "2";
        }

        private void btnTres_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "3";
        }

        private void btnQuatro_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "4";
        }

        private void btnCinco_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "5";
        }

        private void btnSeis_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "6";
        }

        private void btnSete_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "7";
        }

        private void btnOito_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "8";
        }

        private void btnNove_Click(object sender, EventArgs e)
        {
            txtResultado.Text += "9";
        }

        private void btnSoma_Click(object sender, EventArgs e)
        {
            OperacaoSelecionada = Operacao.Soma;

            Valor = Convert.ToDecimal(txtResultado.Text);
            txtResultado.Text = "";
           
        }

        private void btnSubtracao_Click(object sender, EventArgs e)
        {
            OperacaoSelecionada = Operacao.Subtracao;
            Valor = Convert.ToDecimal(txtResultado.Text);
            txtResultado.Text = "";
            
        }

        private void btnMultiplicacao_Click(object sender, EventArgs e)
        {
            OperacaoSelecionada = Operacao.Multiplicacao;
            Valor = Convert.ToDecimal(txtResultado.Text);
            txtResultado.Text = "";
            

        }

        private void btnDivisao_Click(object sender, EventArgs e)
        {
            OperacaoSelecionada = Operacao.Divisao;
            Valor = Convert.ToDecimal(txtResultado.Text);
            txtResultado.Text = "";
            
        }

        private void btnIgual_Click(object sender, EventArgs e)
        {
            switch (OperacaoSelecionada)
            {
                case Operacao.Soma:
                    Resultado = Valor + Convert.ToDecimal(txtResultado.Text);
                    break;
                case Operacao.Subtracao:
                    Resultado = Valor - Convert.ToDecimal(txtResultado.Text);
                    break;
                case Operacao.Multiplicacao:
                    Resultado = Valor * Convert.ToDecimal(txtResultado.Text);
                    break;
                case Operacao.Divisao:
                    Resultado = Valor / Convert.ToDecimal(txtResultado.Text);
                    break;


            }
            txtResultado.Text = Convert.ToString(Resultado);
        }

        private void btnVirgula_Click(object sender, EventArgs e)
        {
            if (!txtResultado.Text.Contains(","))
                txtResultado.Text += ",";
        }

        private void btnLimpar_Click(object sender, EventArgs e)
        {
            txtResultado.Text = "";
            
        }
    }
}
