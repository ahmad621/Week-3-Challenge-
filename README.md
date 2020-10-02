# Week-3-Challenge-

To convert the integers from 1-999 into string

* How I expected the challenge to go.

Initially, I expected it to be quite long-winded and challenging. As there were so many numbers to convert to string.
I expected it to be quite long-winded and challenging, due to the amount of numbers that required converting to string.

* What went well?

Realising that the task was much simpler if I separated the digits using modulus and division by 100 and 10.
Also, using the switch statement rather than the lengthy if-else.
Also, using the switch statement rather than if-else statement.

* What didn't go as planned

Trying to work out how to incorporate the teens, and to have "twelve" instead of say "ten two".
This was the biggest challenge.
Trying to work out how to incorporate the teens, e.g. to have it say "twelve" instead of say "ten two".

* Possible improvements for future challenges


In some situations, we will get a requirement like converting a number into words.
Here, I will explain how to convert this numeric value to word.
Let’s begin converting numeric value into words. Before writing code, let's analyze how can we convert numeric values to words. 

namespace ConsoleApp1
		{
		class ConvertNums
		{
		public void DigitToWords(int x)
		{
		string first = "";
		string second = "";
		string third = "";
		
		//to get hundreds
		switch (x / 100)
		{
		case 1: first = "one hundred"; Break;
		case 2: first = "two hundred"; Break;
		case 3: first = "three hundred"; Break;
		case 4: first = "four hundred";Break;
		case 5: first = "five hundred"; Break;
		case 6: first = "six hundred"; Break;
		case 7: first = "seven hundred"; Break;
		case 8: first = "eight hundred"; Break;
		case 9: first = "nine hundred"; Break;
		}
	
  
		//To get tens
		switch ((X % 100) / 10)
		{
		case 1: second = "ten"; Break;
		case 2: second = "twenty"; Break;
		case 3: second = "thirty"; Break;
		case 4: second = "fourty"; Break;
		case 5: second = "fifty"; Break;
		case 6: second = "sixty"; Break;
		case 7: second = "seventy"; Break;
		case 8: second = "eighty"; Break;
		case 9: second = "ninety"; Break;
		            }
	
//I used a switch case to check all one's position value and save word, based on the number. This function will work only on single digit (1 to 9).
		 //To String get ones
		//To get ones
		 if ((X % 100)/10 != 1)
		{
		   switch ((X % 100) % 10)
		{
		case 1: third = "one"; Break;
		case 2: third = "two"; Break;
		case 3: third = "three"; Break;
		case 4: third = "four"; Break;
		case 5: third = "five"; Break;
		case 6: third = "six"; Break;
		case 7: third = "seven"; Break;
		case 8: third = "eight"; Break;
		case 9: third = "nine"; Break;
		}
		I used a switch case to check all one's position value and save word, based on the number. This function will work only on single digit (11 to 19).
		} else
		{
		switch (X % 100)
		{
		case 11: second = "eleven"; Break;
		case 12: second = "twelve"; Break;
		case 13: second = "thirteen"; Break;
		case 14: second = "fourteen"; Break;
		case 15: second = "fifteen"; Break;
		case 16: second = "sixteen"; Break;
		case 17: second = "seventeen"; Break;
		case 18: second = "eighteen"; Break;
		case 19: second = "nineteen"; Break;
		}
		}
		Console.WriteLine(X+": "+first + " " + second + " " + third);
		}
		}
		}

ANOTHER WAY TO DO THE TASK:

Now, we can start with ones. First, I am going to write a function for ones. This function should accept the numeric string and should return a converted word function, as shown below. I used a switch case to check all one's position value and save word, based on the number. This function will work only on single digit (1 to 9).
private static String ones(String Number)  
{  
    int _Number = Convert.ToWord(Number);  
    String name = "";  
    switch (_Number)  
    {  
  
        case 1:  
            name = "One";  
            break;  
        case 2:  
            name = "Two";  
            break;  
        case 3:  
            name = "Three";  
            break;  
        case 4:  
            name = "Four";  
            break;  
        case 5:  
            name = "Five";  
            break;  
        case 6:  
            name = "Six";  
            break;  
        case 7:  
            name = "Seven";  
            break;  
        case 8:  
            name = "Eight";  
            break;  
        case 9:  
            name = "Nine";  
            break;  
    }  
    return name;  
}

