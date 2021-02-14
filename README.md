# UppGoogleTest
UppGoogleTest is a distributed source nest for [U++](https://www.ultimatepp.org/) platform that wraps [GoogleTest](https://github.com/google/googletest) a popular C++ unit testing framework. The package can be directly downloade using UppHub.

UppGoogleTest provieds two following package:
- **plugin/gtest** - the wrapepr for GoogleTest library.
- **plugin/gmock** - the wrapper for GoogleMock library.

## Examples
To simplify the example, let's test basic String from Upp Core package:
```cpp
#include <Core/Core.h>
#include <plugin/gtest/gtest.h>

class StringTest : public testing::Test {}

TEST_F(StringTest, TestConstruction)
{
    Upp::String empty_string;

    EXPECT_EQ(0, empty_string.GetCount());
    EXPECT_TRUE(empty_string.IsEmpty());
}

TEST_APP_MAIN {}
```

More examples can be found under examples directory.