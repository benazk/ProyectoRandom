import java.util.Arrays;
import java.util.Scanner;

public class ProyectoRandom {

	public static void main(String[] args) {
		int score[] = new int[10];
		int intentos = 0;
		int intentostotales = 0;
		int juegos = 0;

		double a = (int) Math.floor(Math.random() * 100 + 1);
		boolean bucle = true;
		System.out.println("Saludos aventurero, para pasar por este portón has de adivinar el numero secreto.");
		System.out.println("He sido notificado de que dicho numero se encuentra entre el 1 y el 100");
		System.out.println("Por que nombre he de llamarle?");
		Scanner nombre = new Scanner(System.in);
		String aventurero = nombre.nextLine();
		while (bucle == true) {
			System.out.println(aventurero + ", elija su proximo numero: " + a);
			Scanner scanner = new Scanner(System.in);
			int numinputeado = scanner.nextInt();
			intentos++;
			intentostotales++;
			if (numinputeado > a) {
				System.out.println("Ha excedido al número secreto");
			}
			if (numinputeado > 100 || numinputeado < 0) {
				System.out.println("Esta usted fuera de los límites impuestos");
			}
			if (numinputeado < a) {
				System.out.println("No alcanza el número secreto");
			}

			if (numinputeado == a) {
				System.out.println("Felicitaciones " + aventurero + ", está usted permitido a pasar por este portón");
				System.out.println("Ha hecho " + intentos + " intentos");

				System.out.println("Quiere enfrentarse a otro reto de adivinación? (Es opcional) S/N");
				Scanner escaneo = new Scanner(System.in);
				String jugarotro = escaneo.nextLine();
				if (jugarotro.equals("S")) {
					score[juegos] = intentos;
					juegos++;
					intentos = 0;
					bucle = true;
					a = (int) Math.floor(Math.random() * 100 + 1);

				}
				if (jugarotro.equals("N")) {
					score[juegos] = intentos;
					juegos++;
					System.out.println("Ha hecho " + juegos + " retos");
					System.out.println("Sus intentos totales han sido " + intentostotales);
					System.out.println("LISTA DE MEJORES VICTORIAS ");
					System.out.println("---------------------------------");
					Arrays.sort(score);
					int o = 6;
					for (int i = 9; i >= 5; i--) {
						o--;
						if (score[i] != 0)
							System.out.println("Puesto " + o + ": " + score[i] + " intentos");
					}
					bucle = false;
					break;
				}
			}

		}

	}
}
