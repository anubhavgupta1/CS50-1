# Emoji

## Questions

1. As many as 4

2. sizeof(char) == 1 byte
   emoji > 1 byte
    In other words, it won't fit.

3.

```c
emoji get_emoji(string prompt)
{
    // Get a string from user
    // while (true)
    // {
        string s = get_string("%s", prompt);
        if ((s[0] == 'U' || s[0] == 'u') && s[1] == '+')
        {
            s[0] = '0';
            emoji out = 0;
            //mbstowcs(*out, *s, size_t size);
            emoji bit = mbstowcs(&out, s, 4);
            return bit;
        }
    // }
    return false;
}
```

## Debrief

1. Spent about an hours so far,

2. TODO
