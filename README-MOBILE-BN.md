# Maya AI HUD — Mobile Edition

এই প্যাকেজে মূল Windows/Python প্রজেক্ট `desktop_original/` ফোল্ডারে অপরিবর্তিত রাখা হয়েছে এবং `mobile/` ফোল্ডারে নতুন responsive Mobile Web App/PWA তৈরি করা হয়েছে।

## মোবাইলে চালানো
1. `mobile` ফোল্ডারের ফাইলগুলো কোনো HTTPS static hosting-এ প্রকাশ করুন (যেমন GitHub Pages/Netlify)।
2. Android Chrome-এ প্রকাশিত HTTPS লিংক খুলুন।
3. Chrome menu থেকে **Add to Home screen** বা **Install app** নির্বাচন করুন।
4. মাইক্রোফোন ভিজ্যুয়ালাইজার চালাতে **START MIC** চাপুন এবং permission দিন। HTTPS বা localhost আবশ্যক।

## কী কাজ করে
- Responsive mobile-first Maya HUD interface
- Animated central orb
- Live clock এবং browser network online/offline state
- User permission-সহ microphone audio visualizer
- PWA manifest এবং offline cache

## Android browser-এর সীমাবদ্ধতা
সাধারণ ওয়েবসাইট/ব্রাউজার Android-এর সম্পূর্ণ CPU/RAM/GPU usage বা hardware temperature পড়তে পারে না। তাই এসবের জায়গায় স্পষ্টভাবে limitation দেখানো হয়েছে; ভুয়া live metric দেখানো হয় না। Android-এ প্রকৃত system metrics, background service, speaker loopback audio ইত্যাদি পেতে আলাদা native Android app এবং platform permissions/API দরকার।

## মূল Windows অ্যাপ
মূল Python/PySide6 desktop project `desktop_original/`-এ রাখা আছে। এই mobile edition মূল desktop app-কে Android APK-তে রূপান্তর করেছে—এমন দাবি করা হচ্ছে না; এটি একই visual direction অনুসরণ করে তৈরি browser-installable mobile version।
