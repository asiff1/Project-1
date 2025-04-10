# Project-1

import java.util.Scanner;

// Donor class
class Donor {
    String name;
    String bloodGroup;
    
    // Constructor
    Donor(String name, String bloodGroup) {
        this.name = name;
        this.bloodGroup = bloodGroup;
    }
    
    // Method to display donor information
    public void displayDonorInfo() {
        System.out.println("Donor Name: " + name);
        System.out.println("Blood Group: " + bloodGroup);
    }
}

// BloodDonationSystem class
public class BloodDonationSystem {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Create a simple menu
        System.out.println("Welcome to the Blood Donation System");
        
        // Register donor
        System.out.print("Enter your name: ");
        String donorName = scanner.nextLine();
        
        System.out.print("Enter your blood group (e.g., A+, B-, O+): ");
        String donorBloodGroup = scanner.nextLine();
        
        // Create a donor object
        Donor donor = new Donor(donorName, donorBloodGroup);
        
        // Display donor information
        donor.displayDonorInfo();
        
        // Blood group matching (basic example)
        System.out.println("\nLooking for a donor with blood group A+...");
        
        if (donor.bloodGroup.equals("A+")) {
            System.out.println("This donor is a match!");
        } else {
            System.out.println("This donor is not a match for blood group A+.");
        }
        
        scanner.close();
    }
}
