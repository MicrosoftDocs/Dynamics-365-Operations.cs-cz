---
title: Technické verze a kategorie technických produktů
description: Tento článek poskytuje informace o konceptu technických verzí. Technické verze zajišťují, že různé stavy produktu a jeho dat jsou udržovány aktuální a jasné a že je lze v systému vizualizovat.
author: t-benebo
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a98ead81a61ceac2ed721848847164f76e758f80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872058"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Technické verze a kategorie technických produktů

[!include [banner](../includes/banner.md)]

Technické produkty se během svého životního cyklu vyvíjejí z mnoha důvodů. Mohou být například zavedeny změny za účelem zlepšení provozuschopnosti produktu, změny komponenty, protože ji dodavatel již nenabízí, reakce na nové poznatky nebo oprava chyb v počátečním návrhu. Existuje také mnoho důvodů, proč by tyto změny měly být ukládány jako součást probíhajícího produktu takovým způsobem, aby nedošlo k přepsání předchozích dat. Zde je několik takových důvodů:

- Chcete sledovat produkt, jak byl vyroben a dodán vašim zákazníkům v předchozích stavech životního cyklu.
- Než změny schválíte a použijete, potřebujete dobu realizace.
- Chcete mít časové razítko na každé změně a chcete mít možnost dodávat dříve vyrobené produkty odděleně od sebe navzájem.

*Technické verze* zajišťují, že různé stavy produktu a jeho dat jsou udržovány aktuální a jasné a že je lze v systému vizualizovat. Tento koncept vám pomůže udržovat konzistenci, uzamknout kusovník (BOM) pro výrobu, eliminovat variabilitu a snadno identifikovat změny.

Obecně platí, že pravidlo *form-fit-function* se použije k určení, zda změna vyžaduje nový produkt, novou verzi nebo aktualizaci stávající verze. Každý ze tří výrazů v názvu tohoto pravidla odkazuje na konkrétní aspekt dílu, který pomáhá technikům spárovat díky s potřebami. Pravidlo form-fit-function zvyšuje flexibilitu konstrukčních změn, protože ke změně dílu jsou vyžadovány minimální náklady na dokumentaci a design, za předpokladu, že bude zachováno vhodnost, forma a funkce produktu.

- **Vhodnost** označuje schopnost dílu nebo funkce připojit se k jiné funkci nebo díl v sestavení, spojit se s nimi nebo se k nim připojit. Vhodnost umožňuje dílu vyhovět požadovaným tolerancím sestavení, aby bylo užitečné.
- **Forma** odkazuje na vlastnosti dílu nebo sestavení, jako jsou vnější rozměry, hmotnost, velikost a vizuální vzhled. Forma je aspekt, který je nejvíce ovlivněn estetickými možnostmi technika. Zahrnuje kryt, šasi a ovládací panel, které se stávají vnější „tváří“ produktu.
- **Funkce** je kritérium, které je splněno, když díl účinně a spolehlivě plní stanovený účel. Například v elektronickém produktu může funkce záviset na použitých polovodičových součástech a softwaru nebo firmwaru. Často to také může záviset na vlastnostech vybraného krytu. Dva z nejčastějších důvodů, proč kryt může selhat v kritériu funkce, jsou špatně umístěné porty nebo jejich nesprávná velikost, a zavádějící nebo chybějící označení. 

## <a name="engineering-versions"></a>Technické verze

Když používáte technické produkty, každý produkt má alespoň jednu technickou verzi. Počáteční technická verze se vytvoří automaticky při vytváření technického produktu. Každá technická verze ukládá technická data, která jsou specifická pro tuto verzi. Následuje několik příkladů těchto dat:

