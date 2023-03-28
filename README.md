# Java-project
#Atm interface using java language
package basics;
import java.util.Scanner;

public class AtmMachine {

public static void main(String[] args) {
int balance=100000,withdraw,deposite;
Scanner sc=new Scanner(System.in);
System.out.println("ATM(Automated Teller Machine)");
System.out.println("choose 1 for withdraw");
System.out.println("choose 2 for deposite");
System.out.println("choose 3 for check balance");
System.out.println("choose 4 for Exit");
System.out.println("choose  the operation you want to perform:");

int choi = sc.nextInt();

switch(choi)
{
case 1:
System.out.println("enter amount of to be withdraw");
withdraw = sc.nextInt();
if(balance >=withdraw)
{
balance=balance-withdraw;
System.out.println("withdrawal successful."+balance);

}
else
{
System.out.println("your balance is low");

}
System.out.println("");
break;
case 2:
System.out.println("enter amount to be deposited:");
deposite=sc.nextInt();
balance=balance+deposite;
System.out.println("your money has been successfully deposited:"+balance);
System.out.println("");
break;
case 3:
System.out.println("available balance:"+balance);
System.out.println("");
break;
case 4:
System.out.println("successfully exit.");
System.exit(0);


}

}

}

