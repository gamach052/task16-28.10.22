###  [Task 7kyu](https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/java)

In a small town the population is p0 = 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new inhabitants per year come to live in the town. How many years does the town need to see its population greater or equal to p = 1200 inhabitants?



### My solution
```Java
class Arge {

    public static int nbYear(int p0, double percent, int aug, int p)
    {
        percent*=0.01;
        int years=0;
        while(p0<p)
        {
            years++;
            p0+=p0*percent+aug;
        }
        return years;
    }
}
```

### Fav solution
```Java
class Arge {

    public static int nbYear(int p0, double percent, int aug, int p) {
        if (p0>=p) return 0;
        else return nbYear((int) (p0+aug+p0*(percent/100)), percent, aug, p) + 1;
    }
}

```
I like this solution because I like it
