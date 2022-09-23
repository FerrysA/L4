# L4
import java.util.Scanner;

public class sem {
    private static Scanner inn = new Scanner(System.in);

    public static long numberOfDivisors(int n) {
        long count = 0;
        int i = 1;
        while (i < Math.sqrt(n)) {
            if (n % i == 0) {
                count++;
            }
            i++;
        }
        if (Math.pow((int) Math.sqrt(n), 2) == n) {
            return count * 2 + 1;
        }
        return count * 2;
    }

    public static <string> void main(String[] args) {
        System.out.println("введите натуральное чилсо до 50 000");
        int n = inn.nextInt();
        System.out.println(n);

        System.out.println(numberOfDivisors(n));
    }
}
