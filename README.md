# chatbot
#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <ctype.h>

string print_respond(string m);

int main(void)
{
    //hello & get name
    string name = get_string("Hi there! What's your name?\n");
    printf("Nice to meet you %s!\n", name);
    //get variable
    string m = get_string("How are you?\n");
    //make capital
    m[0] = toupper(m[0]);
    //respond function outcome
    print_respond(m);
    printf("Goodbye, %s!\n", name);
}

//respond function
string print_respond(string m)
{
    if (0 == strcmp(m, "Good"))
    {
        printf("I'm glad to hear that!\n");
    }
    if (0 == strcmp(m, "Bad"))
    {
        printf("Aw, I'm sorry!\n");
    }

    return m;
}

