import java.util.Scanner;
public class Main
{
    public static void main(String[] args){
        
        int opcao, i = 0;
        double pot, med;
        double num1, num2;
        
        Scanner l = new Scanner(System.in);
        
        Operacao operacao = new Operacao();
        
        while(i < 1){
            System.out.println("\n1 - subtrair\n2 - calcular potencia\n3 - calcular media ponderada\n4 - calcular fatorial\n5 - ENCERRAR PROGAMA");
            opcao = l.nextInt();
        
            if(opcao == 1){
                operacao.Subtrair();
            }
            
            if(opcao == 2){
                pot = operacao.calcularPotencia();
                System.out.println(pot);
            }
            
            if(opcao == 3){
                System.out.println("Insira os dois numeros que deseja saber a media ponderada:");
                num1 = l.nextDouble();
                num2 = l.nextDouble();
                med = operacao.calcularMediaPonderada(num1, num2);
                System.out.println(med);
            }
            
            if(opcao == 4){
                System.out.println("Insira o numero (inteiro) cujo fatorial deseja saber:");
                num1 = l.nextInt();
                operacao.calcularFatorial(num1);
            }
            
            if(opcao == 5){
                i ++;
            }
        }
        
        
    }
}
