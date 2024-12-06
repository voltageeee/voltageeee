<h1 align="center">Hi, I'm Ilya</h1>
<h3 align="center">A self-taught pseudodev from Germany</h3>

```
#include <iostream>
#include <ctime>

using namespace std;

struct me {
    const char* name = "ilya";
    int age = 15;
};

int main() {
    time_t now;
    time_t birthday;
    struct tm birthday_date;

    time(&now);

    birthday_date.tm_year = 2025 - 1900;
    birthday_date.tm_mon = 0;
    birthday_date.tm_mday = 31;
    birthday_date.tm_hour = 12;
    birthday_date.tm_min = 30;
    birthday_date.tm_sec = 1;
    birthday_date.tm_isdst = -1;

    birthday = mktime(&birthday_date);

    std::cout << "Days left till my birthday: " << difftime(birthday, now)  / (60 * 60 * 24) << std::endl;

    return 0;
}
```
