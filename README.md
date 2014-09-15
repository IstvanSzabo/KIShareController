KIShareController
=================

[iOS] An UIActivityViewController without view, which has performance improvement and extensible structure.

```objc
@interface MYShareController : KIShareController

+ (NSArray *)supportedActivities {
    return @{
        [[TwitterAcitvity alloc] init],
        [[FacebookActivity alloc] init],
        [[LINEActivity] alloc] init],
        [[WhatsAppActivity] alloc] init],
        [[EmailActivity alloc] init],
        [[SMSActivity alloc] init]
    };
}

@end
```

Then

```objc
NSURL *url = ...;
NSString *text = ...;

NSArray *items = [url, text];
KIShareController *controller = [[KIShareController alloc] initWithActivityItems:items];

controller.activities; // You can use as Data Source

[controller performShareWithIndex:index];
```
