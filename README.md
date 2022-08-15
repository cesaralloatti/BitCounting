# misejercicios
Ejercicios
package BitCounting;

import java.util.Scanner;

public class countBits {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        String binario = "";
        int modulo;
        System.out.println("Ingrese su numero a convertir: ");
        int entrada = input.nextInt();



        if (entrada<0){
            entrada = entrada*-1;
        }

        while (entrada > 0) {
            modulo = entrada%2;
            binario = binario + modulo;
            entrada /= 2;
        }

        String conversion = "";
        for (int i = binario.length()-1; i >= 0; i--) {
            conversion += binario.charAt(i);
        }

        System.out.println("el numero " + entrada + " en binario es igual a :" + conversion + ".");


    }



}
