#include <iostream>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

using namespace std;


int main(int argc, char *argv[]){
    char var1[8] = "-encode";
    char var2[8] = "-decode";
    int rotatorN;
    char bukva;
    rotatorN = atoi(argv[2]);
    if (strcmpi(argv[1], var1) == 0){
        FILE *file1, *file2;
        file1 = fopen(argv[3], "r");
        file2 = fopen(argv[4], "w");
        bukva = getc(file1);
        while (!feof(file1)){
        if (bukva >= 'A' && bukva <= 'Z'){
            bukva = bukva + (rotatorN % 26);
            if (bukva > 'Z'){
                bukva = 'A'+ (bukva-'Z')-1;
            }
            fprintf (file2, "%c", bukva);
        } else if (bukva >= 'a' && bukva <= 'z'){
            bukva = bukva + (rotatorN % 26);
            if (bukva > 'z'){
                bukva = 'a'+ (bukva-'z')-1;
            }
            fprintf (file2, "%c", bukva);
        } else {
            fprintf (file2, "%c", bukva);
            }
        bukva = getc(file1);
        }
        }

    if (strcmpi(argv[1], var2) == 0){
        FILE *file1, *file2;
        file1 = fopen(argv[3], "r");
        file2 = fopen(argv[4], "w");
        bukva = getc(file1);
        while (!feof(file1)){
        if (bukva >= 'A' && bukva <= 'Z'){
            bukva = bukva - (rotatorN % 26);
            if (bukva < 'A'){
                bukva = 'Z'- ('A'-bukva)+1;
            }
            fprintf (file2, "%c", bukva);
        } else if (bukva >= 'a' && bukva <= 'z'){
            bukva = bukva - (rotatorN % 26);
            if (bukva < 'a'){
                bukva = 'z'- ('a' - bukva)+1;
            }
            fprintf (file2, "%c", bukva);
        } else {
            fprintf (file2, "%c", bukva);
            }
        bukva = getc(file1);
        }
    }
    return 0;
}
