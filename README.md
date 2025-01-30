# 34.Interface
package calculaterprogram;
import java.util.Scanner;
import javafx.beans.binding.Bindings;
interface Calculater {
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculater implements Calculater {
    @Override
    public double add(double a,double b){
    return a+b;
}
    @Override
    public double subtract(double a,double b) {
        return a-b;
    }
    @Override
    public double multiply(double a,double b) {
        return a*b;
    }
    @Override
    public double divide(double a,double b) {
        if(b==0){
            System.out.println("Error:Division by zero not allowed!");
            return Double.NaN;
        }
        return a/b;
        }
    }
public class CalculaterProgram {
    public static void main(String[] args) {
        // TODO code application logic here
   Scanner scanner=new Scanner(System.in);
   Calculater calculater=new SimpleCalculater();
        System.out.println("Welcome to the Simple Calculater");
        System.out.println("Enter rhe first number");
    double num1=scanner.nextDouble();
        System.out.println("Enter the second number");
    double num2=scanner.nextDouble();
        System.out.println("\n Results");
        System.out.println("Addition:"+ calculater.add(num1, num2));
        System.out.println("Subtraction"+ calculater.subtract(num1, num2));
        System.out.println("Multiplication"+ calculater.multiply(num1, num2));
        System.out.println("Division"+ calculater.divide(num1, num2));
        scanner.close();
    }
    
}


Output
Welcome to the Simple Calculater
Enter rhe first number

45
Enter the second number
30

 Results
Addition:75.0
Subtraction75.0
Multiplication1350.0
Division1.5
