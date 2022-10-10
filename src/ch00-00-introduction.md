# Úvod

> Pozn.: Toto vydání je stejné jako kniha [The Rust Programming
> Language][nsprust] dostupná v tištěné formě nebo jako ebook. [No Starch
> Press][nsp].

[nsprust]: https://nostarch.com/rust

[nsp]: https://nostarch.com/

Vítejte v úvodní knize o jazyce Rust. Rust vám pomůže psát rychlejší a
spolehlivější software. Vysokoúrovňová ergonomie a nízkoúrovňové řízení jsou v
programování často v rozporu a Rust tento rozpor zpochybňuje. Díky vyvážení
výkonné technické kapacity a skvělého vývojářského zážitku vám Rust dává možnost
kontrolovat nízkoúrovňové detaily (například využití paměti) bez všech problémů
tradičně s takovou kontrolou spojených.

## Pro koho je Rust

Rust je ideální pro mnoho lidí z několika různých důvodů. Podívejme se na
některé z těch nejdůležitějších skupin.

### Týmy vývojářů

Rust se ukazuje jako produktivní nástroj pro spolupráci velkých vývojářských
týmů s různou úrovní znalostí systémového programování. Nízkoúrovňový kód je
náchylný k různým nenápadným chybám, které lze ve většině jiných jazyků zachytit
pouze díky rozsáhlému testování a pečlivé kontrole kódu zkušenými vývojáři.
V jazyce Rust hraje kompilátor roli strážce tím, že odmítá kompilovat kód s
těmito nevyzpytatelnými chybami, včetně chyb spojených s pararelismem. S pomocí
kompilátoru může tým věnovat svůj čas soustředění se na logiku programu, místo
aby se zabýval hledáním chyb.

Rust přináší do světa systémového programování také moderní vývojářské nástroje:

* Cargo, přibalený správce závislostí a nástroj pro sestavení, umožňuje
  přidávat, kompilovat a spravovat závislosti bez problémů a konzistentně v
  celém ekosystému Rust.
* Rustfmt zajišťuje konzistentní styl zápisu u všech vývojářů.
* Rust Language Server umožňuje integraci automatického dokončování kódu a
  inline chybových zpráv do vývojového prostředí (IDE).

Pomocí těchto a dalších nástrojů v ekosystému Rust mohou být vývojáři
produktivní při psaní kódu na systémové úrovni.

### Studenti

Rust je určen pro studenty a zájemce o systémové koncepty. Pomocí jazyka Rust se
mnoho lidí naučilo témata, jako je vývoj operačních systémů. Komunita je velmi
vstřícná a ráda odpovídá na dotazy studentů. Prostřednictvím úsilí, jako je
tato kniha, chtějí týmy Rustu zpřístupnit systémové koncepty více lidem, zejména
těm, kteří se s programováním teprve seznamují.

### Společnosti

Stovky velkých i malých firem používají Rust v produkci pro nejrůznější úlohy.
Mezi tyto úlohy patří nástroje příkazového řádku, webové služby a DevOps
nástroje, vestavěné systémy, analýza a transkódování zvuku a videa, kryptoměny,
bioinformatika, vyhledávače, aplikace pro internet věcí, strojové
učení, a dokonce i podstatné části webového prohlížeče Firefox.

### Open Source Vývojáři

Rust je určen pro lidi, kteří chtějí budovat programovací jazyk Rust, jeho
komunitu, vývojářské nástroje a knihovny. Budeme rádi, když se i vy budete
podílet na vývoji.

### Lidé, kterým záleží na rychlosti a stabilitě

Rust je pro lidi, kteří touží po rychlosti a stabilitě jazyka. Rychlostí máme na
mysli rychlost programů, které můžete v jazyce Rust vytvářet, a rychlost, s
jakou vám Rust umožní je psát. Kontroly překladače jazyka Rust zajišťují
stabilitu prostřednictvím doplňování funkcí a refaktoringu. To jde v kontrastu s
křehkým starším kódem v jazycích bez těchto kontrol, který se vývojáři často
bojí upravovat. Díky snaze o abstrakce s nulovými náklady, tedy funkce vyšší
úrovně, které se kompilují do kódu nižší úrovně stejně rychle jako kód napsaný
ručně, Rust usiluje o to, aby bezpečný kód byl také rychlým kódem.

