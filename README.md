# snake5.java
public class Snake5 {
	public static void main(String[] args) {
	int startPosition = 0;
	int counter = 0;

	System.out.println("Start Position : " +startPosition);

	int diceValue=(int) Math.floor((Math.random()*6) + 1);	

	System.out.println("diceValue: "+diceValue);	

	while(startPosition < 100) {

		int checkOption = (int)(Math.random() * 10) % 3 + 1;

		System.out.println("check "+checkOption);

		counter++;
		switch(checkOption) {
			case 1:
					startPosition = startPosition + diceValue;
					if(startPosition > 100) {
						startPosition = startPosition -diceValue;
					}

			break;

			case 2:

					startPosition = startPosition - diceValue;
					if(startPosition < 0) {
						startPosition = 0;
					}
					break;
			default:

					System.out.println("Player is not playing " + startPosition);



					}

			System.out.println("total counter to win game: "+counter);
			System.out.println("player position:" +startPosition);

			}

	}

}
