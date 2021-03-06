# Monolog

*Monolog* is a C++ library for basic logging purposes. It writes given records to the console, the debugger and a file.

## Example

```cpp
#include <iostream>
#include <monolog/monolog.h>

int main() {
  monolog::log.set_level(monolog::Level::Debug);
  monolog::log.set_path("test.log");

  LOGD("This is a debug message.");
  LOGW("This is a warning.");
  LOGE("This is an error.");

  return 0;
}
```

```
2016-12-28 21:58:48 [Debug] test.cpp:8 main | This is a debug message.
2016-12-28 21:58:48 [Warning] test.cpp:9 main | This is a warning.
2016-12-28 21:58:48 [Error] test.cpp:10 main | This is an error.
```

## License

*Monolog* is licensed under the [MIT License](https://opensource.org/licenses/MIT).
