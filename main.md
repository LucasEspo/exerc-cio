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
                System.out.println("Insira os numeros que deseja subtrair:");
                num1 = l.nextDouble();
                num2 = l.nextDouble();
                operacao.subtrair(num1,num2);
            }
            
            if(opcao == 2){
                System.out.println("Insira primeiro o numero, em seguida a potencia:");
                num1 = l.nextDouble();
                num2 = l.nextInt();
                pot = operacao.calcularPotencia(num1,num2);
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