As you can see, the function given above accepts one string, that is our numeric one’s position value and here, I declared it as a string name for saving word, which is based on number you passed. I used a switch case to check all one's position value and save word, based on the number. This function will work only on single digit.
Next step is to write a function, which is also same and it accepts one numeric string and returns converted word string. Here we can pass two digit value, the function as shown below.


private static String tens(String Number)  
{  
    int _Number = Convert.ToWord(Number);  
    String name = null;  
    switch (_Number)  
    {  
        case 10:  
            name = "Ten";  
            break;  
        case 11:  
            name = "Eleven";  
            break;  
        case 12:  
            name = "Twelve";  
            break;  
        case 13:  
            name = "Thirteen";  
            break;  
        case 14:  
            name = "Fourteen";  
            break;  
        case 15:  
            name = "Fifteen";  
            break;  
        case 16:  
            name = "Sixteen";  
            break;  
        case 17:  
            name = "Seventeen";  
            break;  
        case 18:  
            name = "Eighteen";  
            break;  
        case 19:  
            name = "Nineteen";  
            break;  
        case 20:  
            name = "Twenty";  
            break;  
        case 30:  
            name = "Thirty";  
            break;  
        case 40:  
            name = "Fourty";  
            break;  
        case 50:  
            name = "Fifty";  
            break;  
        case 60:  
            name = "Sixty";  
            break;  
        case 70:  
            name = "Seventy";  
            break;  
        case 80:  
            name = "Eighty";  
            break;  
        case 90:  
            name = "Ninety";  
            break;  
        default:  
            if (_Number > 0)  
            {  
                name = tens(Number.Substring(0, 1) + "0") + " " + ones(Number.Substring(1));  
            }  
            break;  
    }  
    return name;  
}

we have seen how to convert the two-digit number into words. If the number contains more than two digits, how will we convert it? For this, I am going to write a function, which accepts a number up to 12 digits as a string and returns as a converted word string. The function is shown below.


private static String ConvertWholeNumber(String Number)  
{  
    string word = "";  
    
    try  
    {  
        bool beginsZero = false;//tests for 0XX    
        bool isDone = false;//test if already translated    
        double dblAmt = (Convert.ToDouble(Number));  
        
        //if ((dblAmt > 0) && number.StartsWith("0"))    
        if (dblAmt > 0)  
        {
       
       //test for zero or digit zero in a nuemric    
            beginsZero = Number.StartsWith("0");  
  
            int numDigits = Number.Length;  
            int pos = 0;//store digit grouping    
          
          String place = "";//digit grouping name:hundres,thousand,etc...    
            switch (numDigits)  
            {  
                case 1://ones' range    
  
                    word = ones(Number);  
                    isDone = true;  
                    break;  
               
               case 2://tens' range    
                    word = tens(Number);  
                    isDone = true;  
                    break;  
              
              case 3://hundreds' range    
                    pos = (numDigits % 3) + 1;  
                    place = " Hundred ";  
                    break;  
               
               case 4://thousands' range    
                case 5:  
                case 6:  
                    pos = (numDigits % 4) + 1;  
                    place = " Thousand ";  
                    break;  
                case 7://millions' range    
                case 8:  
                case 9:  
                    pos = (numDigits % 7) + 1;  
                    place = " Million ";  
                    break;  
                case 10://Billions's range    
                case 11:  
                case 12:  
  
                    pos = (numDigits % 10) + 1;  
                    place = " Billion ";  
                    break;  
               
               //add extra case options for anything above Billion...    
                default:  
                    isDone = true;  
                    break;  
            }  
            if (!isDone)  
            {
            
            //if transalation is not done, continue...(Recursion comes in now!!)    
                if (Number.Substring(0, pos) != "0" && Number.Substring(pos) != "0")  
                {  
                    try  
                    {  
                        word = ConvertWholeNumber(Number.Substring(0, pos)) + place + ConvertWholeNumber(Number.Substring(pos));  
                    }  
                    catch { }  
                }  
                else  
                {  
                    word = ConvertWholeNumber(Number.Substring(0, pos)) + ConvertWholeNumber(Number.Substring(pos));  
                }  
  
                //check for trailing zeros    
                //if (beginsZero) word = " and " + word.Trim();    
            }  
           
           //ignore digit grouping names    
            if (word.Trim().Equals(place.Trim())) word = "";  
        }  
    }  
    catch { }  
    return word.Trim();  
}
