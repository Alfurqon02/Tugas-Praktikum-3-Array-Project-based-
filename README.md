# Tugas-Praktikum-3-Array-Project-based-
Oct 4, 2021

Buatlah program menggunakan bahasa C sesuai dengan ketentuan di bawah ini.   
1. Program mencakup varabel bertipe array* 
2. Program mencakup sebuah fungsi buatan sendiri yang menerima argumen bertipe array*


              #include <stdlib.h>
              #include <stdio.h>
              #include <string.h>

              int NIM (void * a, void * b)
              {
                  return strcmp (*(char **) a, *(char **) b);
              }

              void sort(char *arr[], int n)
              {
                  qsort (arr, n, sizeof (const char *), NIM);
              }

              int main ()
              {
                  char *arr[] = {"M0521044", "M0521023", "M0521054", "M0521055", "M0521034", "M0521067"};
                  int n = sizeof(arr)/sizeof(arr[0]);
                  int i;

                  printf("NIM Sebelum Diurut\n");
                  for (i = 0; i < n; i++)
                      printf("%d. %s \n", i+1, arr[i]);

                  sort(arr, n);

                  printf("\NIM Setelah Diurut\n");
                  for (i = 0; i < n; i++)
                      printf("%d. %s \n", i+1, arr[i]);

                  return 0;
              }
