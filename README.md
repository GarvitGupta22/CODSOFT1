
import java.util.*;
public class RandomNumber {
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        Random random = new Random();
        int max = 5;
        int count = 0;
        int guess =0;
        boolean str = true;
        while(str){
            int num = random.nextInt(100);
            System.out.println("You have only "+max+" chance to guess number between 1-100");
            System.out.println();
            while(count != max){
                System.out.println("                ---------------- Chance" +" "+ (count+1)+" -------------------");
                System.out.println();
                System.out.print("Guess Number : ");
                guess = sc.nextInt();
                if(guess==num){
                    System.out.println("Congratulation! You Guess A Number Perfectly in" + " " + (count+1)+" "+"Chance");
                    break;
                }
                else if(guess>num){
                    System.out.println("**************** (You Guess Too High!) *****************");
                    System.out.println();
                }
                else{
                    System.out.println("**************** (You Guess Too Low!) ******************");
                    System.out.println();
                }
                count++;
            }
            if(guess != num){
                System.out.println("You Lost your all Turn");
                System.out.println("Guess Number : "+num);
            }
            System.out.print("Do You Want To Play Again(y/n) : ");
            String s = sc.next();
            str = s.equalsIgnoreCase("y");
            count=0;


        }
        System.out.print("Thank You , Hope You Enjoyed A Game!");


    }
}
