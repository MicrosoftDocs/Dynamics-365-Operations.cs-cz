---
title: Operace odchozích zásob v POS
description: Tento článek popisuje možnosti odchozí skladové operace v pokladním místě (POS).
author: hhaines
ms.date: 07/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: dd2c124660643628ca4c19dc3a49366b67f29ad3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850216"
---
# <a name="outbound-inventory-operation-in-pos"></a>Operace odchozích zásob v POS

[!include [banner](includes/banner.md)]


V Microsoft Dynamics 365 Commerce verze 10.0.10 a novějších nahrazují příchozí a odchozí operace v pokladním místě (POS) operace výdeje a příjmu.

> [!NOTE]
> Ve verzi 10.0.10 a novějších budou jakékoli nové funkce aplikace POS související s příjmem skladových zásob podle nákupních objednávek a převodních příkazů přidány do příchozí operace. Pokud právě používáte operace výdeje a příjmu v aplikaci POS, doporučujeme, abyste vytvořili strategii pro přechod od těchto operací k novým příchozím a odchozím operacím. Ačkoli operace výdeje a příjmu nebudou z produktu odebrány, po verzi 10.0.9 do nich nebude nic investováno z hlediska funkčního nebo výkonnostního výhledu.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Předpoklad: Konfigurace asynchronní architektury dokumentu

Odchozí operace zahrnuje zlepšení výkonu, aby se zajistilo, že uživatelé, kteří mají velké objemy zaúčtování příjmů v mnoha obchodech nebo společnostech a velké skladové dokumenty, mohou tyto dokumenty zpracovat do centrály Commerce, aniž by došlo k překročení časových limitů nebo selhání. Tato zlepšení vyžadují použití asynchronní architektury dokumentu.

Při použití asynchronní architektury dokumentu můžete potvrdit změny odchozích dokumentů z POS do centrály Commerce a poté se věnovat jiným úkolům, zatímco na pozadí probíhá zpracování do centrály Commerce (HQ). Můžete zkontrolovat stav dokumentu pomocí stránky seznamu dokumentů **Odchozí operace** v POS, abyste se ujistili, že zaúčtování bylo úspěšné. V aplikaci POS můžete také pomocí aktivního seznamu dokumentů odchozí operace zobrazit všechny dokumenty, které nelze zaúčtovat do centrály Commerce (HQ). Pokud dokument selže, uživatelé POS jej mohou opravit a poté opakovat zpracování do centrály Commerce (HQ).

> [!IMPORTANT]
> Asynchronní architektura dokumentu musí být nakonfigurována předtím, než se společnost pokusí použít odchozí operaci v POS.

Chcete-li konfigurovat asynchronní architekturu dokumentu, postupujte podle následujících pokynů.

### <a name="create-and-configure-a-number-sequence"></a>Vytvoření a konfigurace číselné řady

1. Přejděte na **Správa organizace \> Číselné řady \> Číselné řady**.
2. Na stránce **Číselné řady** vytvořte číselnou řadu.
3. V polích **Kód číselné řady** a **Název** zadejte hodnoty definované uživatelem.
4. Na pevné záložce **Odkazy** vyberte **Přidat**.
5. V poli **Oblast** vyberte možnost **Parametry Commerce**.
6. V poli **Odkaz** vyberte možnost **Identifikátoroperace maloobchodního dokladu**.
7. Na pevé záložce **Obecné** v sekci **Nastavení** nastavte možnost **Souvislé** na hodnotu **Ne**, aby se předešlo jakýmkoli problémům s výkonem.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Vytvoření a naplánování dvou dávkových úloh pro zpracování a sledování dokumentů

> [!NOTE]
> V Commerce verze 10.0.13 a novějších nemusíte dávkové úlohy konfigurovat prostřednictvím rámce dávkových úloh. Dávkové procesy lze konfigurovat z nabídky **Retail a Commerce > IT pro Retail a Commerce**. Ke konfiguraci dávkových úloh použijte možnosti nabídky **Sledování operace maloobchodního dokumentu** a **Zpracování operace maloobchodního dokumentu**

