Background:

I started with a simple intuitive algorithm.
Then I implemented a recursive algorithm, which should be ok because I do not see risk of complexity explosion.
Then I tried to do it with Dynamic programming, it was going well but I made the mistake of checking ChatGPT and I found out I was doing similarly to it.
I did not have time to make a new one so I benchamrked the 3 algos and I chose the fastest among those I did without help.
With some time my goal was to approach or improve the results of ChatGPT.


| Method                           | Mean     | Error     | StdDev    |
|--------------------------------- |---------:|----------:|----------:|
| RecursionToBenchmark             | 4.536 ms | 0.2937 ms | 0.8428 ms |
| ConverternNoRecursionToBenchmark | 5.510 ms | 0.1615 ms | 0.4738 ms |
| ConverterChatGPTToBenchmark      | 2.363 ms | 0.0718 ms | 0.2071 ms |

You can see these tests in Benchmark_Runs solution.

!!!
It uses Frozendictionary so it needs .NET 8  .
If you want to use .NET6 too I can modify to use Dictionaries.
If you want to use .NET 9 (Preview) let me know so I can add SearcValues<T> (probably the best solution)

YOu can see the other 2 algorithms I tried in 

How to start.
1.Start the Server side solution: KLA_NumberConverter_ServerSide.sln
wait till you see console instruction similar to these:
info: Microsoft.Hosting.Lifetime[14]
      Now listening on: https://localhost:7018
info: Microsoft.Hosting.Lifetime[14]
      Now listening on: http://localhost:5257
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Development
info: Microsoft.Hosting.Lifetime[0]
      Content root path: C:\Repos\KLA\KLA_CurrencyConverter\

2.Start the desktop client: CurrencyConverterDesktop.sln
insert the number and convert.

Server's side logic is tested with xUnit.

