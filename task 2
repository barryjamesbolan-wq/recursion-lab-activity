/* Description: Recursive binary search on a user-entered array. Sorts the
 *              input, then recursively searches for a target value,
 *              printing the low/high/mid values at every recursive call.
 * Programmed by: <Your Name> <Your Course & Section> <Instructor/CN> <Subject>
 * Last Modified: <date of latest revision>
 * Version: 1.0
 * Acknowledgements: Claude (Anthropic), Claude Sonnet 5, accessed via
 *   claude.ai - used for code drafting and explanation. See AI disclosure
 *   statement in the lab document for full details.
 */
 
import java.util.Arrays;
import java.util.Scanner;
 
public class BinarySearch {
 
    public static int binarySearch(int[] arr, int low, int high, int target) {
        if (low > high) {
            System.out.println("binarySearch(" + low + ", " + high + ", target) -> not found");
            return -1;
        }
 
        int mid = low + (high - low) / 2;
        System.out.println("binarySearch(" + low + ", " + high + ", target) -> mid = " + mid + ", array[mid] = " + arr[mid]);
 
        if (arr[mid] == target) {
            return mid;
        } else if (target < arr[mid]) {
            return binarySearch(arr, low, mid - 1, target);
        } else {
            return binarySearch(arr, mid + 1, high, target);
        }
    }
 
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
 
        System.out.print("Number of elements: ");
        int n = sc.nextInt();
 
        int[] arr = new int[n];
        System.out.println("Enter " + n + " array elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
 
        Arrays.sort(arr);
        System.out.println("Sorted array: " + Arrays.toString(arr));
 
        System.out.print("Target: ");
        int target = sc.nextInt();
 
        int result = binarySearch(arr, 0, arr.length - 1, target);
 
        if (result != -1) {
            System.out.println("Target found.");
            System.out.println("Index: " + result);
        } else {
            System.out.println("Target not found.");
            System.out.println("Index: -1");
        }
 
        sc.close();
    }
}
