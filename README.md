# Teehee
api for teehee.dev random free joke site
# main
```cpp
#include "Teehee.h"
#include <iostream>

int main() {
   Teehee api;

    auto joke = api.get_random_joke().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    joke.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
