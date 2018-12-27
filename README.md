# BestPlayer
import java.util.Scanner;

public class P02_BestPlayer {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String playerName = scanner.nextLine();
        String winnerName = "";
        int winnerGoals = Integer.MIN_VALUE;

        while (!playerName.equalsIgnoreCase("End")){

            int playerGoals = Integer.parseInt(scanner.nextLine());

            if (playerGoals > winnerGoals){
                winnerGoals = playerGoals;
                winnerName = playerName;
            }

            if (winnerGoals >= 10){
                break;
            }

            playerName = scanner.nextLine();

        }

        System.out.printf("%s is the best player!\n", winnerName);
        if (winnerGoals >= 3){
            System.out.printf("He has scored %d goals and made a hat-trick !!!", winnerGoals);
        }
        else {
            System.out.printf("He has scored %d goals.", winnerGoals);
        }

    }

}
