# snowflake-cpp
A C++ port of Twitter's Snowflake id generation algorithm

# Use
```cpp
    using snowlake_t = snowflake<1534832906275L>;
    snowlake_t snf;
    snf.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = snf.nextid();
        std::cout << id << "\n";
    }
```

# Use with lock
```cpp
    using snowlake_t = snowflake<1534832906275L,std::mutex>;
    snf.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = snf.nextid();
        std::cout << id << "\n";
    }
```


