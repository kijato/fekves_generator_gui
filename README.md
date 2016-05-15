# fekves_generator_gui

Felhasználói útmutató a "fekves_general_gui.exe" programhoz

A program fejlesztésének eredeti célja a fekves_general.exe-vel feldarabolt DAT állományok NKP-s igény szerinti könyvtár-struktúrába történő másolása volt, melyet eddig egy batch-fájl párossal lehetett viszonylag kényelmesen megoldani.
Mivel sokan vannak, akik idegenkednek a parancssortól, a fejlesztés közben fekvésenkénti daraboláshoz használt program kényelmesebb használata is bekerült a megvalósított funkciók közé.

Követelmények:
- A program .NET-es, így ezen keretrendszer kell a futtatásához (4.0-s verzióval teszteltem).
(Egyéb különleges igény nincs: ha az XP elindul a gépen és van keretrendszer, akkor nem lehet gond az indítással. Elvileg.)
+ A fekvésekre bontáshoz szükséges a fekves_general.exe elérhetősége. (Ajánlott a fekves_general.exe mellé tenni, bár ez nem létkérdés.)
+ A "pakolászáshoz" szükséges egy, a jogerős állományok elérhetőségét megadó fájl-lista.

Használat:
- Első lépés a fájl-lista összeállítása (bár ha már megvan, mert például nem most kezdted a fekvésekre bontást, ez átugorható).
- Második lépés (és fül) a fekves_general.exe és a hozzá tartozó lista megadása és "a dolog" elindítása.
- Harmadik lépés - az NKP kedvéért - a keletkezett állományok szétpakolászása (igény szerint: másolása, vagy mozgatása) a szükséges könyvtárakba.

Megjegyzések:
- A fekves_general.exe által készített log-fájlok az eredeti helyükön maradnak.
- A textbox-okba 2x kattintva felugrik az OpenFile/DirDialog.
- A járási könyvtárakat nem hozza létre, de tervezgetem ezt is, és a pakolászás utáni automata tömörítést és MD5 ellenőrző összeg képzést (digitális aláírás hiányában ezzel "hitelesítek"), hogy ezzel se kelljen "kézzel" vacakolni.
- Nálam minden funkció rendesen működött, azonban volt egy visszajelzés, amivel nem tudtam mit kezdeni: "Win XP SP3 van a gépen, .Net 4 Extended keretrendszerrel. A települések és fekvések könyvtárait a program létrehozza, a null.txt is kezeli, de mivel magát a leválogatott fekvést nem helyezi át, így az minden fekvés-könyvtárban megjelenik. Az állományok mozgatásával csak a teljes állományt helyezi át a település könyvtárába."


