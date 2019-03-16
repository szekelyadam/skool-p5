# A p5.js és a p5.play alapjai

A mai órán megtanuljuk, hogy lehet p5-ös szereplőket létrehozni és a kevünk szerint beállítani - egyelőre még mozgás nélkül.  


A p5.js alapvető elgondolása az, hogy a képernyő egy nagy vászon, amire rajzolni lehet.  
A p5.play kiegészítő segítségével _szereplőket_, úgynevezett _sprite-okat_ tudunk létrehozni, amiknek a megrajzolása már automatikusan történik.  

## Saját sprite létrehozása

Ebben a binben dolgozz: http://jsbin.com/vizodax/edit?console,output  


Új sprite létrehozása: `bob = createSprite()`  
(Nem muszáj bobnak nevezni, én megszokásból csinálom, így nem kell rajta gondolkodni.)  

bob egy objektum, akinek van egy `rotation` nevű változója.
Mennyi ennek az értéke most? Mi történik, ha megváltoztatod?  
Most már azt is látjuk,  hogy bob a bal felső sarokban forog. Mozgatni kéne.  



bob mozgatása: nagyon precíz lélek, képpontra pontosan meg kell neki mondani, hol legyen: a bal felső saroktól mennyire jobbra és mennyire lefelé.  
`bob.position.x` és `bob.position.y`  


Az egér helye: globális `mouseX` és `mouseY` változók.  

Van globális `width` és `height` változó. Mit adnak meg? Be tudod állítani bobot pont a vászon jobb alsó sarkába?  
Be tudod állítani bobot a vászon közepére?  

Ha segítséget szeretnél a tájékozódáshoz, kattints, és látni fogok a koordinátákat és a tengelyeket.  

bob mérete: `bob.width` és `bob.height`. Nem összekeverendő a globális `width` és `height` változókkal!  

bob színe: `bob.shapeColor`. Választható színek: Google "CSS colors". (https://www.w3schools.com/cssref/css_colors.asp)  
Pl. `bob.shapeColor = "indigo"`  

Ha ki akarod törölni bobot: `bob.remove()`  

## RGBA-színek

Színmodellek: http://output.jsbin.com/befobun/quiet  

RGB színmodell: http://output.jsbin.com/vulomek/quiet  

Sprite színének beállítása RGB színre:  
```
bob.shapeColor = color(189, 70, 102)
```
Az első szám a pirosságot határozza meg, a második a zöldséget, a harmadik a kékséget. Mindhárom 0 és 255 között mozog. Minél nagyobbak a számok, annál világosabb a szín, tehát `color(0, 0, 0)` a fekete és a `color(255, 255, 255)` a fehér.  
(Színek kikereséséhez keress rá Google-n arra, hogy "színválasztó".)  

Ha átlátszóságot is akarsz állítani a sprite-nak, adj meg egy negyedik számot is:  
```
bob.shapeColor = color(189, 70, 102, 50)
```
A negyedik szám a szín "láthatóságát" szabályozó, úgynevezett _alpha_ beállítás. Ez is 0 és 255 között mozog, ahol a 0 a teljesen átlátszó (tehát láthatatlan) és a 255 a teljesen látható (ami amúgy is az alapértelmezés).  

## Sprite-gyűlés
Próbáld ki a sprite-os parancsokat itt: http://jsbin.com/weduva/edit?console,output  
Közben figyeld, mi történik a kivetítőn.  


## GitHub regisztráció

Jövő órától nem parancssorba írjuk a programokat, hanem kódszerkesztőben, és el is mentjük őket. Ehhez regisztrálni kell JSBinre, ami úgy történik, hogy az ember a [github.com](http://github.com) oldalra regisztrál, és utána JSBinen bejelentkezik a GitHub regisztrációjával.  
Részletes instrukciókat [itt találsz](jsbin/jsbin-instructions.md).  

