class MyCalculator {
    // Method to calculate n^p
    public int power(int n, int p) {
        try {
            // Check if either n or p is negative
            if (n < 0 || p < 0) {
                throw new Exception("n and p should be non-negative");
            }
            // Calculate and return n^p
            return (int) Math.pow(n, p);
        } catch (Exception e) {
            // Handle the exception and print the message
            System.out.println(e.getMessage());
            return -1; // Return a value indicating an error
        }
    }

    public static void main(String[] args) {
        MyCalculator calculator = new MyCalculator();
        
        // Test cases
        System.out.println(calculator.power(2, 3)); // Should print 8
        System.out.println(calculator.power(-2, 3)); // Should print "n and p should be non-negative" and -1
    }
}
