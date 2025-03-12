import java.util.Scanner;

Scanner keyboard = new Scanner(System.in);

String productName1 = "Stylos"; 
double unitPrice1 = 1.2; 

System.out.printf("How many %s at €%.2f ?\n", productName1, unitPrice1);
int quantity1 = keyboard.nextInt();

String productName2 = "Cahier";
double unitPrice2 = 3.5;

System.out.printf("How many %s à €%.2f ?\n", productName2, unitPrice2);
int quantity2 = keyboard.nextInt();

keyboard.close();

double total = 0;

System.out.println("+---------------+---------+-----+----------+");
System.out.println("| Product       | € Unit  | Qty |   price  |");
System.out.println("+---------------+---------+-----+----------+");

double price1 = unitPrice1 * (double)quantity1;

total += price1;
System.out.printf("| %-13s | %6.2f€ | %3d | %7.2f€ |\n", productName1, unitPrice1, quantity1, price1);

double price2 = unitPrice2 * (double)quantity2;

total += price2;
System.out.printf("| %-13s | %6.2f€ | %3d | %7.2f€ |\n", productName2, unitPrice2, quantity2, price2);

System.out.println("+---------------+---------+-----+----------+");
System.out.printf("                                | %7.2f€ |\n", total);
System.out.println("                                +----------+");