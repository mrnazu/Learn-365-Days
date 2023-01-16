# URL Encoding
Even though web applications have different purposes, technologies, etc., the use of data encoding is something that cannot be neglected.

From a penetration testing point of view, understanding what kind of data encoding is being used and how it works is fundamental in ensuring that the tests are performed as intended

Main types of data encoding used in web-oriented applications:
-- URL encoding
-- HTML encoding
-- Base (32|64) encoding
-- Unicode encoding

URLs sent over the Internet must contain characters in the range of the US-ASCII code character set. If unsafe characters are present in a URL, encoding them is required.

The URL-encoding, or percent-encoding, replaces characters outside the allowed set with a "%" followed by the two hexadecimal digits representing the numeric value of the octet.

```# => %23
? => %3F
& => %24
% => %25
/ => %2F
+ => %2B
<space> => %20 or + ```

# HTML Encoding
