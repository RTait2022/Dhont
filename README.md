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
int Liberal_Democrats_votes = Convert.ToInt32(Console.ReadLine());

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
int cange_uk_meps = 1;
int independent_network_meps = 1;
int independent_meps = 1;

int[] numbers = { brexit_votes, Liberal_Democrats_votes, labour_votes, conservative_votes, green_party_votes, ukip_votes, change_uk_votes, independent_network_votes, independent_votes };
int biggestNumber = numbers.Max();

Console.WriteLine(("The party with the most initial votes is:") + biggestNumber);
Console.ReadLine();
