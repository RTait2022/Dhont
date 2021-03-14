using System;
using System.Linq;

namespace ConsoleApp2
{
    public class Program
    {
        public class Mep
        {
            public string Party { get; set; }
            public int Meps { get; set; }
            public Mep(string party, int meps)
            {
                Party = party;
                Meps = meps;
            }


        }
        public class Store
        {
            private string Party { get; set; }
            private int Votes { get; set; }
            private Store(string party, int votes)
            {
                Party = party;
                Votes = votes;
            }
        Store brexit_votes_astore = new Store("brexit votes", 452321);

        }
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

            Mep brexit_eps = new Mep("brexit", 1);
            Mep liberal_democrats_eps = new Mep("liberal democrats", 1);
            Mep labour_eps = new Mep("labour", 1);
            Mep conservative_eps = new Mep("conservative", 1);
            Mep green_party_eps = new Mep("green party", 1);
            Mep ukip_eps = new Mep("ukip", 1);
            Mep change_uk_eps = new Mep("Change uk", 1);
            Mep independent_network_eps = new Mep("Independent network", 1);
            Mep independent_eps = new Mep("Independent", 1);

            int brexit_meps = brexit_eps.Meps;
            int liberal_democrats_meps = liberal_democrats_eps.Meps;
            int labour_meps = labour_eps.Meps;
            int conservative_meps = conservative_eps.Meps;
            int green_party_meps = green_party_eps.Meps;
            int ukip_meps = ukip_eps.Meps;
            int change_uk_meps = change_uk_eps.Meps;
            int independent_network_meps = independent_network_eps.Meps;
            int independent_meps = independent_eps.Meps;

                int brexit_votes_store = brexit_votes;
                int liberal_democrats_votes_store = liberal_democrats_votes;
                int labour_votes_store = labour_votes;
                int conservative_votes_store = conservative_votes;
                int green_party_votes_store = green_party_votes;
                int ukip_votes_store = ukip_votes;
                int change_uk_votes_store = conservative_votes;
                int independent_network_votes_store = independent_network_votes;
                int independent_votes_store = independent_votes;
           


            for (; ; )
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
                    
                    static void RevealResults(int brexit_meps, int liberal_democrats_meps, int labour_meps, int conservative_meps, int green_party_meps, int ukip_meps, int change_uk_meps, int independent_network_meps, int independent_meps)
                    {
                        Console.WriteLine(("The amount of new brexit meps is;") + brexit_meps);
                        Console.WriteLine(("The amount of new liberal democrat meps is;") + liberal_democrats_meps);
                        Console.WriteLine(("The amount of new labour meps is;") + labour_meps);
                        Console.WriteLine(("The amount of new conservative meps is;") + conservative_meps);
                        Console.WriteLine(("The amount of new green party meps is;") + green_party_meps);
                        Console.WriteLine(("The amount of new UKIP meps is;") + ukip_meps);
                        Console.WriteLine(("The amount of new Change UK meps is;") + change_uk_meps);
                        Console.WriteLine(("The amount of new independent network meps is;") + independent_network_meps);
                        Console.WriteLine(("The amount of new independent meps is;") + independent_meps);
                    }
                    RevealResults(brexit_meps, liberal_democrats_meps, labour_meps, conservative_meps, green_party_meps, ukip_meps, change_uk_meps, independent_network_meps, independent_meps);
                    break;
                }
            }





        }
    }
}
