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
| Cricket | Stadium | 10-15 |
| Basket Ball | court | 33-38|
| Hockey | stadium | 6- 13|
| FootBall | court | 5-10|

***
### Favourite Quotes ###

> "The greatest glory in living lies not in never falling, but in rising every time we fall." Author: *Nelson Mandela*

> "Keep your face always toward the sunshine, and shadows will fall behind you." Author: *Walt Whitman*

***
### Section for code fencing 

>  Rabin–Karp algorithm or Karp–Rabin algorithm is a string-searching algorithm created by Richard M. Karp and Michael O. Rabin (1987) that uses hashing to find an exact match of a pattern string in a text. Quick link to the source
<https://en.wikipedia.org/wiki/Rabin%E2%80%93Karp_algorithm>

```
vector<int> rabin_karp(string const& s, string const& t) {
    const int p = 31; 
    const int m = 1e9 + 9;
    int S = s.size(), T = t.size();

    vector<long long> p_pow(max(S, T)); 
    p_pow[0] = 1; 
    for (int i = 1; i < (int)p_pow.size(); i++) 
        p_pow[i] = (p_pow[i-1] * p) % m;

    vector<long long> h(T + 1, 0); 
    for (int i = 0; i < T; i++)
        h[i+1] = (h[i] + (t[i] - 'a' + 1) * p_pow[i]) % m; 
    long long h_s = 0; 
    for (int i = 0; i < S; i++) 
        h_s = (h_s + (s[i] - 'a' + 1) * p_pow[i]) % m; 

    vector<int> occurences;
    for (int i = 0; i + S - 1 < T; i++) { 
        long long cur_h = (h[i+S] + m - h[i]) % m; 
        if (cur_h == h_s * p_pow[i] % m)
            occurences.push_back(i);
    }
    return occurences;
}
```

 <https://cp-algorithms.com/string/rabin-karp.html>