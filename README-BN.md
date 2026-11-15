# Maya AI HUD — Android Studio Project

এই ফোল্ডারটি Android WebView wrapper project। এতে আগের mobile web UI assets অ্যাপের মধ্যে রাখা হয়েছে এবং Android microphone permission bridge যুক্ত করা হয়েছে।

## APK বানানোর নিয়ম
1. কম্পিউটারে Android Studio ইনস্টল করুন।
2. Android Studio → **Open** → এই `maya-android` ফোল্ডার নির্বাচন করুন।
3. Gradle sync শেষ হওয়া পর্যন্ত অপেক্ষা করুন। প্রয়োজনে Android SDK Platform 35 ইনস্টল করুন।
4. **Build → Build Bundle(s) / APK(s) → Build APK(s)** নির্বাচন করুন।
5. APK তৈরি হলে Android Studio-তে **locate** চাপুন। সাধারণত ফাইলটি `app/build/outputs/apk/debug/app-debug.apk`-এ থাকবে।
6. APK ফোনে পাঠিয়ে ইনস্টল করুন। ফোনে “Install unknown apps” অনুমতি চাইতে পারে।

## কী আছে
- Maya HUD-এর responsive mobile interface ও animated orb
- Android WebView app shell
- Android runtime microphone permission এবং browser audio capture bridge
- Offline web asset bundle

## গুরুত্বপূর্ণ সীমাবদ্ধতা
এটি Android Studio-তে build করার জন্য প্রস্তুত source project; এই পরিবেশে Android SDK/Gradle build tool নেই, তাই এখানে signed বা debug APK compile করে পরীক্ষা করা যায়নি। Android-এর CPU/RAM/GPU usage ও temperature দেখানোর native system-monitor module এখনো অন্তর্ভুক্ত নয়; webview edition সেগুলো Android security restriction-এর কারণে দেখায় না।