Dávkové úlohy, které vytvoříte, budou použity ke zpracování dokumentů, které selhaly nebo jejichž časový limit vypršel. Použijí se také v případě, že počet aktivních skladových dokladů, které jsou zpracovávány z POS, přesahuje hodnotu konfigurovanou systémem.

1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy**.
2. Na stránce **Dávková úloha** vytvořte dvě dávkové úlohy:

    - Nakonfigurujte jednu úlohu pro spuštění třídy **RetailDocumentOperationMonitorBatch**.
    - Nakonfigurujte další úlohu pro spuštění třídy **RetailDocumentOperationProcessingBatch**.

3. Naplánujte nové dávkové úlohy, aby se opakovaně spouštěly. Nastavte například plán tak, aby byly úlohy spouštěny každých pět minut.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Předpoklad: Přidání odchozí operace do rozvržení obrazovky POS

Aby mohla vaše organizace používat funkci odchozí operace, musí v POS konfigurovat **odchozí operaci** v jednom nebo více [rozloženích obrazovky POS](/dynamics365/unified-operations/retail/pos-screen-layouts). Před nasazením nové operace v provozním prostředí se ujistěte, že jste ji důkladně otestovali a svoje uživatele vyškolili k jejímu používání.

## <a name="overview"></a>Přehled

Odchozí operace umožňuje uživateli POS provádět následující úlohy:

- Zaúčtovat dodávky pro dokumenty převodního příkazu v případech, kdy je obchodem uživatele určený odchozí sklad.
- Zobrazit informace o historických dodávkách převodních příkazů, které byly zaúčtovány obchodem.
- Vytvářet nové požadavky na odchozí převodní příkazy.

Při spuštění odchozí operace z aplikace POS se zobrazí stránka seznamu. Toto zobrazení obsahuje otevřené dokumenty převodních příkazů s řádky zásob, které má expedovat a plnit aktuální obchod uživatele. Chcete-li najít a vybrat dokument, můžete seznam posunout nebo použít funkci vyhledávání.

Seznam dokumentů odchozích zásob obsahuje tři karty.

- **Aktivní** – na této kartě jsou zobrazeny převodní příkazy, které mají stav **Požadováno** nebo **Částečně expedováno**. Příkazy obsahují řádky nebo množství na řádcích, které musí být expedovány aktuálním obchodem uživatele. Na této kartě jsou zobrazeny také objednávky ve stavu **Zpracování v HQ** (to znamená, že čekají na potvrzení úspěšného zaúčtování z centrály Commerce (HQ)) nebo **Zpracování selhalo** (to znamená, že zaúčtování do centrály Commerce (HQ) bylo neúspěšné a uživatel musí data opravit a pokusit se znovu odeslat příkazy).
- **Koncept** – Tato karta zobrazuje nové požadavky na odchozí převodní příkazy, které byly vytvořeny v obchodě uživatele. Dokumenty však jsou uloženy pouze místně. Dosud nebyly odeslány do centrály Commerce (HQ) ke zpracování.
- **Dokončeno** – Na této kartě je zobrazen seznam dokumentů převodních příkazů, které obchod plně expedoval během posledních sedmi dnů. Tato karta je určena pouze pro informaci. Všechny informace o dokumentech jsou pro daný obchod určeny pouze pro čtení.

Při zobrazení dokumentů na kterékoli z těchto karet vám pole **Stav** může pomoci pochopit fázi, ve které se dokument nachází.

