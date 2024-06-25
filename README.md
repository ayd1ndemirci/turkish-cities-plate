# Bu paket, Türkiye'deki plaka numaraları ve şehir isimlerini ilişkilendiren bir API sağlar.

# Kurulum
Paketi npm üzerinden yüklemek için:
```npm install turkish-cities-plate```

# Kullanım
```js
const turkishCitiesPlate = require('turkish-cities-plate');

// Plaka numarasına göre şehir ismi almak
console.log(turkishCitiesPlate.plaka(34)); // İstanbul
console.log(turkishCitiesPlate.plaka(81)); // Düzce
console.log(turkishCitiesPlate.plaka(100)); // Error: Invalid plate number

// Şehir ismine göre plaka numarası almak
console.log(turkishCitiesPlate.sehir('istanbul')); // 34
console.log(turkishCitiesPlate.sehir('Düzce')); // 81
console.log(turkishCitiesPlate.sehir('Ankara')); // 6
console.log(turkishCitiesPlate.sehir('NonExistingCity')); // Error: City not found
```
# API Referansı
`plaka(num: number): string`

Verilen plaka numarasına karşılık gelen şehir ismini döndürür.

- `num` (number): Plaka numarası (1-81 arası bir tamsayı).
- Döndürülen Değer (string): Şehir ismi veya hata mesajı.

`sehir(name: string): number | string`

Verilen şehir ismine karşılık gelen plaka numarasını döndürür.
- `name (string): Şehir ismi.`
- Döndürülen Değer (number | string): Plaka numarası veya hata mesajı