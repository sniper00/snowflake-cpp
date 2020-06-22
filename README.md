# snowflake-cpp
A C++ port of Twitter's Snowflake id generation algorithm

# Use
```cpp
    using snowflake_t = snowflake<1534832906275L>;
    snowflake_t uuid;
    uuid.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = uuid.nextid();
        std::cout << id << "\n";
    }
```

# Use with lock
```cpp
    using snowflake_t = snowflake<1534832906275L,std::mutex>;
    snowflake_t uuid;
    uuid.init(1, 1);

    for (int64_t i = 0; i < 10000; ++i)
    {
        auto id = uuid.nextid();
        std::cout << id << "\n";
    }
```