- **Koncept** – dokument převodního příkazu byl uložen pouze místně do databáze kanálů obchodu. Do centrály Commerce (HQ) nebyly odeslány žádné informace o požadavku na převodní příkaz.
- **Požadováno** – Nákupní objednávka nebo převodní příkaz byly vytvořeny v Commerce Headquarters (HQ) a jsou plně otevřené. Aktuální obchod uživatele dosud zpracoval všechny dodávky v rámci dokumentu.
- **Částečně expedováno** – doklad převodního příkazu má jeden nebo více řádků množství nebo částečného množství, které byly zaúčtovány jako expedované výstupním skladem. Tyto expedované řádky jsou dostupné k přijetí prostřednictvím příchozí operace.
- **Expedováno v plném rozsahu** – všechny řádky a celá množství na řádcích převodního příkazu byly zaúčtovány jako expedované výstupním skladem.
- **Probíhá** – tento stav slouží k informování uživatelů zařízení o tom, že dokument aktivně zpracovává jiný uživatel.
- **Pozastaveno** – tento stav se zobrazí po zaškrtnutí políčka **Pozastavit příjem** pro dočasné zastavení procesu příjmu.
- **Zpracování v HQ** – dokument byl odeslán do centrály Commerce (HQ) z aplikace POS, ale dosud nebyl úspěšně zaúčtován do centrály Commerce (HQ). Dokument prochází procesem asynchronního zaúčtování dokumentů. Po úspěšném zaúčtování dokumentu do centrály Commerce (HQ) by měl být jeho stav aktualizován na **Plně přijato** nebo **Částečně přijato**.
- **Zpracování selhalo** – dokument byl zaúčtován do centrály Commerce (HQ) a odmítnut. V podokně **Podrobnosti** se zobrazuje důvod selhání zaúčtování. Chcete-li opravit problémy s daty, je nutné upravit dokument a poté jej znovu odeslat do centrály Commerce (HQ) ke zpracování.

Pokud vyberete řádek dokumentu v seznamu, zobrazí se podokno **Podrobnosti**. V tomto podokně jsou zobrazeny další informace o daném dokumentu, například informace o dodávce a datu. Indikátor průběhu ukazuje, kolik položek musí být ještě zpracováno. Pokud dokument nebyl úspěšně zpracován do centrály Commerce (HQ), zobrazí se v podokně **Podrobnosti** také chybové zprávy související s chybou.

Chcete-li zobrazit podrobnosti dokumentu, můžete v zobrazení stránky se seznamem dokumentů vybrat **Podrobnosti objednávky** na panelu aplikací. Zpracování příjmu lze rovněž aktivovat na vhodných řádcích dokladu.

V zobrazení stránky se seznamem dokumentů lze rovněž vytvořit nový odchozí převodní příkaz pro obchod.

## <a name="transfer-order-shipping-process"></a>Proces expedice převodního příkazu

Po výběru dokumentu převodního příkazu na kartě **Aktivní** můžete vybrat **Podrobnosti objednávky** a zahájit tak proces plnění. Zobrazí se **Úplný seznam objednávek**. Na této stránce jsou zobrazeny všechny řádky dokumentu, které tuto položku obsahují. Dále jsou zde uvedeny podrobnosti objednaného množství.

Každé skenování čárového kódu aktualizuje množství v poli **Probíhá expedice** o jednu jednotku. Expedované množství můžete také zadat výběrem možnosti **Dodat produkt** na panelu aplikací, zadáním ID položky a zadáním množství. Je-li položka řízena dle umístění, můžete potvrdit nebo nastavit místo expedice pro řádek dokumentu.

V zobrazení **Úplný seznam objednávek** můžete ručně vybrat řádek v seznamu a poté aktualizovat množství **Probíhá expedice** pro vybraný řádek v podokně **Podrobnosti**.

### <a name="over-delivery-shipping-validations"></a>Ověření nadměrné dodávky

Během procesu plnění pro řádky dokumentu dochází k jejich ověření. To zahrnuje ověření pro navýšení dodávky. Pokud se uživatel pokusí expedovat více zásob, než bylo objednáno na převodním příkazu, ale buď není konfigurována nadměrná dodávka, nebo expedované množství překračuje toleranci nadměrné dodávky, která je konfigurována pro řádek převodního příkazu, obdrží uživatel chybu a není povoleno expedovat nadměrné množství.

### <a name="underdelivery-close-lines"></a>Snížení dodávky pro uzavřené řádky

V Commerce verzi 10.0.12 byla přidána funkce, která umožňuje uživatelům POS uzavřít nebo zrušit zbývající množství během odeslání odchozí objednávky, pokud odchozí sklad zjistí, že nemůže odeslat celé požadované množství. Množství lze také uzavřít nebo zrušit později. Aby bylo možné tuto funkci využívat, musí být společnost nakonfigurována tak, aby umožňovala doručování snížených dodávek převodních příkazů. Kromě toho musí být pro řádek objednávky převodu definováno procento nedoručení.

