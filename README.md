# assignment2-Mohammad
# Sajida Mohammad
#### Gokul Chat

Gokul Chat is located in Koti in the city Hyderabad. Koti is famous for street **shopping** and has attractive wares, handicrafts, clothing, footware and accessories.
Gokul Chat is **famous for tasty street food** like various chats, **pani puri and dahi puri with affordable prices**
***
## Heading for the list
1. Maryville
2. Kansas 
    1. Kansas Airport
    3. Aeroplane
3. India
4. Hyderabad
5. Cab
6. Public transporation

* Pav bhaji
* Samosa
* Paani puri
* Kachori
* Masala Puri



[About Me](AboutMe.md)
***
### Heading for the sports/activities
This table is regarding the sports/activities and the location where one can participated. It also includes the cost required for any personal equipment.

| **Sports Name**| **location**| **cost**|
| --- | --- | --- |
| Cricket | India | 10-15 |
| Basket Ball | United States | 33-38|
| Hockey | Australia | 6- 13|
| FootBall | Newzealand | 5-10|

***
### Favourite Quotes ###

> "The greatest glory in living lies not in never falling, but in rising every time we fall." Author: *Nelson Mandela*

> "Keep your face always toward the sunshine, and shadows will fall behind you." Author: *Walt Whitman*

***
### Section for code fencing 

> Fast String Hashing Algorithm with low collision rates with 32 bit integer
Quick link to the source

 [source code](https://stackoverflow.com/questions/114085/fast-string-hashing-algorithm-with-low-collision-rates-with-3er2-bit-integer)

```
#include <stdint.h>

uint32_t hash_string(const char * s)
{
    uint32_t hash = 0;

    for(; *s; ++s)
    {
        hash += *s;
        hash += (hash << 10);
        hash ^= (hash >> 6);
    }

    hash += (hash << 3);
    hash ^= (hash >> 11);
    hash += (hash << 15);

    return hash;
}
```

 [source code](https://stackoverflow.com/questions/114085/fast-string-hashing-algorithm-with-low-collision-rates-with-3er2-bit-integer)