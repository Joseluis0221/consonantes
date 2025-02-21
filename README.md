import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    System.out.println("Introduce una palabra en minúsculas sin símbolos, caracteres especiales, acentos, ni números:");
    String palabra = scanner.nextLine();

    int vcount = 0;
    int ccount = 0;

    palabra = palabra.toLowerCase();

    for (int i = 0; i < palabra.length(); i++) {
      char ch = palabra.charAt(i);
      if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
        vcount++;
      } else if ((ch >= 'a' && ch <= 'z')) {
        ccount++;
      }
    }

    System.out.println("Número de vocales: " + vcount);
    System.out.println("Número de consonantes: " + ccount);
  }
}