Rust má potenciál pomáhat i mnoha dalším uživatelům; ti, kteří jsou zde zmíněni,
jsou pouze jedněmi z největších zástupců. Největší ambicí jazyka je Rust
odstranit kompromisy, které programátoři přijímali po desetiletí, a to
zajištěním bezpečnosti *a* produktivity a také rychlosti *a* ergonomie.
Vyzkoušejte Rust a zjistěte, zda vám budou jeho
rozhodnutí vyhovovat.

## Pro koho je tato kniha

Tato kniha předpokládá, že jste již psali kód v jiném programovacím jazyce, ale
nepředpokládá, ve kterém. Snažili jsme se, aby byl materiál široce přístupný pro
zájemce z nejrůznějších programátorských prostředí. Nevěnujeme mnoho času
tomu, co programování *je* nebo jak o něm přemýšlet. Pokud jste v programování
úplní nováčci, bude pro vás lepší, když si přečtete knihu, která poskytuje
speciální úvod do programování.

## Jak knihu používat

Tato kniha obecně předpokládá, že ji budete číst postupně od začátku do konce.
Pozdější kapitoly navazují na koncepty v předchozích kapitolách a dřívější
kapitoly se nemusí zabývat podrobnostmi o daném tématu; obvykle se k tématu
vracíme v pozdější kapitole.

V této knize najdete dva druhy kapitol: kapitoly o konceptech a kapitoly o
projektech. V konceptových kapitolách se seznámíte s určitým aspektem Rustu.
Zatímco v projektových kapitolách budeme společně vytvářet menší programy a
aplikovat v nich to, co jste se doposud naučili. Kapitoly 2, 12 a 20 jsou
projektové kapitoly; zbytek jsou kapitoly konceptové.

První kapitola vysvětluje, jak nainstalovat Rust, jak napsat program "Hello,
world!" a jak používat Cargo, správce balíčků a nástroj pro sestavení Rustu.
Kapitola 2 je praktickým úvodem do jazyka Rust. Zde se věnujeme konceptům na
vysoké úrovni a další kapitoly se budou věnovat podrobnějším detailům. Pokud si
chcete všechno hned vyzkoušet na vlastní kůži, je kapitola 2 tím pravým místem.
Zpočátku možná budete chtít dokonce přeskočit kapitolu 3, která se zabývá
funkcemi jazyka Rust podobnými funkcím jiných programovacích jazyků, a přejít
rovnou ke kapitole 4, kde se seznámíte se systémem vlastnictví jazyka Rust.
Pokud jste však obzvláště pečliví žáci, kteří se raději naučí každý detail, než
přejdou k dalšímu, možná budete chtít kapitolu 2 přeskočit a přejít rovnou ke
kapitole 3 a ke kapitole 2 se vrátit, až když budete chtít pracovat na projektu
s využitím nabytých znalostí.

Kapitola 5 pojednává o strukturách a metodách a kapitola 6 se zabývá
výčty, `match` výrazy a konstruktu `if let` pro tok řízení. V Rustu budete
struktury a metody používat k vytváření vlastních datových typů.

V kapitole 7 se seznámíte se systémem modulů a s pravidly viditelnosti pro
uspořádání kódu a s jeho veřejným rozhraním (API). Kapitola 8 pojednává o
některých běžných kolekcích, které poskytuje standardní knihovna, jako jsou
například vektory, řetězce nebo hashovací mapy. Kapitola 9 se zabývá filozofií
a technikami zpracování chyb v jazyce Rust.

