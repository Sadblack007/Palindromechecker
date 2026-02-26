// case 1

public class PalindromeChecker {

    public static boolean isPalindrome(String str) {
        if (str == null) {
            return false;
        }
        String cleanStr = str.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        int left = 0;
        int right = cleanStr.length() - 1;

        while (left < right) {
            if (cleanStr.charAt(left) != cleanStr.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        // --- Use Case 1: Startup Display ---
        System.out.println("Welcome to the Palindrome Checker Application"); // Application Name
        System.out.println("Application Version: 1.0.0");                  // Application Version
        System.out.println("-------------------------------------------");

        // Existing logic continues below
        String testWord = "Racecar";
        if (isPalindrome(testWord)) {
            System.out.println(testWord + " is a palindrome.");
        } else {
            System.out.println(testWord + " is not a palindrome.");
        }
    }
}
