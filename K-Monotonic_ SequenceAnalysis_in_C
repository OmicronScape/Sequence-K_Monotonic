#include <stdio.h>

#define N 10

int main() {
    int sequence[N];
    int i, k = 0, max_length = 1, min_length = N, current_length = 1;
    int monotony_changes = 0;
    int valid; // Boolean variable for validity check
    
    // Input and defensive programming to ensure valid values
    do {
        valid = 1;
        for (i = 0; i < N; i++) {
            printf("Enter element %d: ", i + 1);
            scanf("%d", &sequence[i]);
            if (i > 0 && sequence[i] == sequence[i - 1]) {
                printf("Two consecutive identical elements were entered – please re-enter the sequence from the beginning.\n");
                valid = 0;
                break;
            }
        }
    } while (!valid);
    
    // Display the sequence
    printf("The sequence is: [ ");
    for (i = 0; i < N; i++) {
        printf("%d ", sequence[i]);
    }
    printf("]\n");
    
    // Calculate monotony changes and lengths of subsequences
    for (i = 1; i < N; i++) {
        if ((sequence[i] > sequence[i - 1] && sequence[i - 1] < sequence[i - 2]) || 
            (sequence[i] < sequence[i - 1] && sequence[i - 1] > sequence[i - 2])) {
            monotony_changes++;
            if (current_length > max_length) {
                max_length = current_length;
            }
            if (current_length < min_length && current_length > 1) {
                min_length = current_length;
            }
            current_length = 1;
        } else {
            current_length++;
        }
    }
    
    // Update for the last subsequence
    if (current_length > max_length) {
        max_length = current_length;
    }
    if (current_length < min_length && current_length > 1) {
        min_length = current_length;
    }
    
    // Display the results
    printf("The given sequence is %d-monotonic.\n", monotony_changes);
    printf("Minimum length of monotonic subsequences: %d\n", min_length);
    printf("Maximum length of monotonic subsequences: %d\n", max_length);
    
    return 0;
}
