# TFGRelativeDateFormatter

[![Build
Status](https://travis-ci.org/tomguthrie/TFGRelativeDateFormatter.svg?branch=master)](https://travis-ci.org/tomguthrie/TFGRelativeDateFormatter)

Mail.app style relative date formatter.

## Examples

|           | en_GB      | en_US     |
|-----------|:----------:|:---------:|
| Same Day  | 13:45      | 1:45 PM   |
| Yesterday | Yesterday  | Yesterday |
| Same Week | Monday     | Monday    |
| Same Year | 15 Mar     | Mar 15    |
| Last Year | 22/04/2013 | 4/22/13   |

## Usage

```objective-c
NSDate *date = ...;
TFGRelativeDateFormatter *formatter = [[TFGRelativeDateFormatter alloc] init];
NSString *relativeString = [formatter stringForDate:date];
```

The formatter is not thread safe (it uses `NSDateFormatter` internally) but a helper `+sharedFormatter` is provided to easily get a relative date string on the main thread.

```objective-c
NSDate *date = ...;
NSString *relativeString = [[TFGRelativeDateFormatter sharedFormatter] stringForDate:date];
```

## Installation

TFGRelativeDateFormatter is available through
[CocoaPods](http://cocoapods.org), to install it simply add the following line
to your Podfile:

    pod 'TFGRelativeDateFormatter'

Alternatively, simply drag `TFGRelativeDateFormatter.h` and `TFGRelativeDateFormatter.m` to your project.

## Contact

[Thomas Guthrie](https://github.com/tomguthrie)
[@tomguthrie](https://twitter.com/tomguthrie)

## License

TFGRelativeDateFormatter is available under the MIT license. See the LICENSE
file for more info.
