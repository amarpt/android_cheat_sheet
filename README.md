# Android Cheat Sheet

### Kotlin Flow

[Kotlin’s Flow, ChannelFlow, and CallbackFlow Made Easy](https://medium.com/mobile-app-development-publication/kotlins-flow-channelflow-and-callbackflow-made-easy-5e82ce2e27c0)

### Bitmap Pool
```Bitmap bitmapOne = BitmapFactory.decodeFile(filePathOne);
imageView.setImageBitmap(bitmapOne);

// Reuse the bitmap one with two
final BitmapFactory.Options options = new BitmapFactory.Options();
options.inJustDecodeBounds = true;
BitmapFactory.decodeFile(filePathTwo, options);
options.inMutable = true;
options.inBitmap = bitmapOne;
options.inJustDecodeBounds = false;
Bitmap bitmapTwo = BitmapFactory.decodeFile(filePathTwo, options);
imageView.setImageBitmap(bitmapTwo);```
