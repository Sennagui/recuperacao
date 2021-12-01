
   package sample.model;

   public abstract class  Pessoa {
    private String nome;

    public Pessoa(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    
    @Override
    public String toString() {
        return "\nNome: " + nome;
    }

    public Pessoa(String telefone) {
        this.telefone = telefone;
    }

    public String getTelefone() {
        return telefone;
    }

    @Override
    public String toString() {
        return "\nTelefone: " + telefone;
    }


    public class Professor extends Pessoa {

    private String salario;

    public String getSalario() {
        return salario;
    }

    public void setSalario(String salario) {
        this.salario = salario;
    }

    public class Aluno extends Pessoa{
    private int nota1;
    private int nota2;
    private double media;


    public Aluno(String nome, int nota1, int nota2, double media) {
        super(nome);
        this.nota1 = nota1;
        this.nota2 = nota2;
        this.media = media;
    }

    public int getNota1() {
        return nota1;
    }

    public void setNota1(int nota1) {
        this.nota1 = nota1;
    }

    public int getNota2() {
        return nota2;
    }

    public void setNota2(int nota2) {
        this.nota2 = nota2;
    }

    public double getMedia() {
        return media;
    }

    public void setMedia(double media) {
        this.media = media;
    }

    @Override
    public String toString() {
        return super.toString() + " - Aluno " + "\nNota 1: " + nota1 + "\nNota 2: " + nota2 + "\nMédia: " + media;
    }


    public class Endereço extends Pessoa {
  
    private String Rua;
    private int Uf;
    private String CEP;
    private String Cidade;
    private String Pais;

    public void setRua(String Rua) { this.Rua = Rua; }

    public String getRua() { return this.Rua; }

    public void setUf(int Uf) { this.Uf = Uf; }

    public int getUf() { return this.Uf; }

    public void setCep(String Cep) { this.Cep = Cep; }

    public String getCep() { return this.Cep; }

    public void setCidade(String Cidade) { this.Cidade = Cidade; }

    public String getCidade() { return this.Cidade; }

    public void setPais(String Pais) { this.Pais = Pais; }

    public String getPais() { return this.Pais; }

    public String toString() {
        return "Uf " + Rua + ", " + Cep + ", " + Pais + ", " + Cidade;

    }

}

