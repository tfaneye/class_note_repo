# class_note_repo
This will be for holding class materials

public class Program
    {
        public static void ATMMachine()
        {
            Console.WriteLine("Welcome!, please insert your card");
            string cardDetails = Console.ReadLine();
            int cardLenght = cardDetails.Length;
            if (cardLenght != 16)
            {
                Console.WriteLine("You have inserted a wrong card, please remove your card");
                Console.ReadLine();
            }
            else
            {
                Console.WriteLine("Please enter the amount you want to withdraw");
                string amount = Console.ReadLine();
                double withdrawalAmount = Convert.ToDouble(amount);
                Console.WriteLine("Thank you, you have withdrawn £" + amount + " from your account, please take your money, goodbye");
                Console.ReadLine();
            }
        }

        enum DrinkTypes
        {
            CoffeeWhite = 1,
            CoffeeBlack = 2,
            TeaHerbal = 3,
            TeaNormal = 4,
            HotChocolate = 5,
            Orange = 6,
            AppleJuice = 7,
            MangoJuice = 8,

        }

        public static void NewVendMachine()
        {
            Console.WriteLine("Please check our menu and the number corresponding to your order");
            string drink = Console.ReadLine();
            //int drink = Convert.ToInt32(myDrinkChoice);
            if(drink.Equals("1"))
            {
                drink = DrinkTypes.CoffeeWhite.ToString();
                Console.WriteLine("Kindly wait while we prepare your Coffee please...");
                Console.ReadLine();
                Console.WriteLine("Here is your White coffee with 2 sugar please");
                Console.ReadLine();
            }
            else if (drink.Equals("2"))
            {
                drink = DrinkTypes.CoffeeBlack.ToString();
                Console.WriteLine("Kindly wait black we prepare your Coffee please...");
                Console.ReadLine();
                Console.WriteLine("Here is your Black coffee with 2 sugar please");
                Console.ReadLine();
            }
            else if (drink.Equals("3"))
            {
                drink = DrinkTypes.TeaHerbal.ToString();
                Console.WriteLine("Kindly wait while we prepare your Tea please...");
                Console.ReadLine();
                Console.WriteLine("Here is your Herbal Tea with 2 sugar please");
                Console.ReadLine();
            }

        }


        public static void VendMachine()
        {
            Console.WriteLine("What drink would you like please");
            string myDrinkChoice = Console.ReadLine();

            if (myDrinkChoice.Equals("Coffee") || myDrinkChoice.Equals("coffee"))
            {
                Console.WriteLine("White or Black please");
                string myCoffeChoice = Console.ReadLine();
                if (myCoffeChoice.Equals("White") || myCoffeChoice.Equals("white"))
                {
                    Console.WriteLine("Kindly wait while we prepare your Coffee please...");
                    Console.ReadLine();
                    Console.WriteLine("Here is your White coffee with 2 sugar please");
                    Console.ReadLine();

                }
                else if (myCoffeChoice.Equals("Black") || myCoffeChoice.Equals("black"))
                {
                    Console.WriteLine("Kindly wait while we prepare your Coffee please...");
                    Console.ReadLine();
                    Console.WriteLine("Here is your Black coffee with 2 sugar please");
                    Console.ReadLine();
                }
                else
                {
                    Console.WriteLine("Sorry we only server either white or black coffee");
                }
            }
            else if (myDrinkChoice.Equals("Tea") || myDrinkChoice.Equals("tea"))
            {
                Console.WriteLine("Herbal or Normal please");
                string myCoffeChoice = Console.ReadLine();
                if (myCoffeChoice.Equals("Herbal") || myCoffeChoice.Equals("herbal"))
                {
                    Console.WriteLine("Kindly wait while we prepare your Tea please...");
                    Console.ReadLine();
                    Console.WriteLine("Here is your Herbal Tea with 2 sugar please");
                    Console.ReadLine();
                }
                else if (myCoffeChoice.Equals("Normal") || myCoffeChoice.Equals("normal"))
                {
                    Console.WriteLine("Do you want milk please?, Type Yes or No");
                    string myMilkChoice = Console.ReadLine();
                    if (myMilkChoice.Equals("Yes") || myMilkChoice.Equals("yes"))
                    {
                        Console.WriteLine("Kindly wait while we prepare your Tea please...");
                        Console.ReadLine();
                        Console.WriteLine("Here is your Normal Tea with milk and 2 sugar please");
                        Console.ReadLine();
                    }
                    else if(myMilkChoice.Equals("No") || myMilkChoice.Equals("no"))
                    {
                        Console.WriteLine("Kindly wait while we prepare your Tea please...");
                        Console.ReadLine();
                        Console.WriteLine("Here is your Normal Tea without milk but with 2 sugar please");
                        Console.ReadLine();
                    }
                    else
                    {
                        Console.WriteLine("Sorry it is either you add suggar or not...");
                    }
                }
                else
                {
                    Console.WriteLine("Sorry we only server either herbal or normal tea");
                }
            }
            else
            {
                Console.WriteLine("\nSorry we do not serve such drink here!!" + "\nThank you bye bye");
                Console.ReadLine();
            }
        }


        public static void Main(string[] args)
        {

           // NewVendMachine();

           // ATMMachine();

            Console.WriteLine("\n===============================================================");

            Console.WriteLine("Enter you sales amount");
            string mySalesAmount = Console.ReadLine();
            double sale = Double.Parse(mySalesAmount);

            //double sale = Convert.ToDouble(mySalesAmount);

            //double sale = 2700;
            if (sale < 100)
            {
                double salesComm = 0.025 * sale;
                Console.WriteLine("Thank you for your contribution, £" + salesComm + " has been paid into your account as commission for your sales of " + sale);
                //Console.WriteLine("You have earned commission of = " + salesComm);
                Console.WriteLine("\t" + (char)0x263A);
                double actualSales = sale - salesComm;
                Console.WriteLine("Your actual sales now = " + actualSales);
                Console.ReadLine();
            }
            else if (sale >= 100 && sale <= 500)
            {
                double salesComm = 0.08 * sale;
                Console.WriteLine("Thank you for your contribution, £" + salesComm + " has been paid into your account as commission for your sales of " + sale);
                //Console.WriteLine("You have earned commission of = " + salesComm);
                Console.WriteLine("\t" + (char)0x263A);
                double actualSales = sale - salesComm;
                Console.WriteLine("Your actual sales now = " + actualSales);
                Console.ReadLine();
            }
            else if (sale >= 501 && sale <= 1000)
            {
                double salesComm = 0.125 * sale;
                Console.WriteLine("Thank you for your contribution, £" + salesComm + " has been paid into your account as commission for your sales of " + sale);
                //Console.WriteLine("You have earned commission of = " + salesComm);
                Console.WriteLine("\t" + (char)0x263A);
                double actualSales = sale - salesComm;
                Console.WriteLine("Your actual sales now = " + actualSales);
                Console.ReadLine();
            }
            else if (sale >= 1001 && sale <= 5000)
            {
                double salesComm = 0.175 * sale;
                Console.WriteLine("Thank you for your contribution, £" + salesComm + " has been paid into your account as commission for your sales of " + sale);
                //Console.WriteLine("You have earned commission of = " + salesComm);
                Console.WriteLine("\t" + (char)0x263A);
                double actualSales = sale - salesComm;
                Console.WriteLine("Your actual sales now = " + actualSales);
                Console.ReadLine();
            }
            else if (sale >= 5001)
            {
                double salesComm = 0.23 * sale;
                Console.WriteLine("Thank you for your contribution, £" + salesComm + " has been paid into your account as commission for your sales of " + sale);
                //Console.WriteLine("You have earned commission of = " + salesComm);
                Console.WriteLine("\t" + (char)0x263A);
                double actualSales = sale - salesComm;
                Console.WriteLine("Your actual sales now = " + actualSales);
                Console.ReadLine();
            }

            Console.WriteLine("\n===============================================================");

            if (sale >= 1000)
            {
                VendMachine();
            }
            else
            {
                Console.WriteLine("Thanks for your contribution, but you do not deserve a drink");
                Console.ReadLine();
            }            
        }
    }
