# İmza Klasörü

Operatör ıslak imzalarının taranmış görsellerini (tercihen şeffaf arka planlı PNG)
bu klasöre koyun. Örnek:

- `imzalar/kantar1.png`
- `imzalar/lod1.png`

Ardından `index.html` içindeki `operatorImzalari` eşlemesine operatör adı → dosya
yolunu ekleyin:

```js
const operatorImzalari = {
    "KANTAR1": "imzalar/kantar1.png",
    "LOD-1":   "imzalar/lod1.png"
};
```

Eşleme eklenmeyen operatörlerde fişte kesik çizgili (elle imzalanacak) alan görünür.
