# GTMBase64-Objective-C-
A library of Base64 with Objective-C (iOS)

How to use this Base64 library:
1.
   #import "GTMBase64.h"
   #import "GTMDefines.h"

2. 

// encode base64
- (NSString *) encodeBase64:(NSString *) input{
    NSData *data = [input dataUsingEncoding:NSUTF8StringEncoding allowLossyConversion:YES];
    data = [GTMBase64 encodeData:data];
    NSString *base64String = [[NSString alloc] initWithData:data encoding:NSUTF8StringEncoding];
    return base64String;
}

//decode base64
- (NSString *) decodeBase64:(NSString *) input{
    NSData *data = [input dataUsingEncoding:NSUTF8StringEncoding allowLossyConversion:YES];
    data = [GTMBase64 decodeData:data];
    NSString *string = [[NSString alloc] initWithData:data encoding:NSUTF8StringEncoding];
    return string;
}
