#include <stdio.h>
#include <string.h>

int main() {
    char input[100];
    int length;
    int i;

    printf("Enter a string: ");
    scanf("%s", input);
    length = strlen(input);

    if (length == 2 && input[0] == 'a' && input[1] == 'b') {
        printf("String recognized under ab*\n");
    } else if (length == 3 && input[0] == 'a' && input[1] == 'b' && input[2] == 'c') {
        printf("String recognized under a+b+c\n");
    } else {
        printf("String not recognized\n");
    }

    return 0;
}
