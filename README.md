# c-program-to-find-unique-element-in-the-given-range
#include <stdio.h>

int main ()
{
  long long int n, low, high, a[100] = { 0 }, k, i, j, ctr = 0, flag = 0;
  scanf ("%lld %lld", &low, &high);
  while (low < high)
    {
      n = low;
      flag = 0;
      k = 0;
      ctr = 0;
      while (n != 0)
	{
	  a[k++] = n % 10;
	  n /= 10;
	  ctr++;
	}
      for (i = 0; i < ctr; i++)
	{
	  for (j = i + 1; j < ctr; j++)
	    {
	      if (a[i] == a[j])
		flag++;
	    }
	}
      if (flag == 0)
	printf ("%lld ", low);
      low++;

    }
}
