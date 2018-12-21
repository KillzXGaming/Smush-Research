## Footer

| Offset | Size | Type | Description |
| --- | --- | --- | --- |
| -0x00 | 2 | UInt16| Major version of file |
| -0x02 | 2 | UInt16| Minor version of file |
| -0x04 | 4 | Char[4]| Magic |
| -0x08 | 4 | UInt32| Image size |
| -0x0C | 4 | UInt32| Array count. Cubemaps use 6 |
| -0x10 | 4 | UInt32| Alignment of image block. Usually 4096 |
| -0x14 | 4 | UInt32| Number of mip maps |
| -0x16 | 4 | UInt32| Image format + Type |
| -0x20 | 4 | UInt32| Pixel Size Z |
| -0x24 | 4 | UInt32| Pixel Size Y (Height) |
| -0x28 | 4 | UInt32| Pixel Size X (Width) |
| -0x2C | 4 | UInt32| Padding |
| -0x70 | 64 | String| Name of texture. Total space is 64 bytes. |
| -0xB0 | 64 | UInt32[]| Array of mip map sizes |

## Image Block

Everything after the footer is the image block. This block is swizzled in Smash Ultimate with the same algorithm as BNTX.
The game might be able to use raw DDS but is untested. 

[Example Swizzle](https://github.com/KillzXGaming/Switch-Toolbox/blob/master/Switch_FileFormatsMain/FileFormats/Texture/TegraX1Swizzle.cs)

## Image formats:

| Type | Value |
| --- | --- |
| R8G8B8A8_UNORM | 0x0000 |
| R8G8B8A8_SRGB | 0x0005 |
| R32G32B32A32_FLOAT | 0x3004 |
| B8G8R8A8_UNORM | 0x5000 |
| B8G8R8A8_SRGB | 0x5005 |
| BC1_UNORM | 0x8000 |
| BC1_UNORM | 0x8000 |
| BC1_UNORM | 0x8005 |
| BC2_UNORM | 0x9000 |
| BC2_SRGB | 0x9005 |
| BC3_UNORM | 0xa001 |
| BC3_SRGB | 0xa005 |
| BC6_UFLOAT | 0xd007 |
| BC7_UNORM | 0xe000 |
| BC7_SRGB | 0xe005 |
