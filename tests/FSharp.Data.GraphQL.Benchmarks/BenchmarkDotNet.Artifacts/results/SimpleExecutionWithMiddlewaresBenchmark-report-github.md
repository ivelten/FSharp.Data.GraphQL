``` ini

BenchmarkDotNet=v0.10.9, OS=Windows 10.0.17134
Processor=Intel Core i7-2600 CPU 3.40GHz (Sandy Bridge), ProcessorCount=8
.NET Core SDK=2.1.300
  [Host] : .NET Core 2.0.7 (Framework 4.6.26328.01), 64bit RyuJIT DEBUG
  Core   : .NET Core 2.0.7 (Framework 4.6.26328.01), 64bit RyuJIT
  Mono   : Mono 5.12.0 (Visual Studio), 32bit 


```
 |                         Method |  Job | Runtime |      Mean |      Error |     StdDev |    Median |       Min |       Max |     Op/s |
 |------------------------------- |----- |-------- |----------:|-----------:|-----------:|----------:|----------:|----------:|---------:|
 |   BenchmarkSimpleQueryUnparsed | Core |    Core |  76.91 us |  1.5138 us |  1.3419 us |  76.95 us |  74.67 us |  79.02 us | 13,001.5 |
 |     BenchmarkSimpleQueryParsed | Core |    Core |  37.39 us |  0.8233 us |  2.2814 us |  36.49 us |  34.87 us |  43.51 us | 26,745.7 |
 |    BenchmarkSimpleQueryPlanned | Core |    Core |  28.11 us |  0.4333 us |  0.4053 us |  28.02 us |  27.61 us |  28.91 us | 35,570.8 |
 |     BenchmarkFlatQueryUnparsed | Core |    Core | 764.11 us | 15.9194 us | 26.5978 us | 756.36 us | 735.18 us | 839.11 us |  1,308.7 |
 |       BenchmarkFlatQueryParsed | Core |    Core | 685.61 us | 10.3700 us |  9.1927 us | 686.29 us | 668.02 us | 696.84 us |  1,458.6 |
 |      BenchmarkFlatQueryPlanned | Core |    Core | 671.41 us | 10.0553 us |  9.4057 us | 670.22 us | 655.71 us | 689.20 us |  1,489.4 |
 |   BenchmarkNestedQueryUnparsed | Core |    Core | 592.24 us | 11.7265 us | 29.6343 us | 590.17 us | 546.45 us | 669.00 us |  1,688.5 |
 |     BenchmarkNestedQueryParsed | Core |    Core | 404.04 us |  8.0123 us | 10.4183 us | 404.74 us | 388.58 us | 423.70 us |  2,475.0 |
 |    BenchmarkNestedQueryPlanned | Core |    Core | 396.58 us |  8.2996 us | 15.3839 us | 395.66 us | 375.44 us | 438.12 us |  2,521.6 |
 | BenchmarkFilteredQueryUnparsed | Core |    Core | 202.05 us |  3.8502 us |  4.5834 us | 202.54 us | 196.13 us | 211.55 us |  4,949.3 |
 |   BenchmarkFilteredQueryParsed | Core |    Core | 103.52 us |  1.2202 us |  1.0189 us | 103.64 us | 101.87 us | 105.34 us |  9,659.9 |
 |  BenchmarkFilteredQueryPlanned | Core |    Core |  91.31 us |  1.7846 us |  2.3824 us |  90.62 us |  88.50 us |  96.52 us | 10,951.3 |
 |   BenchmarkSimpleQueryUnparsed | Mono |    Mono |  79.20 us |  0.8202 us |  0.7271 us |  79.02 us |  77.95 us |  80.75 us | 12,626.3 |
 |     BenchmarkSimpleQueryParsed | Mono |    Mono |  46.62 us |  0.9292 us |  1.0701 us |  46.29 us |  44.66 us |  48.23 us | 21,448.3 |
 |    BenchmarkSimpleQueryPlanned | Mono |    Mono |  43.24 us |  0.8615 us |  2.4016 us |  42.98 us |  39.63 us |  50.42 us | 23,127.5 |
 |     BenchmarkFlatQueryUnparsed | Mono |    Mono | 922.57 us | 17.3296 us | 17.7962 us | 920.40 us | 887.15 us | 955.28 us |  1,083.9 |
 |       BenchmarkFlatQueryParsed | Mono |    Mono | 834.60 us | 16.3285 us | 16.0367 us | 838.73 us | 806.02 us | 861.76 us |  1,198.2 |
 |      BenchmarkFlatQueryPlanned | Mono |    Mono | 875.53 us | 17.3852 us | 50.9877 us | 869.95 us | 804.07 us | 998.14 us |  1,142.2 |
 |   BenchmarkNestedQueryUnparsed | Mono |    Mono | 817.81 us | 16.2626 us | 46.3981 us | 816.63 us | 745.58 us | 941.76 us |  1,222.8 |
 |     BenchmarkNestedQueryParsed | Mono |    Mono | 654.67 us | 12.9669 us | 24.0351 us | 647.89 us | 620.11 us | 709.60 us |  1,527.5 |
 |    BenchmarkNestedQueryPlanned | Mono |    Mono | 601.30 us |  8.3861 us |  7.4341 us | 600.63 us | 586.85 us | 617.86 us |  1,663.1 |
 | BenchmarkFilteredQueryUnparsed | Mono |    Mono | 225.72 us |  3.0642 us |  2.8663 us | 225.41 us | 220.51 us | 231.26 us |  4,430.2 |
 |   BenchmarkFilteredQueryParsed | Mono |    Mono | 150.79 us |  2.1233 us |  1.9861 us | 150.75 us | 147.45 us | 154.70 us |  6,631.6 |
 |  BenchmarkFilteredQueryPlanned | Mono |    Mono | 143.83 us |  2.7346 us |  2.6858 us | 143.71 us | 139.66 us | 150.62 us |  6,952.6 |
