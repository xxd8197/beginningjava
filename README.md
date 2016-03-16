# beginningjava

//Food Survey

import java.util.Scanner;

public class FoodSurvey
{
	public static void main(String[] args)
	{
		Scanner input = new Scanner(System.in);
		int stinkytofu = 1, oyster = 2, braised = 3;
		int counter=0,tofucounter=0,oystercounter=0,braisedcounter=0;

		System.out.print("Please vote for your favorite Taiwanese snack.\nEnter 1 for stinky tofu\nEnter 2 for oyster pancakes\nEnter 3 for braised food\nEnter -1 to quit.\n");
		int vote = input.nextInt();
		counter += 1;
		if (vote == 1)
			{
				System.out.println("You voted for stinky tofu.");
				tofucounter += 1;
			}
			else if(vote == 2)
				{
					System.out.println("You voted for oyster pancakes.");
					oystercounter += 1;
				}
					else if(vote == 3)
					{
						System.out.println("You voted for braised food.");
						braisedcounter += 1;
					}
						else
						{
							System.out.println("Invalid Vote.");
							counter-=1;
						}
						
		while(vote != -1)
		{
			System.out.print("Please vote for your favorite Taiwanese snack.\nEnter 1 for stinky tofu\nEnter 2 for oyster pancakes\nEnter 3 for braised food\nEnter -1 to quit.\n");
			vote = input.nextInt();
			counter += 1;
		
			if (vote == 1)
			{
				System.out.println("You voted for stinky tofu.");
				tofucounter += 1;
			}
			else if(vote == 2)
				{
					System.out.println("You voted for oyster pancakes.");
					oystercounter += 1;
				}
					else if(vote == 3)
					{
						System.out.println("You voted for braised food.");
						braisedcounter += 1;
					}
						else
						{
							System.out.println("Invalid Vote.");
							counter-=1;
						}
		}
		
		System.out.printf("Thank you for voting! %d people (person) voted.\n%d people (person) voted for stinky tofu.\n%d people (person) voted for oyster pancakes.\n%d people (person) voted for braised food.\n",counter,tofucounter,oystercounter,braisedcounter);
		double perctofu, percoyster, percbraised;
		perctofu = (double)tofucounter/counter;
		percoyster = (double)oystercounter/counter;
		percbraised = (double)braisedcounter/counter;
		System.out.printf("%.2f percent of people voted for stinky tofu.\n%.2f percent of people.\n%.2f percent of people voted for braised food.\n",perctofu*100,percoyster*100,percbraised*100);
		
		if (tofucounter > oystercounter && tofucounter > braisedcounter)
		{
			System.out.println("The most amount of people picked stinky tofu.");
		}
			else if (oystercounter > tofucounter && oystercounter > braisedcounter)
			{
				System.out.println("The most amount of people picked oyster pancakes.");
			}
				else if (braisedcounter>tofucounter&&braisedcounter>oystercounter)
				{
					System.out.println("The most amount of people picked braised food.");
				}
					else
					{
						System.out.println("There is a tie between the most picked foods.");
					}
	}
}
