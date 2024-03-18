# Today I Learnt

## 28-02-2024 (Manifest Chaos)

Today I learnt the structure of `AndroidManifest.xml`, which is a file in Android application, crucial for defining essential information such as package name, permissions, and components like activities and services. It specifies permissions required for accessing device features and declares intent filters for handling various types of intents.

I was working on a Flutter project, where I needed to integrate "access phone's internal storage" functionality. I used a package from `pub.dev` and copy pasted the following snippet without thinking too much(silly me 😅) in `AndroidManifest.xml`

```xml
<application android:requestLegacyExternalStorage="true"></application>
```

After adding this, the app was working fine in debug mode, but when I tried to built the release apk, it started to crash. On this day, I learnt that, there is always one `<application>` tag, in `AndroidManifest.xml` file. It took me almost 2 to 3 days along with a colleague, to debug this error. But, it was great learning experience, and I would never make this mistake again in my whole life lol.
