Homework19
==========
public class Dice {
  private int sRollcount = 0;
  private int nDiceNumber = 1;
public void DiceCount(int y){
  nDiceNumber = y;
	
}
  public Dice() {
	  sRollcount = 0;
	  nDiceNumber =1;
  }
  public int RollDice(){
	  int random;
	  random = 1 + (int) (Math.random()*6)* nDiceNumber;
	  sRollcount = sRollcount + nDiceNumber;
	  return random;
  }
  public int Rollcount(){
	  return sRollcount;
  }
  public String RollCountMsg(){
	  return "Roll Dices at this moment:" + sRollcount;
  }
}
public class DiceTest {
  public static void main(String[] args) {
    Dice D1 = new Dice();
  	Dice ThreeDices = new TripleDice();
  	
  	System.out.println("Dice roll output: " + D1.RollDice());
	System.out.println("Dice roll output: " + D1.RollDice());
	System.out.println("Dice roll output: " + D1.RollDice());

	System.out.println("TrippleDice roll output: " + ThreeDices.RollDice());
	System.out.println("TrippleDice roll output: " + ThreeDices.RollDice());
	System.out.println("TrippleDice roll output: " + ThreeDices.RollDice());

	System.out.println("Dice rollcount: " + D1.RollCountMsg());
	System.out.println("ThreeDices rollcount: " + ThreeDices.RollCountMsg());
  	
  	
  }
}

  public class TripleDice extends Dice {

		public void TrippleDice(){
			super.DiceCount(3);
		}

		public String RollCountMsg()
		  {
			String msg;
			msg = "Calling my super to get ";
			msg = msg + super.RollCountMsg();
		  	return msg ;
		  }

	}

