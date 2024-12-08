# GCD
Greatest common Divisor in java
import java.util.Scanner;

public class gcd {
    public gcd() {
    }

    static int gcd(int a, int b) {
        if (a != 0 && b != 0) {
            if (a == b) {
                return a;
            } else {
                return a > b ? gcd(a - b, b) : gcd(a, b - a);
            }
        } else {
            return 0;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a: ");
        int a = sc.nextInt();
        System.out.println("Enter b: ");
        int b = sc.nextInt();
        System.out.println("GCD(" + a + "," + b + ")= " + gcd(a, b));
    }
}
