using System;
using System.Linq;
namespace ConsoleApp1
{
    public class Input_variables
    {
        static void Main(string[] args)
        {

            Console.WriteLine("Please enter the amount of votes the brexit party got:");
            int brexit_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the Liberal Democrats got:");
            int liberal_democrats_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the Labour party got:");
            int labour_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the Conservative party got:");
            int conservative_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the Green party got:");
            int green_party_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes that UKIP got:");
            int ukip_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the change UK party got:");
            int change_uk_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes the Independent Network got:");
            int independent_network_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of votes that independent candidates got:");
            int independent_votes = Convert.ToInt32(Console.ReadLine());

            Console.WriteLine("Please enter the amount of meps seats are avalible:");
            int round = Convert.ToInt32(Console.ReadLine());
        }
        public class Calc_variables {

            public int brexit_meps = 1;
            public int liberal_democrats_meps = 1;
            public int labour_meps = 1;
            public int conservative_meps = 1;
            public int green_party_meps = 1;
            public int ukip_meps = 1;
            public int change_uk_meps = 1;
            public int independent_network_meps = 1;
            public int independent_meps = 1;

            public int brexit_votes_store = brexit_votes;
            public int liberal_democrats_votes_store = liberal_democrats_votes;
            public int labour_votes_store = labour_votes;
            public int conservative_votes_store = conservative_votes;
            public int green_party_votes_store = green_party_votes;
            public int ukip_votes_store = ukip_votes;
            public int change_uk_votes_store = conservative_votes;
            public int independent_network_votes_store = independent_network_votes;
            public int independent_votes_store = independent_votes;
        }

        }
    



    public class Biggest_calc
    {


        static void Main(string[] args)
        {

            for (;;)
                {

                if (round > 0)
                {
                     string win =
                        new[] {
                                Tuple.Create(brexit_votes, "Brexit"),
                                Tuple.Create(liberal_democrats_votes, "The liberal democrats"),
                                Tuple.Create(labour_votes, "Labour"),
                                Tuple.Create(conservative_votes, "conservative"),
                                Tuple.Create(green_party_votes, "the green party"),
                                Tuple.Create(ukip_votes, "UKIP"),
                                Tuple.Create(change_uk_votes, "change UK"),
                                Tuple.Create(independent_network_votes, "the independent network"),
                                Tuple.Create(independent_votes, "indpendent")
                        }.Max()
                        .Item2;
                        


                        Console.WriteLine(("The party with the most votes is:") + win);
                        Console.WriteLine("Please press enter to continue:");
                        Console.ReadLine();

                        if (win == "Brexit")
                        {
                            brexit_votes = brexit_votes_store;
                            brexit_meps = (brexit_meps + 1);
                            brexit_votes = (brexit_votes / brexit_meps);


                        }

                        else if (win == "The liberal democrats")
                        {
                            liberal_democrats_votes = liberal_democrats_votes_store;
                            liberal_democrats_meps = (liberal_democrats_meps + 1);
                            liberal_democrats_votes = (liberal_democrats_votes / liberal_democrats_meps);

                        }

                        else if (win == "Labour")
                        {
                            labour_votes = labour_votes_store;
                            labour_meps = (labour_meps + 1);
                            labour_votes = (labour_votes / labour_meps);

                        }

                        else if (win == "conservative")
                        {
                            conservative_votes = conservative_votes_store;
                            conservative_meps = (conservative_meps + 1);
                            conservative_votes = (conservative_votes / conservative_meps);
                        }

                        else if (win == "the green party")
                        {
                            green_party_votes = green_party_votes_store;
                            green_party_meps = (green_party_meps + 1);
                            green_party_votes = (green_party_votes / green_party_meps);
                        }

                        else if (win == "UKIP")
                        {
                            ukip_votes = ukip_votes_store;
                            ukip_meps = (ukip_meps + 1);
                            ukip_votes = (ukip_votes / ukip_meps);
                        }

                        else if (win == "change UK")
                        {
                            change_uk_votes = change_uk_votes_store;
                            change_uk_meps = (change_uk_meps + 1);
                            change_uk_votes = (change_uk_votes / change_uk_meps);
                        }

                        else if (win == "the independent network")
                        {
                            independent_network_votes = independent_network_votes_store;
                            independent_network_meps = (independent_network_meps + 1);
                            independent_network_votes = (independent_network_votes / independent_network_meps);
                        }

                        else if (win == "independent")
                        {
                            independent_votes = independent_votes_store;
                            independent_meps = (independent_meps + 1);
                            independent_votes = (independent_votes / independent_meps);
                        }

                        round = (round - 1);
                    }
                    else
                    {
                        brexit_meps = brexit_meps - 1;
                        liberal_democrats_meps = liberal_democrats_meps - 1;
                        labour_meps = labour_meps - 1;
                        conservative_meps = conservative_meps - 1;
                        green_party_meps = green_party_meps - 1;
                        ukip_meps = ukip_meps - 1;
                        change_uk_meps = change_uk_meps - 1;
                        independent_network_meps = independent_network_meps - 1;
                        independent_meps = independent_meps - 1;

                        Console.WriteLine(("The amount of new brexit meps is;") + brexit_meps);
                        Console.WriteLine(("The amount of new liberal democrat meps is;") + liberal_democrats_meps);
                        Console.WriteLine(("The amount of new labour meps is;") + labour_meps);
                        Console.WriteLine(("The amount of new conservative meps is;") + conservative_meps);
                        Console.WriteLine(("The amount of new green party meps is;") + green_party_meps);
                        Console.WriteLine(("The amount of new UKIP meps is;") + ukip_meps);
                        Console.WriteLine(("The amount of new Change UK meps is;") + change_uk_meps);
                        Console.WriteLine(("The amount of new independent network meps is;") + independent_network_meps);
                        Console.WriteLine(("The amount of new independent meps is;") + independent_meps);
                        break;
                    }
                }





            }
        }
}
