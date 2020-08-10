Final assignment for course Sistemas Inteligentes I, ULPGC Universidad de Las Palmas de Gran Canaria, January 2020.

//TODO:
confirm analyses in statistics
improve implementation

Algoritm description from:
Palomo, Esteban & Domínguez, Enrique. (2013). Hierarchical Color Quantization Based on Self-organization. Journal of Mathematical Imaging and Vision. 49. 1-19. 10.1007/s10851-013-0433-8.
https://www.researchgate.net/publication/236027587_Hierarchical_Color_Quantization_Based_on_Self-organization

Dataset: New York Yellow Taxi Trip Data (provided in the course)

Implementation in TensorFlow using sessions. Works correctly for small sets, does not work on larger sets.

The analyses using self-organising maps were made using Mini-SOM library. When my implementation is improved, it will be possible to compare the behavior of both implementations.
https://github.com/JustGlowing/minisom

#### 1. Typical pickup spots for each hour
Pickup longitude and latitude were used in the training. Time data was only used to show additional dependency. Groups of dots indicate typical pickup spots, eg. airport.

![Typical pickup spots in each hour](./pickup_loc_hours.png)

#### 2. Price vs. payment type
The model was trained on ride distance, payment value and payment type (cash, credit card). The markers indicate payment type and taxi company.

The outcome could show a discrepancy in payment value based on payment type (could be that tax is omitted in cash payments so the effective payment is higher) for both companies, to be evaluated by statistics!!!

x, o - taxi companies

&#x1F34F; - payment type 1

&#x1F49A; - payment type 2

![Price vs. payment type](./price.png)
