# CMSC203_Lab4
/** 
*The purpose of this class is to model a television
*Tanna Nguyen, 08/29/2021
*/
import java.util.Scanner;
public class Television {
	
	// Attributes or fields
	private String MANUFACTURER; //hold brand name,CANNOT be changed
	private int SCREEN_SIZE;  //holds size of the television screen		boolean powerOn;  //holds value true when on, false when off
	private int channel; // holds value of the station that the television is showing
	private int volume; //holds the number value representing the loudness (0 being no sounds)
	private boolean powerOn;	
	
	public static void main(String[] args)
	{
		//create a Scanner object to read from the keyboard
		Scanner keyboard = new Scanner (System.in);
		//declare variables
		int station; //the user’s channel choice
		//declare and instantiate a television object
		Television bigScreen = new Television("Toshiba", 55);
		//turn the power on
		bigScreen.getPower();
		//display the state of the television
		System.out.println("A " + bigScreen.getSCREEN_SIZE() + "-inch " +
				bigScreen.getMANUFACTURER() + " has been turned on.");
		//prompt the user for input and store into station
		System.out.print("What channel do you want? ");
		station = keyboard.nextInt();
		//change the channel on the television
		bigScreen.setChannel(station);
		//increase the volume of the television
		bigScreen.increaseVolume();
		//display the the current channel and volume of the television
		System.out.println("Channel: " + bigScreen.getChannel() +
				", Volume: " + bigScreen.getVolume());
		System.out.println("Too loud!! I am lowering the volume.");
		//decrease the volume of the television
		bigScreen.decreaseVolume();
		bigScreen.decreaseVolume();
		bigScreen.decreaseVolume();
		bigScreen.decreaseVolume();
		bigScreen.decreaseVolume();
		bigScreen.decreaseVolume();
		//display the current channel and volume of the television
		System.out.println("Channel: " + bigScreen.getChannel() +
				", Volume: " + bigScreen.getVolume());
		System.out.println(); //for a blank line
		
		
		
		//HERE IS WHERE YOU DO TASK #5
		Television portable = new Television("Sharp", 19);
		portable.getPower();
	    System.out.println("A " + portable.getSCREEN_SIZE() + 
	    " inch " + portable.getMANUFACTURER() + " has been turned on.");
	    System.out.print("What channel do you want? ");
	    station = keyboard.nextInt();
	    portable.setChannel(station);
	    portable.decreaseVolume();
	    portable.decreaseVolume();
	    System.out.println("Channel: " + portable.getChannel() +" Volume: " +
	    portable.getVolume());
	}

		
		


		public Television (String brand, int size)   //this constructor initializes new object before use
	{
		this.MANUFACTURER = brand;
		this.SCREEN_SIZE = size;
		powerOn = false;
		volume = 20;
		channel = 2;		
	}
	
	
	//return the stored the the volume field
	public int getVolume() {
		return volume;
	}

	//return the value stored in the channel field
	public int getChannel() {
		return channel;
	}
	
	//return the constant value stored in the MANUFACTURER field
	public String getMANUFACTURER() {
		return MANUFACTURER;
	}
	
	//return the constant value stored in the SCREEN_SIZE field
	public int getSCREEN_SIZE() {
		return SCREEN_SIZE;
	}
	
	public boolean getPower() {
		return powerOn;
		
	}

	//store the desired station the channel field 
	public void setChannel(int channel) {
		this.channel = channel;
	}
	
	//toggle the power between on and off, changing the value from true to false and false to true
	public void getPower(boolean powerOn) {
		this.powerOn = !powerOn;
	}
	
	//increase the value  stored in the volume filed by 1  
	public void increaseVolume() {
		volume+=1;
	}
	
	//decrease the value stored in the volume field by 1
	public void decreaseVolume() {
		volume-=1;
	}
	
	
	
}