Kapitola 10 se zabývá genericitou, vlastnostmi a životností. Tyto nástroje vám
umožňují definovat kód, který se vztahuje na více datových typů. Kapitola 11 je
věnována testování, které je i díky bezpečnostním zárukám Rustu nezbytné pro
zajištění správné logiky programu. V kapitole 12 vytvoříme vlastní implementaci
podmnožiny funkcí nástroje `grep` pro příkazový řádek, který vyhledává text v
souborech. K tomu využijeme mnoho konceptů, které jsme probrali v předchozích
kapitolách.

Kapitola 13 se zabývá uzávěry a iterátory: funkcionalitami, které pocházejí z
funkcionálních programovacích jazyků. V kapitole 14 se budeme podrobněji zabývat
systémem Cargo a probereme osvědčené postupy pro sdílení knihoven s ostatními.
Kapitola 15 se zabývá chytrými ukazateli a vlastnostmi (traits), které umožňují
jejich funkčnost.

V kapitole 16 se seznámíme s různými modely paralelního programování a povíme
si, jak vám Rust pomůže programovat ve více vláknech bez obav. V kapitole 17 se
podíváme na srovnání idiomů jazyka Rust s principy objektového programování,
které možná znáte.

Kapitola 18 je odkazem na vzory a porovnávání vzorů, což jsou mocné způsoby
vyjádření myšlenek v Rustu. Kapitola 19 obsahuje přehršel pokročilých zajímavých
témat, včetně nechráněného (unsafe) Rustu, maker a dalších informací o dobách
životnosti, vlastnostech, typech, funkcích a uzávěrech.

V kapitole 20 dokončíme projekt, ve kterém budeme implementovat nízkoúrovňový
vícevláknový webový server!

Některé přílohy obsahují užitečné informace o jazyce ve formě příručky. Dodatek
A se zabývá klíčovými slovy jazyka Rust, dodatek B operátory a symboly jazyka
Rust, dodatek C derivovatelnými vlastnostmi poskytovanými standardní knihovnou,
dodatek D některými užitečnými vývojovými nástroji a dodatek E vysvětluje edice
jazyka Rust. V dodatku F najdete překlady knihy a v dodatku G se budeme zabývat
tím, jak se Rust vyvíjí a co je to tzv. "nightly" Rust.

Neexistuje žádný nesprávný způsob, jak tuto knihu číst: pokud chcete
přeskakovat, jděte směle do toho! Možná se budete muset vrátit k dřívějším
kapitolám, pokud se někde ztratíte. Ale postupujte tak, jak vám to vyhovuje.

<span id="ferris"></span>

Důležitou součástí procesu studia jazyka Rust je naučit se číst chybová hlášení,
která překladač zobrazuje: ta vás navedou k funkčnímu kódu.
Proto uvedeme mnoho příkladů, které se nezkompilují, spolu s chybovými
hlášeními, které vám překladač v každé situaci zobrazí. Pamatujte, že pokud
zadáte a spustíte náhodný příklad, nemusí se zkompilovat! Ujistěte se, že jste
si přečetli okolní text, kde najdete, zda příklad, který se snažíte spustit, má
selhat nebo ne. Ferris vám také pomůže rozlišit kód, který nemá fungovat:

| Ferris                                                                                                           | Meaning                               |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <img src="img/ferris/does_not_compile.svg" class="ferris-explain" alt="Ferris with a question mark"/>            | Tento kód se nezkompiluje!            |
| <img src="img/ferris/panics.svg" class="ferris-explain" alt="Ferris throwing up their hands"/>                   | Tento kód selže (panic)!              |
| <img src="img/ferris/not_desired_behavior.svg" class="ferris-explain" alt="Ferris with one claw up, shrugging"/> | Tento kód nevede k žádoucímu chování. |

Ve většině situací vás navedeme k nápravě kódu, který nejdříve nepůjde
zkompilovat.

## Source Code

Zdrojové soubory, ze kterých je tato kniha vygenerována, naleznete na
[GitHubu][book].

[book]: https://github.com/rust-lang/book/tree/main/src
