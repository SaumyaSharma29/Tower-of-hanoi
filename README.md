# Tower-of-hanoi

#include <stdio.h>
void hanoifun(int n, char fr, char tr, char ar)/      /fr=from rod,tr =to rod, ar=aux rod
{
    if (n == 1)
    {
        printf("\n Move disk 1 from rod %c to rod %c", fr, tr);
        return;
    }
    hanoifun(n-1, fr, ar, tr);
    printf("\n Move disk %d from rod %c to rod %c", n, fr, tr);
    hanoifun(n-1, ar, tr, fr);
}

int main()
{
    int n = 4; // n immplies the number of discs
    hanoifun(n, 'A', 'C', 'B');  
    return 0;
}
