| Offset | Size | Type | Description |
| --- | --- | --- | --- |
| -0x00 | 2 | UInt16| Unknown. Possibly major version of file |
| -0x02 | 2 | UInt16| Unknown. Possibly minor version of file |
| -0x04 | 4 | Char[4]| Magic |
| -0x08 | 4 | UInt32| Image size |
| -0x0C | 4 | UInt32| Array count. Cubemaps use 6 |
| -0x10 | 4 | UInt32| Alignment of image block. Usually 4096 |
| -0x14 | 4 | UInt32| Number of mip maps |
| -0x16 | 2 | UInt16| Padding |
| -0x19 | 1 | UInt8| Unknown. Usually 4 |
| -0x20 | 1 | UInt8| Image format |
| -0x24 | 4 | UInt32| Unknown. Usually 1 |
| -0x28 | 4 | UInt32| Image height |
| -0x2C | 4 | UInt32| Image width |
| -0x30 | 4 | UInt32| Padding |
| -0x70 | 64 | String| Name of texture. Total space is 64 bytes. |
| -0xB0 | 64 | UInt32[]| Array of mip map sizes |

Everything after the footer is the image block. This block is swizzled in Smash Ultimate with the same algorithm as BNTX.
The game might be able to use raw DDS but is untested. 

Image formats:

| Type | Value |
| --- | --- |
| R8G8B8A8_UNORM | 0x00 |
| R8G8B8A8_SRGB | 0x05 |
| R32G32B32A32_FLOAT | 0x34 |
| B8G8R8A8_UNORM | 0x50 |
| B8G8R8A8_SRGB | 0x55 |
| BC1_UNORM | 0x80 |
| BC1_UNORM | 0x80 |
| BC1_UNORM | 0x85 |
| BC2_UNORM | 0x90 |
| BC2_SRGB | 0x95 |
| BC3_UNORM | 0xa0 |
| BC3_SRGB | 0xa5 |
| BC4_UNORM | 0xb0 |
| BC4_SNORM | 0xb5 |
| BC5_UNORM | 0xc0 |
| BC5_SNORM | 0xc5 |
| BC6_UFLOAT | 0xd7 |
| BC7_UNORM | 0xe0 |
| BC7_SRGB | 0xe5 |