- Číslo verze a číslo předchozí verze (je-li k dispozici)
- Data účinnosti od a účinnosti do
- Aktivní stav verze produktu, který označuje, zda lze verzi uvolnit a použít v transakcích (Další informace viz [Připravenost produktu](product-readiness.md).)
- Technická společnost, která produkt vytvořila a vlastní (Další informace viz [Technické společnosti a pravidla vlastnictví dat](engineering-org-data-ownership-rules.md) .)
- Související technické dokumenty, jako je montážní příručka, uživatelské pokyny, obrázky a odkazy
- Technické atributy (Další informace viz [Technické atributy a vyhledávání technických atributů](engineering-attributes-and-search.md) .)
- Kusovník (BOM) pro strojírenské výrobky
- Vzorce pro produkty výrobního procesu
- Technické postupy

Tato data můžete aktualizovat na existující verzi nebo vytvořit novou verzi pomocí *příkazu k technické změně*. (Další informace viz [Správa změn technických produktů](engineering-change-management.md).) Pokud vytvoříte novou verzi produktu, systém zkopíruje všechna technická data do této nové verze. Poté můžete upravit data pro tuto novou verzi. Tímto způsobem můžete sledovat konkrétní data pro každou následující verzi. Chcete-li porovnat rozdíly mezi po sobě následujícími technickými verzemi, zkontrolujte příkaz k technické změně, který zahrnuje typy změn označují všechny změny.

Jak již bylo uvedeno, počáteční technická verze se vytvoří automaticky při vytváření technického produktu. Číslo verze pro tuto verzi se řídí pravidlem pro číslo verze, které je definováno v technické kategorii produktu. Chcete-li přejít na následující verzi, musíte produkt přidat do příkazu k technické změně jako řádek a musíte nastavit pole **Dopad** na možnost *Nová verze*. Příkaz k technické změně bude obsahovat podrobnosti o změně z aktuální verze na další verzi.

Upozorňujeme, že technický produkt může být najednou pouze v jednom příkazu k technické změně. Toto omezení zajišťuje přesnost dat a pomáhá se vyhnout překrývajícím se nebo protichůdným změnám v produktu. Všimněte si také, že pole **Technik** v zobrazení **Záhlaví** příkazu k technické změně zobrazuje technika, který je za příkaz ke změně odpovědný. Pokud technik patří k týmu, který je definován v systému, v poli **Odpovědný** je uveden vedoucí týmu.

## <a name="track-versions-in-transactions"></a>Sledování verzí v transakcích

