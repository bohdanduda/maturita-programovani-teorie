# GDI grafika
* nejčastěji kreslíme na PictureBox
* kreslení můžeme spouštět 2mi způsoby -
1. událost Paint,
2. vyrobíme objekt Graphics v jakymkoli objektu ve formsech
* Objekt graphics: __Draw__ - pero, __Fill__ - štětec
## kreslení jednoduchých objektů
* střed souřadného systému je v levém rohu
### čára
* použijeme fuknci `Draw()`, vybereme barvu pera, zadáme souřadnice
### kružnice
* funkce `DrawElipse()`, vybereme barvu, souřadnice, šiřku a výšku
* je vepsaná do čtverce, nemá poloměr
### obdélník
* použijeme funkci `DrawRectangle()`, vybereme barvu, zadáme počáteční souřadnice, také zadáme šířku a výšku obdélníku
## Funkce fill
* práce stejná jako se štětcem, až na to, že pro výběr barvy se používá Brushes. Objekt vyplní
## práce s barvami
* můžeme si vytvořit vlastní barvu pomocí funkce `FromArgb()`, zadáme hodnoty rgb a alfa kanál - ten určuje průhlednost
## definice štětce a pera
* Instance nového pera
* `Pen p = new Pen(Color.Black, 10);`
* Instance nového štětce
* `Brush b = new SolidBrush(Color.Blue);`
* u štětce musíme použít třídu SoludBrush - třída Brush je abstraktní
* Vlastní pero, nebo štětec si můžeme vyrobit.. Instancujeme jí jako třídu. Nastavíme barvu a tloušťku
## objekt Graphics
## událost Paint
* Událost Paint se spustí na začátku kompilace, nakreslí na pictureBox zadanou kresbu, nebo tvar
* Příklad nakreslení čtverce v počátečním bodě, o velikosti 100x100 pixelů:
```
private void pictureBox1_Paint(object sender, PaintEventArgs e)
{
    Graphics graphics = e.Graphics;

    Pen pen = new Pen(Brushes.Blue);
    graphics.DrawEllipse(pen, 0, 0, 100, 100);
}
```
## kreslení obrázků
* Provádíme pomocí `graphics.DrawImage()`
* Instance: `graphics.DrawImage(new Bitmap("Cesta obrázku"), 100, 100);` - můžeme definovat i šířku a výšku
* např. bílé pozadí nastavíme pomocí `graphics.Clear(color.White)`
## kreslení textů
* Provadí se pomocí `graphics.DrawString()`
* instance kreslení textu: `graphics.DrawString("Hello World", new Font("Arial", 20), Brushes.Green, 50, 50)`
* Když chceme dát text do středu, tak musíme změřit jeho velikost pomocí `graphics.MeasureString`, také k ní musíme dodat font a velikost textu
* Proměnnou ukládáme do třídy `SizeF` - poskytuje nám šířku a výšku
## export do JPG
* definujeme si obrázek k exportu:
* `Image img = new Bitmap(delkaX, delkaY);`
* z img si pak vyrobíme graphics:
* `Graphics g = new Graphics.FromImage(img);`
* Uložíme pomocí metody save: `img.Save("cesta uložení");`
## transformace SS
* pomocí metody `graphics.TranslateTransform("x", "y");` můžeme posunout počáteční souřadnice
* také můžeme použít metodu `graphics.RotateTransform("úhel");` - tím otočíme souřadnice o stupěň
* `graphics.ScaleTransform("hodnota škálování x", "hodnota škálování y");` - každou hodnotu vynásobí hodnotami škálování
* Reset provádíme metodou `graphics.ResetTransform()`
