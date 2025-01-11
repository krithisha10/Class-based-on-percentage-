import java.util.Scanner;


class Employee {
    // Fields
    private String name;
    private double currentSalary;
    private double percentageIncrease;


    // Getter and Setter methods
    public String getName() {
        return name;
    }


    public void setName(String name) {
        this.name = name;
    }


    public double getCurrentSalary() {
        return currentSalary;
    }


    public void setCurrentSalary(double currentSalary) {
        this.currentSalary = currentSalary;
    }


    public double getPercentageIncrease() {
        return percentageIncrease;
    }


    public void setPercentageIncrease(double percentageIncrease) {
        this.percentageIncrease = percentageIncrease;
    }


    // Method to calculate the new salary after the percentage increase
    public double calculateNewSalary() {
        return currentSalary + (currentSalary * percentageIncrease / 100);
    }


    // Method to display employee details
    public void displayDetails() {
        System.out.println("Employee Name: " + name);
        System.out.println("Current Salary: " + currentSalary);
        System.out.println("Percentage Increase: " + percentageIncrease + "%");
        System.out.println("New Salary: " + calculateNewSalary());
    }
}


public class SalaryIncrease {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        // Create an employee object
        Employee employee = new Employee();


        // Input employee details
        System.out.print("Enter Employee Name: ");
        employee.setName(scanner.nextLine());


        System.out.print("Enter Current Salary: ");
        employee.setCurrentSalary(scanner.nextDouble());


        System.out.print("Enter Percentage Increase: ");
        employee.setPercentageIncrease(scanner.nextDouble());


        // Display employee details and new salary
        employee.displayDetails();


        // Close the scanner
        scanner.close();
    }
}


OUTPUT:
Enter Employee Name: John Doe
Enter Current Salary: 50000
Enter Percentage Increase: 10
Employee Name: John Doe
Current Salary: 50000.0
Percentage Increase: 10.0%
New Salary: 55000.0

