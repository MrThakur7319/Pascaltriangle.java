# Pascaltriangle.java
public class PascalTriangle {
    public static void main(String[] args) {
        // Number of rows to generate in Pascal's triangle
        int rows = 6;  

  // Outer loop: iterate through each row (0 to rows-1)
        for (int i = 0; i < rows; i++) {
            // Initialize the first number in each row (always 1)
            int number = 1;

  // Inner loop 1: Print leading spaces for triangle alignment
            // Each row needs (rows - current_row) spaces for proper centering
            for (int s = 0; s < rows - i; s++) {
                System.out.print(" ");
            }

   // Inner loop 2: Generate and print numbers for current row
            // Row i has (i+1) numbers: from position 0 to position i
            for (int j = 0; j <= i; j++) {
                System.out.print(number + " ");
                
  // Calculate next number using binomial coefficient formula
                // C(n,k+1) = C(n,k) * (n-k) / (k+1)
                // where n=i (current row) and k=j (current position)
                number = number * (i - j) / (j + 1); 
            }
            
  // Move to next line after completing current row
            System.out.println(); 
        }
    }
}
