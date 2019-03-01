# CAST128-for-Delphi
Delphi implementation of the free CAST-128 symmetric encryption algorithm (RFC 2144)

Sample usage
-------------

```
var   
  cast: TCast128;
      
  cast := TCast128.Create;
  cast.Init(key, keyLen, iv); //key must be 1..16 bytes long
  cast.EncryptECB(inBlock, outBlock); //block must be exactly 8-bytes
  cast.Burn;
  cast.Free;
```
