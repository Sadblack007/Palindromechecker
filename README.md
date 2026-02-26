public class PalindromeChecker {
    public static void main(String[] args) {
        String input = "Racecar";
        
        if (isPalindrome(input)) {
            System.out.println(input + " is a palindrome.");
        } else {
            System.out.println(input + " is not a palindrome.");
        }
    }

    public static boolean isPalindrome(String str) {
        // Clean the string: remove non-alphanumeric and convert to lowercase
        String cleanStr = str.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        
        int left = 0;
        int right = cleanStr.length() - 1;

        while (left < right) {
            if (cleanStr.charAt(left) != cleanStr.charAt(right)) {
                return false; // Found a mismatch
            }
            left++;
            right--;
        }
        return true;
    }
}
