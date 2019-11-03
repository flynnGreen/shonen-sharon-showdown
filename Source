//SHONEN SHARON SHOWDOWN
//All code by Flynn Green
//Summary: Sharon, the suburb's ruling mom and your new neighbor, comes to your house with quinoa to get to know you
//As you talk, Sharon is going to start getting more and more aggressive as she realizes you may pose a threat
//By the end it'll be straight up implied hostility and veiled threats, but with a smile the whole time
//Right up until she has a breakdown, before quickly and inexplicably recovering
//Before she leaves she'll just smile pleasantly and deliver the wham line

#include <iostream>
#include <string>
using namespace std;

void Clear();
string Menu(int numArray, string array[]);
void Quinoa(int loopNum);
int GetInteger();
int Check(int min, int max);

const string SHARON = "Sharon";

int main()
{
	//Declare const variables
	const int typeAmt = 4; //If you change this, alter the elements of the 'types' array to match
	const int kidsAmt = 6; //If you change this, alter the elements of the 'kids' array to match
	const int statAmt = 8; //If you change this, alter the elements of the 'statNames' array to match

	int select = 0;
	int points = 150;
	int num = 0;
	int quinoaLoop = 0;

	//All possible options for selection
	string types[typeAmt] = { "PTA Mom", "Soccer Mom", "Scourge Mother: Bane of Retail Workers", "Hot Single Mom in your area" };
	string kids[kidsAmt] = { "Brody", "McKynleigh", "Hunter, but with a y", "Nyarlathotep, The Crawling Chaos", "Brooklynn", "Brooklynn Nyne-Nighn" };
	string statNames[statAmt] = { "minivan driving", "antivax posting", "sharing Facebook memes", "engaging in casual racism",
		"living vicariously through the children", "passive aggression", "calling salt a spice", "demanding the manager" };
	int stats[statAmt] = {};

	//Final choices
	string name = "Sharon";
	string finType = "Mystery Mom";
	string finKid = "Void Child";

	//Output text
	cout << "Knock, knock! It's your new neighbor, "<< SHARON << ", head of the local PTA,\nneighborhood watch, salvation army, and Scientology branch!" << endl;
	cout << "And I brought quinoa!\n" << endl;
	cout << "Welcome to the neighborhood! It's so nice to have a nice new mom and her family\njoin our quiet suburban community." << endl;
	cout << "I'm sure things will go smoothly! As long as you don't cause any trouble for us, that is.\n\n";
	cout << "Oh, silly me! I was so busy talking about myself, I completely forgot to ask your name!";

	while (name == SHARON)
	{
		//Prompt name entry
		cout << "\n(Enter your mom name:) ";
		getline(cin, name);
		system("cls");

		//Ensure name isn't Sharon
		if (name == SHARON)
		{
			cout << SHARON << "? D- did you just say " << SHARON << "?\nThere must be some mistake. My name is " << SHARON << "." << endl;
			cout << "You can't have it.\n\nI'm sure you just misspoke. Yes, that's it.\nNow, I'll ask again. What is your name?";
		}
	}

	cout << "It's wonderful to meet you, " << name << "!" << endl;
	cout << "I'd love to get to know you better! I make it my business to know the business of all the moms on our street." << endl;
	cout << "So, tell me, " << name << ", how would you describe yourself?" << endl;

	//Output type selection menu
	finType = Menu(typeAmt, types);
	system("cls");

	cout << "Hm... You call yourself a " << finType << " too? That's very interesting to hear, " << name << ".\n";
	cout << "Hard to believe that there's another one in the neighborhood now! Just don't try and make this a competition, haha!" << endl;
	cout << "Oh, and don't worry about feeling overshadowed because we're so similar. I'm sure we're actually quite different!\n";
	cout << "For example, my daughter sold a record number of brownies for her school's charity bake sale and beat it the next year!\n" << endl;
	cout << "What's that?\nOh! It's absolutely wonderful to hear that your son won the local science fair!\nYou must be proud to have raised such an intelligent young man.\n";
	cout << "Reminds me of one of mine, Brett!\nHe's going to Yale.\n" << endl;
	cout << "While we're on the topic of kids, I can't help but notice that lovely baby picture on your wall!\nWhat's their name?" << endl;

	//Output child name selection menu
	finKid = Menu(kidsAmt, kids);
	system("cls");

	cout << finKid << "? What a... unique name for a child!" << endl;

	cout << "Anyways, I assume you have at least a couple more kids around the house to keep you busy while your husband is away.\n";
	cout << "I just mean since he leaves late at night so often and all. You might want to keep an eye out, " << name << "," << endl;
	cout << "those night shifts can really do a number on a relationship!\n" << endl;

	cout << "Anyways, " << name << ", I've just got to know. What do you do for fun?\n";
	cout << "Here, let's compare hobbies! Here's a list I prepared.\n" << endl;

	//stat input instructions
	cout << "(You have a total of " << points << " skill points to allocate between " << statAmt << " different white suburban mom behaviours.\n";
	cout << "Be careful not to go overboard! If you use more than " << points << " points, " << SHARON << " will realize you're lying.)\n" << endl;
	Clear();

	while (points > 0)
	{
		quinoaLoop++;
		Quinoa(quinoaLoop);
		cout << "\n\nAnyways, see anything you find interesting?\n" << endl;

		//Output stat selection menu
		cout << "(Select a number)";
		for (int statLoop = 0; statLoop < statAmt; statLoop++)
		{
			cout << "\n(" << statLoop << ") " << statNames[statLoop] << ", (Currently at " << stats[statLoop] << " points)";
		}

		//Prompt stat selection
		cout << "\n(Enter your selection:) ";
		select = Check(0, (statAmt - 1));

		cout << "\nOh, you love " << statNames[select] << " too? We seem to have so much in common, it's wonderful.\nOut of curiosity, how good at it are you?\n";
		cout << "\n(" << points << " points remaining.)";
		cout << "\n(Enter your selection:) ";
		num = Check(0, points);
		points = points - num;
		stats[select] = stats[select] + num;

		cout << num << ", of course.\nHaha, you're just full of fun little surprises, aren't you, " << name << "?\n" << endl;

		Clear();
	}

	system("cls");

	cout << "Wow, you sure seem to have a lot of free time!\nI wonder how your husband feels about you doing all this? You'd better be careful!\n";
	cout << "Especially considering how hard it is these days to find a good man once you reach a certain age.\n" << endl;
	cout << "You're only 30, you say?\nOh, I hope you didn't think I was implying something! Because, trust me, " << name << "." << endl;
	cout << "None of what I said was implied.\n" << endl;

	Clear();

	cout << "No, nothing's wrong! I don't know where you got that idea from. Why would anything be wrong?\n" << endl;
	cout << "All that's happened is another " << finType << " moved into my neighborhood!\n";
	cout << "She's named " << name << " with a kid called " << finKid << ". Not that I care enough to remember any of that!" << endl;
	cout << "And there's nothing wrong with the fact that she said she has ";

	//Display final stats
	for (int statLoop = 0; statLoop < statAmt; statLoop++)
	{
		cout << "a score of " << stats[statLoop] << " in " << statNames[statLoop] << "!\nAnd ";
	}

	cout << "there's absolutely nothing wrong with the fact that all those scores are higher than mine!\n" << endl;
	cout << "It's even okay that she's got me beat in every way and that I've been dethroned as the superior white suburban mom!\n";
	cout << "It's okay because none of it will matter soon!\n" << endl;

	system("pause");
	system("cls");

	cout << "Oh, I see. You have to take your kid to soccer practice and you want me to leave?\nOf course! I'm sorry for keeping you so long.\n";
	cout << "It was lovely to meet you, " << name << "! ";
	cout << "I'd say we should do this again sometime, but I poisoned the quinoa.\n";
	cout << "Tell little " << finKid << " that their new neighbor wishes them good luck at soccer practice!\n" << endl;

	return 0;
}