Chcete-li společnost nakonfigurovat tak, aby umožňovala doručování převodních příkazů pro snížené dodávky, přejděte v centrále Commerce (HQ) na **Řízení zásob \> Založit \> Parametry řízení zásob a skladu**. Na stránce **Parametry řízení zásob a skladu**, v kartě **Převod objednávek**, zapněte **Přijmout doručení snížení dodávek** parametr. Pak spusťte **1070** úloha plánovače distribuce pro synchronizaci změn parametrů s kanálem obchodu.

Procenta doručení snížených dodávek pro řádek objednávky lze předdefinovat u produktů jako součást konfigurace produktu v Commerce Headquarters. Alternativně mohou být nastaveny nebo přepsány na konkrétní řádce převodu přes centrálu Commerce (HQ).

Poté, co organizace dokončí konfiguraci příkazu edpedice pro snížené objednávky, uvidí uživatelé POS novou možnost **Zavřete zbývající množství** v **Podrobnostech**, když vyberou řádek odchozích přenosů přes funkci **Odchozí operace** v POS. Poté, co uživatel dokončí zásilku pomocí **Dokončení plnění** operace, mohou poslat požadavek do centrály Commerce (HQ) ke zrušení zbývajícího nevybaveného množství. Pokud uživatel uzavře zbývající množství, Commerce provede ověření, aby ověřila, že množství, které je zrušeno, je v rámci procentuální tolerance podlimitu, který je definován na řádku objednávky přenosu. Je-li tolerance překročení dodávky překročena, uživatel obdrží chybovou zprávu a nebude moci zbývající množství uzavřít, dokud dříve dodané množství a množství „expedovat nyní“ nesplní nebo nepřekročí toleranci doručení snížené dodávky.

Poté, co je zásilka synchronizována v centrále Commerce (HQ), množství, která jsou definována v **Expedovat nyní** poli pro řádek objednávky převodu v POS jsou aktualizovány na stav odeslání definovaném v centrále Commerce (HQ). Veškerá neexpedovaná množství, která by dříve byla považována za „zbývající expedice“, tj. množství, která budou dodána později, se místo toho považují za zrušená množství. "Zbývající expedice" pro řádek převodního příkazu je nastaveno na **0** (nula) a řádek je považován za plně dodaný.

### <a name="shipping-location-controlled-items"></a>Expedice položek na základě umístění

Pokud jsou položky expedovány na základě umístění, mohou uživatelé zvolit umístění, kam chtějí zásoby vydat během procesu expedice. Doporučujeme nakonfigurovat výchozí místo výdeje na sklad obchodu, aby byl tento proces efektivnější. I v případě, že je nakonfigurováno výchozí umístění, mohou uživatelé přepsat místo výdeje na vybraných řádcích, jak potřebují.

Operace ctí konfiguraci **Povolen prázdný příjem** v dimenzi úložiště **Umístění** a nevyžaduje, aby byla zadána dimenze umístění, pokud je konfigurován prázdný příjem. Nejsou-li pro položku povolena prázdná místa příjmu, aplikace POS zobrazí chybu a vyžaduje zadání umístění před tím, než bude možné zaúčtovat příjem.

### <a name="ship-all"></a>Odeslat vše

Podle potřeby můžete výběrem možnosti **Odeslat vše** na panelu aplikací rychle aktualizovat množství pole **Probíhá expedice** pro všechny řádky dokumentu na maximální hodnotu, která je k dispozici pro plnění pro tyto řádky.

### <a name="cancel-fulfillment"></a>Zrušit plnění

Funkci **Zrušit plnění** na panelu aplikací použijte pouze v případě, že chcete odejít z dokumentu a nechcete uložit žádné změny. Původně jste například vybrali nesprávný dokument a nechcete, aby byla uložena předchozí data expedice.

