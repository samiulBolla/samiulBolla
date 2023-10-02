#include <stdio.h>
#include <string.h>
#include <ctype.h> // For isspace function

void strtrim(char* str) {
    // Trim leading whitespace
    while (isspace((unsigned char)*str)) {
        str++;
    }

    // Trim trailing whitespace
    char* end = str + strlen(str) - 1;
    while (end > str && isspace((unsigned char)*end)) {
        end--;
    }
    end[1] = '\0';
}

int main() {
    char input[22];
    printf("Enter a phrase: ");
    fgets(input, sizeof(input), stdin);

    // Trim whitespace from input
    strtrim(input);

    if (strcmp(input, "her eyes") == 0) {
        printf("an endless ocean in which I wanna drown away.\n");
    }
    else if (strcmp(input, "her lips") == 0) {
        printf("the sharpest thing which is torning me every day.\n");
    }
    else if (strcmp(input, "her smile") == 0) {
        printf("the most soothing thing which I can easily die for.\n");
    }
    else if (strcmp(input, "her words") == 0) {
        printf("a fragrance that calms my soul.\n");
    }
    else if (strcmp(input, "her hair") == 0) {
        printf("a dark cloudy sky.\n");
    }
    else {
        printf("Invalid input.\n");
    }
    return 0;
}