int GetInteger()
{
	int value = 0;
	while (!(cin >> value))
	{
		cin.clear();
		cin.ignore(numeric_limits<streamsize>::max(), '\n');
	}
	return value;
}

int Check(int min, int max)
{
	bool solid = false;
	int input = GetInteger();

	while (solid == false)
	{
		if (input < min || input > max)
		{
			cout << "\n(The answer you gave, " << input << ", is beyond " << SHARON << "'s understanding." << endl;
			cout << "She only comprehends spite and concepts that correlate with numbers between " << min << " and " << max << ". Try again.)\n";
			input = GetInteger();
		}
		else
		{
			solid = true;
		}
	}

	return input;
}

string Menu(int numArray, string array[])
{
	cout << "\n(Select a number)";
	for (int i = 0; i < numArray; i++)
	{
		cout << "\n(" << i << ") " << array[i];
	}

	//Prompt child name selection
	cout << "\n(Enter your selection:) ";
	return array[Check(0, (numArray - 1))];
}

void Quinoa(int loopNum)
{
	if (loopNum < 3)
	{
		cout << "Here, have a bite of my quinoa. I brought it just for you!";
	}
	else if (loopNum == 5)
	{
		cout << "Isn't the quinoa amazing? I got it from the farmer's market at\nBeth's stall, so you know it's locally grown and organic!";
	}
	else if (loopNum == 6)
	{
		cout << "Did I get the quinoa from the farmer's market for the environment?" << endl;
		cout << "No, of course not silly, global warming isn't real!";
	}
	else if (loopNum < 8)
	{
		cout << "Here, have another bite of quinoa. It's all for you!";
	}
	else if (loopNum < 11)
	{
		cout << "Don't you think that's enough quinoa for now? You do have to watch your figure, after all!";
	}
	else if (loopNum == 12)
	{
		cout << "(" << SHARON << " takes out her cell phone and wanders away.)\nYes, you heard me right, Harold! She's literally eating the bowl!\n";
		cout << "Of course I'd like a ride, she almost took my hand off when she grabbed the darn thing!" << endl;
		cout << "(" << SHARON << " turns back to you nervously.)";
	}
	else if (loopNum == 13)
	{
		cout << "(" << SHARON << " smiles widely at you and points at her phone in a 'they just keep talking' gesture.)\nYou're on your way, right Harold?\n";
		cout << "Okay, thank the Lord. I should be done soon. Come quick!";
		cout << "(" << SHARON << " turns back to you, shaking.)";
	}
	else if (loopNum == 14)
	{
		cout << "(" << SHARON << " puts the phone away and approaches you, smile wide and fearful.)\nDon't you think that's enough... quinoa?\n";
	}
	else if (loopNum >= 15)
	{
		cout << "Don't you think that's enough... quinoa?\n";
	}
}

void Clear()
{
	system("pause");
	system("cls");
}
