### Cách để thêm font-face vào trang web

#### Thêm source vào folder
```php
shared\fonts\FOT-TsukuMinPro-B.otf
shared\fonts\FOT-TsukuMinPro-D.otf
shared\fonts\FOT-TsukuMinPro-E.otf
shared\fonts\FOT-TsukuMinPro-H.otf
shared\fonts\FOT-TsukuMinPro-L.otf
shared\fonts\FOT-TsukuMinPro-LB.otf
shared\fonts\FOT-TsukuMinPro-M.otf
shared\fonts\FOT-TsukuMinPro-R.otf
shared\fonts\FOT-TsukuMinPro-RB.otf
```

#### Thêm font-face vào CSS

```css
@font-face {
  font-family: "FOT-TsukuMinPro";
  src: url("/shared/fonts/FOT-TsukuMinPro-B.otf") format("opentype");
  font-weight: normal;
}

@font-face {
  font-family: "FOT-TsukuMinPro";
  src: url("/shared/fonts/FOT-TsukuMinPro-D.otf") format("opentype");
  font-weight: normal;
}

@font-face {
  font-family: "FOT-TsukuMinPro";
  src: url("/shared/fonts/FOT-TsukuMinPro-E.otf") format("opentype");
  font-weight: normal;
}
```

