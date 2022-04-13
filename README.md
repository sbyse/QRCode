# QRCode - ImageSharp
Original readme can be found [here](https://github.com/StefH/QRCode#readme), modified readme [here](https://github.com/paperdropio/QRCode). This is fork of a fork which switches up to dotnet6 (only). Originally based on the QRCode created by StefH, then by Paperdropio using the ImageSharp instead of System.Drawing.Common. System.Drawing.Common is a windows only library now see [here](https://docs.microsoft.com/en-us/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only), the changes allows the QRDecoder to use one of the more modern cross platform 2d graphics library ImageSharp. 

## NuGet packages

| Name | NuGet
| - | - |
| `QRCodeDecoder-ImageSharp` | [[NuGet](https://www.nuget.org/packages/QRCodeDecoder-ImageSharp)]

## QRDecoder

### Configure Dependency Injection
``` csharp
...
services.AddQRCodeDecoder();
...
```

### Usage
``` csharp
var decoder = _serviceProvider.GetRequiredService<QRDecoder>();
byte[][] data = decoder.ImageDecoder(sourceBitmap);

var data = QRDecoder.ByteArrayToString(data[0]);
```

## References
- [QRCode by StefH](https://github.com/StefH/QRCode)
- [ImageSharp Fork by Paperdropio](https://github.com/paperdropio/QRCode)