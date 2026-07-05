# Karavansaray Events V2

Bu kopya, canlı `karavansaray-events` Firebase projesine yazmayacak şekilde hazırlanmıştır.

## Guvenli ayrim

- Eski site: `https://karavansarayevents.netlify.app/`
- Eski Firebase project: `karavansaray-events`
- V2 site: yeni Netlify site olarak kurulacak
- V2 Firebase project: yeni Firebase project olarak kurulacak
- V2 koleksiyon: `events`

`index.html` icindeki Firebase config bilerek bos birakildi. Config doldurulana kadar uygulama yerel modda calisir ve eski Firebase verilerine dokunmaz.

## Yeni Firebase project adimlari

1. Firebase Console'da yeni project olustur: `karavansaray-events-v2`
2. Firestore Database olustur.
3. Web App ekle ve Firebase config degerlerini al.
4. Firestore Rules icin `firestore.rules` dosyasindaki taslagi kullan.
5. Yeni Firestore'a aktarilacak temiz seed dosyasi:
   `data/events-seed.json`

Canli verinin tam yedegi ayrica su dosyada tutuldu:
`C:\Users\Asus\Documents\Codex\2026-07-05\fi\outputs\karavansaray-events-firestore-backup-20260705-091411.json`

## Config ekleme

`index.html` icindeki `firebaseConfig` alanina yeni Firebase Web App config degerlerini yaz:

```js
const firebaseConfig = window.KARAVANSARAY_FIREBASE_CONFIG || {
  apiKey: "YENI_API_KEY",
  authDomain: "karavansaray-events-v2.firebaseapp.com",
  projectId: "karavansaray-events-v2",
  storageBucket: "karavansaray-events-v2.firebasestorage.app",
  messagingSenderId: "YENI_SENDER_ID",
  appId: "YENI_APP_ID",
  measurementId: "YENI_MEASUREMENT_ID"
};
```

## Yeni Netlify site

Yeni Netlify site olustururken bu repo/branch deploy edilebilir. Build komutu gerekmez; publish directory proje kok dizinidir.