### <a name="pause-fulfillment"></a>Pozastavit plnění

Pokud plníte převodní příkaz, můžete použít funkci **Pozastavit plnění**, pokud chcete pozastavit tento proces. Můžete například chtít provést další operaci z POS, jako například zavolat na oddělení prodeje zákazníkům nebo zpozdit zaúčtování expedice do centrály Commerce (HQ).

Pokud vyberete možnost **Pozastavit plnění**, bude stav dokumentu změněn na **Pozastaveno**. Uživatel proto bude vědět, že byla zadána data v daném dokumentu, ale dokument ještě nebyl potvrzen. Až budete připraveni pokračovat v procesu plnění, vyberte pozastavený dokument a pak vyberte **Podrobnosti objednávky**. Všechna dříve uložená množství **Probíhá expedice** budou zachována a lze je zobrazit ze zobrazení **Úplný seznam objednávek**.

### <a name="review"></a>Přehled

Před konečným potvrzením o plnění v centrále Commerce (HQ) můžete pomocí funkce **Kontrola** ověřit odchozí dokument. Tato funkce vás upozorní na chybějící nebo nesprávná data, která mohou způsobit selhání zpracování, a poskytne vám možnost opravit problémy před odesláním žádosti o potvrzení. Chcete-li povolit funkci **Recenze** na panelu aplikací, povolte funkci **Povolit ověření v příchozích a odchozích skladových operacích** POS prostřednictvím pracovního prostoru Správa funkcí v centrále Commerce (HQ).

Funkce **Recenze** ověřuje následující problémy v odchozím dokumentu:
- **Nadměrný příjem** - nyní přijímané množství je větší než objednané množství. Závažnost tohoto problému je dána konfigurací navýšení dodávky v centrále Commerce (HQ).
- **Nedostatečný příjem** - nyní přijímané množství je menší než objednané množství. Závažnost tohoto problému je dána konfigurací snížení dodávky v centrále Commerce (HQ).
- **Sériové číslo** - sériové číslo není poskytnuto ani dostupné pro serializovanou položku, která vyžaduje, aby bylo sériové číslo zapsáno do zásob.
- **Místo není nastaveno** - místo není určeno pro položku na základě polohy, kde není povoleno prázdné místo.
- **Odstraněné řádky** - v objednávce jsou odstraněny řádky uživatelem centrály Commerce (HQ), které nejsou POS aplikaci známy.

Nastavte parametr **Povolit automatické ověření** na **Ano** v **Parametry obchodu** > **Zásoby** > **Operace skladových zásob**, aby bylo ověření provedeno automaticky, když je vybrána volba **Dokončit plnění**.

### <a name="finish-fulfillment"></a>Dokončit plnění

Po dokončení zadávání všech množství **Probíhá expedice** je nutné vybrat možnost **Dokončit plnění** na panelu aplikací.

Při použití asynchronního zpracování dokumentu je příjem odeslán prostřednictvím asynchronní architektury dokumentu. Doba potřebná pro zaúčtování dokumentu závisí na velikosti dokumentu (počtu řádků) a na obecném provozu zpracování na serveru. Obvykle k tomuto zpracování dojde v průběhu několika sekund. Pokud se zaúčtování dokumentu nezdaří, bude uživatel upozorněn prostřednictvím seznamu dokumentů **Odchozí operace** na kartě **Aktivní**, kde se stav dokumentu aktualizuje na **Zpracování selhalo**. Uživatel pak může vybrat neúspěšný dokument v POS, aby zobrazil chybové zprávy a důvod selhání v podokně **Podrobnosti**. Neúspěšný dokument zůstane nezaúčtovaný a vyžaduje, aby se uživatel vrátil k řádkům dokumentu výběrem možnosti **Podrobnosti objednávky** v POS. Uživatel musí poté na základě chyb opravit dokument. Po opravě dokumentu se uživatel může pokusit jej znovu zpracovat výběrem možnosti **Dokončit plnění** na panelu aplikací.

## <a name="create-an-outbound-transfer-order"></a>Vytvoření odchozího převodního příkazu

