# Dhont
using System;
using System.Linq;
namespace ConsoleApp1
{
    class Program
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

            int brexit_meps = 1;
            int liberal_democrats_meps = 1;
            int labour_meps = 1;
            int conservative_meps = 1;
            int green_party_meps = 1;
            int ukip_meps = 1;
            int change_uk_meps = 1;
            int independent_network_meps = 1;
            int independent_meps = 1;

         

            string first_win =
                new[] {
                    Tuple.Create(brexit_votes, "Brexit"),
                    Tuple.Create(liberal_democrats_votes, "The liberal democrats"),
                    Tuple.Create(labour_votes, "Labour"),
                    Tuple.Create(conservative_votes, "conservative"),
                    Tuple.Create(green_party_votes, "the green party"),
                    Tuple.Create(ukip_votes, "UKIP"),
                    Tuple.Create(change_uk_votes, "change UK"),
                    Tuple.Create(independent_network_votes, "the independent network"),
                    Tuple.Create(independent_votes, "an indpendent candidate")
                }.Max()
                .Item2;
            

            Console.WriteLine(("The party with the most initial votes is:") + first_win);
            Console.ReadLine();
