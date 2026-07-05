# Karavansaray Events V2

Bu kopya, canlı `karavansaray-events` Firebase projesine yazmayacak şekilde hazırlanmıştır.

## Guvenli ayrim

- Eski site: `https://karavansarayevents.netlify.app/`
- Eski Firebase project: `karavansaray-events`
- V2 site: yeni Netlify site olarak kurulacak
- V2 Firebase project: yeni Firebase project olarak kurulacak
- V2 koleksiyon: `events`

`index.html` artik yeni `karavansaray-events-v2` Firebase projesine baglidir. Eski `karavansaray-events` Firebase projesine yazmaz.

## Yeni Firebase project adimlari

1. Firebase project olusturuldu: `karavansaray-events-v2`
2. Firestore Database olusturuldu: `(default)` / `nam5`
3. Web App eklendi: `karavansaray-events-v2`
4. Anonymous Authentication etkinlestirildi.
5. Firestore Rules `firestore.rules` ile ayni mantikta yayinda.
6. Yeni Firestore'a aktarilan temiz seed dosyasi:
   `data/events-seed.json`

Canli verinin tam yedegi ayrica su dosyada tutuldu:
`C:\Users\Asus\Documents\Codex\2026-07-05\fi\outputs\karavansaray-events-firestore-backup-20260705-091411.json`

## Config ekleme

Aktif Firebase Web App config:

```js
const firebaseConfig = window.KARAVANSARAY_FIREBASE_CONFIG || {
  apiKey: "AIzaSyDEstgDNz-x3ur0XHFGnUugceWPTgoFdZo",
  authDomain: "karavansaray-events-v2.firebaseapp.com",
  projectId: "karavansaray-events-v2",
  storageBucket: "karavansaray-events-v2.firebasestorage.app",
  messagingSenderId: "528120694671",
  appId: "1:528120694671:web:1a09e4f48007de14c32dfa",
  measurementId: ""
};
```

## Yeni Netlify site

Yeni Netlify site olustururken bu repo/branch deploy edilebilir. Build komutu gerekmez; publish directory proje kok dizinidir.
