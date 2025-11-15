import java.util.Scanner;

public class Conversão {
public static void main (String[] args) {
    Scanner sc = new Scanner(System.in);

    while (true) {
        
        System.out.println("\n***** Conversões entre bases numéricas *****");
        System.out.println("1 - Decimal para binário");
        System.out.println("2 - Decimal para hexadecimal");
        System.out.println("3 - Binário para decimal");
        System.out.println("4 - Hexadecimal para decimal");
        System.out.println("5 - sair");
        System.out.print("Escolha uma opção: ");
        int op = sc.nextInt();
        sc.nextLine();

        switch (op) {

            case 1:
            System.out.print("Digite um número decimal: ");
            int dec = sc.nextInt();
            System.out.println("Binário " + Integer.toBinaryString(dec));
            break;

            case 2:
            System.out.print("Digite um número decimal: ");
            int decHex = sc.nextInt();
            System.out.println("Hexadecimal: " + Integer.toHexString(decHex).toUpperCase());
            break;

            case 3:
             System.out.print("Digite um número binário: ");
            String bin = sc.nextLine();
            int decimalBin = Integer.parseInt(bin, 2);
            System.out.println("Decimal: " + decimalBin);
            break;

            case 4:
            System.out.print("Digite um número hexadecimal: ");
            String hex = sc.nextLine();
            int decimalHex = Integer.parseInt(hex, 16);
            System.out.println("Decimal: " + decimalHex);
            break;
            
            case 0:
            System.out.println("Encerrado, obrigado!!!");
            sc.close();
            return;

            default:
            System.out.println("Opção incorreta!!!");

            sc.close();
            }
        }
    }
}
