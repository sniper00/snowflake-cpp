# snowflake-cpp
A C++ port of Twitter's Snowflake id generation algorithm

# Use
```cpp
    snowflake<> snf;
    snf.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = snf.nextid();
        std::cout << id << "\n";
    }
```

# Use with lock
```cpp
    snowflake<std::mutex> snf;
    snf.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = snf.nextid();
        std::cout << id << "\n";
    }
```


