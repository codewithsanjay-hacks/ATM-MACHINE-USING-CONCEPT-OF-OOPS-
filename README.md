# ATM-MACHINE-USING-CONCEPT-OF-OOPS-
ITS ONLY BASIC OF CLASSES AND OBJECT IN JAVA
import java.util.*;

class atmbob {
    int PIN = 3257;
    float balance = 100f;

    void checkpin() {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter Your Pin");
        int enterpin = input.nextInt();

        if (enterpin == PIN) {
            main();
        } else {
            System.out.println("Enter Valid Pin");
        }
        
    }

    void main(){
        System.out.println("Enter your option");
        System.out.println("1: Check Balance");
        System.out.println("2: Deposit Money");
        System.out.println("3: Withdrwal Money");
        System.out.println("4: Exit");

        Scanner input = new Scanner(System.in);
        int option = input.nextInt();

        if (option==1) {
            checkbalance();
        }else if(option==2) {
            depositemoney();
        }else if(option==3) {
            withdrawlmoney();
        }else if(option==4) {
            return;
        }else{
            System.out.println("Enter Valid choice");


        }

}
   void checkbalance(){
       System.out.println("Balance amount is"+balance);
       main();

   }
   void depositemoney(){
       System.out.println("Enter Depositing Money ");
       Scanner input = new Scanner(System.in);
       float amount = input.nextInt();
       balance+=amount;
       System.out.println("Your money Succesfully Deposited");
       main();

   }

    void withdrawlmoney(){
        System.out.println("Enter witdrawl Money ");
        Scanner input = new Scanner(System.in);
        float amount = input.nextInt();
        if(amount>balance){
            System.out.println("Insuffcient Funds");
        }else{
        balance-=amount;
        System.out.println("Your money Succesfully withdrawl");
        }
        main();
        }
    



public class ATM{
    public static void main(String[] args) {
      atmbob obj = new atmbob();
        obj.checkpin();
    }
}
}
