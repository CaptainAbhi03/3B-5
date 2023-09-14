import java.util.Scanner;

public class MaxElementInEachRow {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get the number of rows and columns from the user
        System.out.print("Enter the number of rows: ");
        int numRows = scanner.nextInt();

        System.out.print("Enter the number of columns: ");
        int numCols = scanner.nextInt();

        // Create a 2D array
        int[][] matrix = new int[numRows][numCols];

        // Input values into the 2D array
        System.out.println("Enter the elements of the 2D array:");
        for (int i = 0; i < numRows; i++) {
            for (int j = 0; j < numCols; j++) {
                System.out.print("Enter element at row " + i + ", column " + j + ": ");
                matrix[i][j] = scanner.nextInt();
            }
        }

        // Find and display the maximum element in each row
        System.out.println("Maximum elements in each row:");
        for (int i = 0; i < numRows; i++) {
            int max = matrix[i][0]; // Assume the first element is the maximum

            for (int j = 1; j < numCols; j++) {
                if (matrix[i][j] > max) {
                    max = matrix[i][j];
                }
            }

            System.out.println("Row " + i + ": " + max);
        }
    }
}
