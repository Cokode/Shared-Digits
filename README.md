# Shared-Digits
This program has two int parameters. it would return false for numbers in parameters not in the rage of 10-99 inclusively. The program will return true if there is a digit that appears in both numbers

public class SharedDigit {
    public static void main(String[] args) {
        System.out.println(hasSharedDigit(87, 77));
    }

    public static boolean hasSharedDigit(int x, int y) {
        if(x < 10 || x > 99 || y < 10 || y > 99) {
            return false;
        }

        int xDigit1 = x % 10;
        int xDigit2 = x / 10;
        int yDigit1 = y % 10;
        int yDigit2 = y / 10;

        return (xDigit1 == yDigit1 || xDigit1 == yDigit2 || xDigit2 == yDigit1 || xDigit2 == yDigit2);


    }
}
