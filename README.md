# fekves_generator_gui

Felhasználói útmutató a "fekves_general_gui.exe" programhoz

### Bevezetés:
A program fejlesztésének eredeti célja az Iván Gyula barátom által készített "fekves_general.exe"-vel feldarabolt DAT állományoknak, az "NKP-s" könyvtár-struktúrába történő rendezése/másolása volt, melyet korábban egy batch-fájl párossal lehetett viszonylag kényelmesen megoldani. Mivel azonban tapasztalataim szerint sokan vannak, akik idegenkednek a parancssortól, így a fejlesztés közben "fekves_general.exe" kényelmesebb használata is bekerült a funkciók közé.

### Követelmények:
- A program .NET-es, így ezen keretrendszer kell a futtatásához (a 4.0-ás és 4.5.2-es verzióval teszteltem XP és Windows 7 alatt).
- Egyéb különleges igény nincs: ha a Windows elindul az adott gépen és van .NET keretrendszer, akkor nem lehet gond az indítással. (Elvileg...)
+ A fájl lista összeállításához szükség van a DAT állományok elérhetőségére.
+ A fekvésekre bontáshoz szükséges a "fekves_general.exe" és az előző pontban létrehozott fájl lista elérhetősége. Egyébként ezt a listát kell(ene) a parancssorban átadni a "fekves_general.exe"-nek. (Ajánlott jelen programot a fekves_general.exe "mellé" tenni, bár ez nem létkérdés.)
+ A feldarabolt állományok rendezéséhez/másolgatásához szükséges az előző pontokban is említett, a jogerős állományok elérhetőségét megadó fájl-lista.

### Használat:
- Első lépés a fájl-lista összeállítása (ha már megvan a lista, mert például nem "most" kezdted a fekvésekre bontást, ez átugorható).
- Második lépés (és fül) a fekves_general.exe és a hozzá tartozó lista (ami vagy már megvan, vagy az előbb készítetted el...) megadása és "a dolog" elindítása.
- Harmadik lépés a keletkezett állományok szétpakolászása (igény szerint: másolása, vagy mozgatása) a szükséges könyvtárakba.
+ Ezt követően a könyvtárakat (mivel "nálam" az egyes teleplülések járásonként külön-külön könyvtárakban vannak, a járási könyvtárakat) át kell nevezni, majd lehet tömöríteni, CD-re írni, stb.

### Megjegyzések:
- A fájl nevekben, elérési utakban biztos, ami biztos alapon ne használjunk szóközt.
- A fekves_general.exe által készített log-fájlok az eredeti helyükön maradnak.
- A textbox-okba 2x kattintva felugrik az OpenFile/DirDialog.
- A program a járási könyvtárakat egyenlőre nem hozza létre, de tervezem ezt is beépíteni, mint a "pakolászás" utáni automata tömörítést és MD5 ellenőrző összeg képzést (digitális aláírás hiányában azt hiszem ez az egyetlen "hitelesítési" lehetőség), hogy ezzel se kelljen "kézzel" vacakolni.
- Nálam minden funkció rendesen működött, azonban volt egy visszajelzés, amivel nem tudtam mit kezdeni:
"Win XP SP3 van a gépen, .Net 4 Extended keretrendszerrel. A települések és fekvések könyvtárait a program létrehozza, a null.txt is kezeli, de mivel magát a leválogatott fekvést nem helyezi át, így az minden fekvés-könyvtárban megjelenik. Az állományok mozgatásával csak a teljes állományt helyezi át a település könyvtárába."
Ennkek az általam nem reprodukálható hibának(?) a javítása még várat magára.

### Hivatkozás(ok):
- A "fekves_general.exe"-t Iván Gyula (ivan.gyula@fomi.hu) késztítette.

### Terjesztési feltételek:
A programok ingyenesen terjeszthetők, kereskedelmi forgalmazásuk tiltott.
