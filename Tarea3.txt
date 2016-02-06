import java.util.Scanner;

public class Tarea3{
	public static void main(String args[]){

		Scanner rd = new Scanner(System.in);
		boolean continuar = false;
		do{
			System.out.println("Ingrese el primer valor");
			int valor1 = rd.nextInt();
			System.out.println("Ingrese el segundo valor");
			int valor2 = rd.nextInt();
			System.out.println(" ---------------- ");
			System.out.println("Ingrese una opcion: ");
			System.out.println("1 = Sumar");
			System.out.println("2 = Restar");
			System.out.println("3 = Multi");
			System.out.println("4 = Dividir");
			System.out.println("5 = Salir");
			System.out.println("6 = Cambiar Valores");

			int menu =rd.nextInt();

			switch(menu){
				case 1: System.out.println(valor1 + valor2);
				break;
				case 2: System.out.println(valor1 - valor2);
				break;
				case 3: System.out.println(valor1 * valor2);
				break;
				case 4: System.out.println(valor1 / valor2);
				break;
				case 5: return;
				case 6: Tarea3.main(null);
				default: break;
			}

			System.out.println(" ------------ ");
			System.out.println("Intentar de Nuevo: Y/N");
			char continuarChar = rd.next().charAt(0);
			continuar = false;
			if(continuarChar == 'Y' || continuarChar == 'y'){
				continuar = true;
			}

		}while(continuar);
	}
}