V aplikaci POS mohou uživatelé vytvářet nové dokumenty převodních příkazů. Chcete-li zahájit proces, vyberte možnost **Nový** na panelu aplikací, zatímco se nacházíte v hlavním seznamu dokumentů **Odchozí operace**. Poté budete vyzváni k výběru skladu nebo obchodu pro možnost **Převést do**, do kterého váš aktuální obchod odešle zásoby. Hodnoty jsou omezeny na výběr, který je definován v konfiguraci skupiny plnění obchodu. V požadavku na odchozí převod bude váš aktuální obchod pro převodní příkaz vždy sklad **Převést z**. Tuto hodnotu nelze změnit.

V případě potřeby můžete zadat hodnoty do polí **Datum expedice**, **Datum příjmu** a **Způsob dodání**. Můžete také přidat poznámku, která bude uložena spolu se záhlavím převodního příkazu jako příloha dokumentu v centrále Commerce (HQ).

Po vytvoření informací v záhlaví můžete do převodního příkazu přidávat produkty. Chcete-li zahájit proces přidávání položek a požadovaných množství, skenujte čárové kódy nebo vyberte možnost **Přidat produkt**.

Po zadání řádků na odchozí převodní příkaz je nutné vybrat možnost **Uložit** pro uložení dokumentu v místním počítači nebo možnost **Odeslat požadavek** pro odeslání podrobností objednávky do centrály Commerce (HQ) za účelem dalšího zpracování. Pokud vyberete možnost **Uložit**, dokument konceptu je uložen v databázi kanálů a výstupní sklad nemůže dokument spustit, dokud není úspěšně zpracován prostřednictvím funkce **Odeslat požadavek**. Možnost **Uložit** vyberte pouze v případě, že nejste připraveni potvrdit zpracování požadavku v centrále Commerce (HQ).

Pokud je dokument uložen místně, lze jej najít na kartě **Koncepty** v seznamu dokumentů **Vstupní operace**. Když je dokument ve stavu **Koncept**, můžete jej upravit výběrem možnosti **Upravit**. Řádky můžete podle potřeby aktualizovat, přidávat nebo odstraňovat. Můžete také odstranit celý dokument, který je ve stavu **Koncept**, výběrem možnosti **Odstranit** na kartě **Koncepty**.

Po úspěšném odeslání dokumentu konceptu do centrály Commerce (HQ) se tento dokument zobrazí na kartě **Aktivní** ve stavu **Požadováno**. V tuto chvíli mohou dokument upravit pouze uživatelé v odchozím skladu výběrem možnosti **Odchozí operace** v aplikaci POS. Uživatelé ve vstupním skladu mohou zobrazit převodní příkaz na kartě **Aktivní** v seznamu dokumentů **Příchozí operace**, ale nemohou jej upravit ani odstranit. Zámek pro úpravy zajišťuje, že nedojde k žádnému konfliktu, kdyby příchozí žadatel změnil převodní příkaz současně s tím, když odchozí přepravce aktivně vyskladňuje a expeduje objednávku. Pokud jsou v příchozím obchodě nebo skladu vyžadovány změny po odeslání převodního příkazu, je třeba se spojit s odchozím přepravcem a požádat jej o zadání změn.

Jakmile je dokument ve stavu **Požadováno**, je připraven pro zpracování plnění výstupním skladem. Během zpracování expedice s použitím odchozí operace je stav dokumentů převodního příkazu aktualizován ze stavu **Požadováno** na **Expedováno v plném rozsahu** nebo **Částečně expedováno**. Jakmile jsou dokumenty ve stavu **Expedováno v plném rozsahu** nebo **Částečně expedováno**, může příchozí obchod nebo sklad podle nich účtovat příjemky pomocí procesu příjmu příchozí operace.

Plně expedované převodní příkazy jsou přesunuty na kartu **Dokončeno** v seznamu dokumentů **Odchozí operace**. Tam po sedm dní zůstanou v režimu pouze pro čtení viditelné uživatelům ve výstupním obchodu nebo skladu.

## <a name="related-articles"></a>Související články

[Operace příchozích zásob v POS](pos-inbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]