Když používáte správu technických změn, vaše hlavní data produktu vždy obsahují jednu nebo více technických verzí. V nastavení technických produktů si můžete vybrat, zda je technická verze také součástí *logistické transakce*. (Další informace viz [Nastavení kategorií technických produktů](#product-category) dále v tomto článku.) Pokud je logistický dopad relevantní, liší se podle produktu a společnosti. Někdy se používá pouze nejnovější verze produktu. Proto při zavedení nové verze již nelze použít předchozí verzi. V ostatních případech je předchozí verze vyžadována v logistických transakcích k překonání následujících výzev:

- Logistické oddělení musí zákazníkovi odeslat dva kusy produktu. V tomto případě se musíte rozhodnout, zda chcete nebo dovolíte odeslat dvě různé verze.
- Později se zjistilo, že nastal problém a že souvisí s konkrétní změnou. V tomto případě by mohlo být výhodné přesně určit, která verze byla v každé objednávce dodána.
- Společnosti obvykle chtějí nejprve odeslat staré verze, aby je vyřadily ze zásob. Zejména u maloobjemových produktů lze tento přístup často řídit určením dat účinnosti nové verze ve vztahu k předpovědím o tom, kdy bude vyčerpána zásoba staré verze. Někdy však nebudete moci provést toto srovnání, nebo můžete považovat nejistotu předpovědí úrovně zásob za příliš vysokou.

Rozhodnutí o tom, zda zviditelnit verze v zásobách, závisí na faktorech, jako jsou ty, které již byly zmíněny, plus na obvyklé praxi společnosti a dalších aspektech, které jsou specifické pro každou společnost. Můžete určit chování pro *kategorie technických produktů*. Poté bude platit pro všechny produkty, které jsou vytvořeny z této kategorie, pro všechny společnosti, kterým je produkt vydán.

U produktů, které jsou nastaveny tak, aby měly logistický dopad, musí být u každé transakce uvedena technická verze. Ačkoli systém navrhne *nejnovější aktivní verzi*, můžete si vybrat ze všech aktivních verzí, které jsou pro společnost k dispozici. U produktů, které jsou nastaveny tak, aby neměly logistický dopad, není u transakcí uvedena technická verze. Systém však používá nejnovější aktivní verzi. Například když přidáte produkt do produkčního kusovníku, použije se nejnovější verze a při spuštění hlavního plánování se předpokládá nejnovější verze.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Nastavení kategorií technických produktů

Kategorie technického produktu poskytuje základ pro vytvoření konkrétního technického produktu. Každá kategorie stanoví sadu výchozích hodnot a zásad. Proto při vytváření technického produktu nejprve vyberete kategorii, ze které ho chcete vytvořit.

Všimněte si, že nový typ hierarchie kategorií (*hierarchie technických produktů*) se automaticky nastaví za vás. Kategorie můžete vytvořit ručně tak, že přejdete na **Správa technických změn \> Nastavit \> Podrobnosti kategorie technického produktu**.

Každá kategorie technických produktů stanoví výchozí chování technických produktů, které jsou vytvořeny na základě dané kategorie. Jakmile vytvoříte technických produkt, nemůžete změnit jeho kategorii technického produktu. Pokud však vyberete nesprávnou kategorii, můžete produkt odstranit a poté jej znovu vytvořit.

Když se vytvoří kategorie technického produktu, nebudete moci změnit následující nastavení:

- Technická společnost
- Typ produktu
- Podtyp produktu
- Skupina dimenzí produktů
- Technologie konfigurace
- Pravidlo čísla verze

Jiná nastavení mohou zdědit výchozí hodnoty, které jsou nastaveny pro kategorii technického produktu. Podle systémových pravidel však lze tyto hodnoty změnit.

Chcete-li pracovat s kategoriemi technického produktu, přejděte na **Správa technických změn \> Nastavit \> Podrobnosti kategorie technického produktu**. Potom proveďte jeden z následujících kroků.

- Chcete-li vytvořit novou kategorii, vyberte **Nová** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li upravit existující kategorii, vyberte ji v podokně seznamu, zvolte **Upravit** v podokně akcí a poté nastavte pole, jak je popsáno v následujících podsekcích.
- Chcete-li odstranit existující kategorii, vyberte ji v podokně seznamu a poté vyberte **Odstranit** v podokně akcí.

### <a name="header"></a>Záhlaví

V záhlaví kategorie technického produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Jméno | Zadejte název kategorie technického produktu. |
| Technická společnost | Vyberte technickou společnost, kde lze produkty v této kategorii technických produktů vytvářet a kde se budou udržovat. |

### <a name="details-fasttab"></a>Záložka s náhledem Podrobnosti

Na záložce s náhledem **Podrobnosti** kategorie technického produktu nastavte následující pole.

| Pole | popis |
|---|---|
| Typ produktu | Vyberte, zda se kategorie vztahuje na produkty nebo služby. |
| Typ výroby | Toto pole se zobrazí, pouze pokud jste povolili [řízení změn receptur](manage-formula-changes.md) ve vašem systému. Vyberte typ výroby, pro který platí tato kategorie strojírenských produktů:<ul><li>**Položka plánování** - Pomocí této technické kategorie můžete provádět správu změn vzorců pro položky plánování. Položky plánování používají receptury. Podobají se položkám receptur, ale používají se k výrobě pouze souběžných produktů a vedlejších produktů, nikoli hotových produktů. Vzorce se používají při výrobním procesu.</li><li>**Kusovník** - Tuto kategorii strojírenství použijte ke správě strojírenských produktů, které nepoužívají vzorce a obvykle (ale nemusí) zahrnovat kusovníky.</li><li>**Vzorec** - Pomocí této technické kategorie můžete provádět správu změn vzorců pro dokončené produkty. Tyto položky budou mít recepturu, ale nikoli kusovník. Vzorce se používají při výrobním procesu.</li></ul> |
| Skutečná hmotnost | Tato možnost se zobrazí, pouze pokud jste povolili [řízení změn vzorců](manage-formula-changes.md) ve vašem systému. Je k dispozici pouze v případě, že je pole **Typ výroby** nastaveno na *Položka plánování* nebo *Vzorec*. Tuto možnost nastavte na *Ano*, pokud tuto strojírenskou kategorii použijete ke správě položek, které vyžadují podporu hmotnosti. |
| Sledování verzí v transakcích | Vyberte, zda má být verze produktu vyznačena u všech transakcí (logistický dopad). Pokud například sledujete verzi v transakcích, každá prodejní objednávka zobrazí, která konkrétní verze produktu byla v dané prodejní objednávce prodána. Pokud nesledujete verzi v transakcích, prodejní objednávky nezobrazí, která konkrétní verze byla prodána. Místo toho vždy zobrazují nejnovější verzi.<ul><li>Pokud je tato možnost nastavena na *Ano*, je pro produkt vytvořen základní produkt a každá verze produktu bude variantou, která používá dimenzi produktu *verze*. Pole **Podtyp produktu** je automaticky nastaveno na *Základní produkt* v poli **Skupina dimenze produktu** a musíte vybrat skupinu dimenzí produktu, kde je dimenze *verze* je aktivní. Zobrazí se pouze skupiny dimenzí produktů, kde *verze* je aktivní dimenzí. Nové skupiny dimenzí produktů můžete vytvořit výběrem tlačítka **Upravit** (symbol tužky).</li><li>Pokud je tato možnost nastavena na *Ne*, dimenze produktu *verze* nebude použita. Poté můžete vybrat, zda chcete vytvořit produkt nebo základní produkt, který používá ostatní dimenze.</li></ul><p>Tato možnost se často používá u produktů, které mají rozdíl nákladů mezi verzemi, nebo u produktů, kde platí různé podmínky ve vztahu k zákazníkovi. Proto je důležité určit, která verze byla použita v každé transakci.</p> |
| Podtyp produktu | Vyberte, zda bude kategorie obsahovat produkty nebo základní produkty. U hlavních produktů se použijí dimenze produktu.
| Skupina dimenzí produktů | Nastavení **Sledování verzí v transakcích** vám pomůže vybrat skupinu dimenze produktu. Pokud jste určili, že chcete sledovat verzi v transakcích, zobrazí se skupiny dimenzí produktu, kde *verze* se používá dimenze. V opačném případě se zobrazí pouze skupiny dimenzí produktů, kde dimenze *verze* se nepoužívá. |
| Stav životního cyklu produktu při vytvoření | Nastavte výchozí stav životního cyklu produktu, který by měl mít technický produkt při prvním vytvoření. Další informace viz [Stavy životního cyklu produktu a transakce](product-lifecycle-state-transactions.md). |
| Pravidlo čísla verze | Vyberte pravidlo čísla verze, které se vztahuje na kategorii:<ul><li>**Manuální** - Pro každou novou verzi vyberete číslo verze.</li><li>**Automatické** - Systém nastaví číslo verze na základě formátu, který definujete. Při nastavování formátu použijte znak čísla (\#), který představuje číslici, a jakýkoli jiný znak představující konstantní hodnotu. Například pokud definujete formát jako *V-\#\#*, první verze bude „V-01“, druhá verze bude „V-02“ atd.</li><li>**Seznam** - Systém vezme další číslo z předdefinovaného seznamu vlastních hodnot, které definujete.</li></ul> |
| Vynutit platnost | Vyberte, zda musí být data účinnosti technických verzí souvislá, nebo zda mohou existovat mezery a překrývání. Toto nastavení ovlivňuje způsob, jakým můžete používat pole **Platné od** a **Platné do** pro každou technickou verzi, kde platí kategorie.<ul><li>Pokud je tato možnost nastavena na *Ano*, hodnota **Platí od** pro každou verzi musí být zadána a mezi verzemi nejsou povoleny překryvy ani mezery. Datový rozsah pro každou technickou verzi je spojeno přímo s předchozí a další technickou verzí, pokud existují. V tomto scénáři se vždy používá nejnovější verze a starší verze se již nepoužívají.</li><li>Pokud je tato možnost nastavena na **Ne**, neexistují žádná omezení v polích data účinnosti u technických verzí a jsou povolena překrývání i mezery. V tomto scénáři může být aktivních více verzí současně a můžete pracovat s jakoukoli aktivní verzí.</li></ul><p>Tato možnost také ovlivní kusovníky a postupy, které jsou připojeny k verzi produktu. Další informace viz [Připojení kusovníků a postupů k technickým verzím](#boms-routes) dále v tomto článku.</p> |
| Použít názvosloví pravidla čísla | Tuto možnost nastavte na *Ano*, čímž povolíte pravidla pro definování čísla produktu pomocí číselných řad, názvů a hodnot technických atributů a textových konstant jako segmentů. Chcete-li vytvořit nebo upravit pravidla, vyberte tlačítko **Upravit**. |
| Použít názvosloví pravidla názvu | Tuto možnost nastavte na *Ano*, čímž povolíte pravidla pro definování názvu pomocí názvů technických atributů, hodnot technických atributů a textových konstant jako segmentů. Chcete-li vytvořit nebo upravit pravidla, vyberte tlačítko **Upravit**. |
| Použít názvosloví pravidla popisu | Tuto možnost nastavte na *Ano*, čímž povolíte pravidla pro definování popisu pomocí názvů technických atributů, hodnot technických atributů a textových konstant jako segmentů. Chcete-li vytvořit nebo upravit pravidla, vyberte tlačítko **Upravit**. |

### <a name="attributes-fasttab"></a>Záložka s náhledem Atributy

Použijte mřížku na záložce s náhledem **Atributy** pro nastavení technických atributů, které se vztahují na produkty patřící do této kategorie. Další informace o vytvoření technických atributů získáte v části [Technické atributy a vyhledávání technických atributů](engineering-attributes-and-search.md).

Použijte tlačítka na záložce s náhledem **Atributy** pro přidání, odebrání a uspořádání atributů v mřížce.

Pokud změníte výběr atributů pro technickou kategorii a již existují produkty založené na dané kategorii, musíte se rozhodnout, zda u těchto produktů použijete změny. Pokud chcete, aby existující produkty odrážely změny, vyberte možnost **Aktualizovat stávající produkty** na záložce s náhledem **Atributy**.

Pro každý řádek, který přidáte do mřížky, nastavte následující pole.

| Pole | popis |
|---|---|
| Jméno | Vyberte atributy, které chcete přidat. |
| Hodnota | Vyberte výchozí hodnotu pro atribut. |
| Povinné | Vyberte, zda je atribut povinný, což znamená, že uživatelé musí před uložením produktu zadat platnou hodnotu atributu. Účinek tohoto nastavení se mírně liší v závislosti na typu dat vybraného atributu, jak je definováno v následujícím seznamu.<ul><li>**Logický** – Nastavte na *Ano*, chcete-li vyžadovat, aby měl atribut hodnotu *Ano* (systém odmítne uložit produkt, kde je atribut nastaven na *Ne*). Tuto možnost nastavte na *Ne*, abyste mohli přijmout *Ano* i *Ne*. (Atributy typu *Logický* nemohou mít prázdnou hodnotu.)</li><li>**Celé číslo nebo Desetinné číslo** – Nastavte na *Ano*, chcete-li požadovat po uživatelích zadání nenulové hodnoty tohoto atributu. Tuto možnost nastavte na *Ne*, abyste uživatelům umožnili ukládat s nulovou hodnotou.  (Atributy těchto typů nemohou mít prázdnou hodnotu.)</li><li>**Seznam** – Seznamy mají datový typ *Text*, ale také obsahují předdefinovaný seznam možných hodnot. U atributů tohoto typu tedy není možné zadat prázdnou hodnotu, takže toto nastavení nemá žádný vliv a je pouze informativní.</li><li>**Všechny ostatní datové typy** – Nastavte toto na *Ano*, aby byl atribut povinný. Nastavte na *Ne*, aby uživatelé mohli uložit produkt bez zadání hodnoty tohoto atributu.</li></ul> |
| Atribut dávky | Vyberte, zda se má atribut rozšířit prostřednictvím dávkové funkce. |

### <a name="readiness-policy-fasttab"></a>Záložka s náhledem Zásady připravenosti

Použijte pole **Zásady připravenosti produktu** a vyberte zásadu připravenosti, která by se měly vztahovat na produkty, které jsou vytvářeny na základě strojírenské kategorie. Další informace naleznete v tématu [Připravenost produktu](product-readiness.md).

> [!NOTE]
> Pole **Zásady připravenosti produktu** funguje trochu jinak, pokud jste zapnuli funkci *Kontroly připravenosti produktu* ve vašem systému. (Tato funkce umožňuje použít zásady připravenosti na standardní \[nestrojírenské\] produkty). Další informace viz [Přiřaďte zásady připravenosti standardním a strojírenským produktům](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Záložka s náhledem Zásady uvolnění

Použijte pole **Zásady uvolnění produktu** a vyberte zásadu uvolnění, která se vztahuje na produkty patřící do této kategorie. Další informace naleznete v tématu [Vydání struktur produktu](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Připojení kusovníků a postupů k technickým verzím

Nastavení možnosti **Vynutit platnost** je důležité pro připojení kusovníků a postupů ke každé technické verzi. Můžete aktivovat více kusovníků nebo postupů pro každý produkt pouze tehdy, když se liší v některém z následujících nastavení:

- Dimenze produktu
- Množství
- Lokalita
- Data platnosti

Technické kusovníky a postupy se vytvářejí z technické verze, kde platí. Poznají se podle značky zaškrtnutí v zaškrtávacím políčku **Technická kontrola**. Když pracujete s technickými kusovníky a postupy, obvykle je nebudete navrhovat pomocí různých množství. Obvykle také nebudete navrhovat různé kusovníky podle pracoviště. Navíc pro technické kusovníky a postupy jsou data účinnosti vždy převzata z technické verze. Proto budou mít technická verze, její kusovník a její postup stejná data účinnosti.

U produktů, kde používáte dimenze produktu *verze* (spolu s logistickým dopadem na transakce), je verze také přidána do kusovníků a postupů. Toto chování pomáhá odlišit kusovníky a postupy po sobě jdoucích verzí, bez ohledu na nastavení **Vynutit platnost**.

U produktů, kde nepoužíváte dimenze produktu *verze* (bez logistického dopadu na transakce), není verze přidána do kusovníků nebo postupů. Proto nebude mezi kusovníky a postupy po sobě jdoucích verzí žádný rozdíl. V tomto případě důrazně doporučujeme nastavit možnost **Vynutit platnost** na *Ano*. Tímto způsobem pomůžete zabránit tomu, aby se technické verze překrývaly, a můžete také aktivovat kusovník a postup novější verze, aniž byste nejprve museli deaktivovat kusovník a postup předchozí verze. Pokud v tomto případě nastavíte možnost **Nastavit platnost** na *Ano*, musíte ručně deaktivovat kusovníky a postupy starších verzí, než budete moci aktivovat nejnovější verzi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
