
# How to use this GTMBase64 library
1.

   #import "GTMBase64.h"
   
   #import "GTMDefines.h"
   
2.
- (NSString *) encodeBase64:(NSString *) input{
    NSData *data = [input dataUsingEncoding:NSUTF8StringEncoding allowLossyConversion:YES];
    data = [GTMBase64 encodeData:data];
    NSString *base64String = [[NSString alloc] initWithData:data encoding:NSUTF8StringEncoding];
    return base64String;
}


- (NSString *) decodeBase64:(NSString *) input{
    NSData *data = [input dataUsingEncoding:NSUTF8StringEncoding allowLossyConversion:YES];
    data = [GTMBase64 decodeData:data];
    NSString *string = [[NSString alloc] initWithData:data encoding:NSUTF8StringEncoding];
    return string;
}
