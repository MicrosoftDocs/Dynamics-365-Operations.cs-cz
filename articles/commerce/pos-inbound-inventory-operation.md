---
title: Příchozí skladová operace v POS
description: Toto téma popisuje možnosti příchozí skladové operace v pokladním místě (POS).
author: hhaines
manager: annbe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 16a786a4b3ca1bcbd202f6753bdf3bf7233a4333
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710302"
---
# <a name="inbound-inventory-operation-in-pos"></a>Příchozí skladová operace v POS

[!include [banner](includes/banner.md)]

V Microsoft Dynamics 365 Commerce verze 10.0.10 a novějších nahrazují příchozí a odchozí operace v pokladním místě (POS) operace výdeje a příjmu.

> [!NOTE]
> Ve verzi Commerce 10.0.10 a novějších budou jakékoli nové funkce aplikace POS související s příjmem skladových zásob podle nákupních objednávek a převodních příkazů přidány do operace POS **Příchozí operace**. Pokud právě používáte operace výdeje a příjmu v aplikaci POS, doporučujeme, abyste vytvořili strategii pro přechod od těchto operací k novým příchozím a odchozím operacím. Ačkoli operace výdeje a příjmu nebudou z produktu odebrány, po verzi 10.0.9 do nich nebude nic investováno z hlediska funkčního nebo výkonnostního výhledu.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Předpoklad: Konfigurace asynchronní architektury dokumentu

Příchozí operace zahrnuje zlepšení výkonu, aby se zajistilo, že uživatelé, kteří mají velké objemy zaúčtování příjmů v mnoha obchodech nebo společnostech a velké skladové dokumenty, mohou tyto dokumenty zpracovat do Commerce Headquarters, aniž by došlo k překročení časových limitů nebo selhání. Tato zlepšení vyžadují použití asynchronní architektury dokumentu.

Při použití asynchronní architektury dokumentu můžete potvrdit změny příchozích dokumentů z POS do Commerce Headquarters a poté se věnovat jiným úkolům, zatímco na pozadí probíhá zpracování do Commerce Headquarters. Můžete zkontrolovat stav dokumentu pomocí stránky seznamu dokumentů **Příchozí operace** v POS, abyste se ujistili, že zaúčtování bylo úspěšné. V aplikaci POS můžete také pomocí aktivního seznamu dokumentů příchozí operace zobrazit všechny dokumenty, které nelze zaúčtovat do Commerce Headquarters. Pokud dokument selže, uživatelé POS jej mohou opravit a poté opakovat zpracování do Commerce Headquarters.

> [!IMPORTANT]
> Asynchronní architektura dokumentu musí být nakonfigurována předtím, než se společnost pokusí použít příchozí operaci v POS.

Chcete-li konfigurovat asynchronní architekturu dokumentu, postupujte podle následujících pokynů.

### <a name="create-and-configure-a-number-sequence"></a>Vytvoření a konfigurace číselné řady

1. Přejděte na **Správa organizace \> Číselné řady \> Číselné řady**.
2. Na stránce **Číselné řady** vytvořte číselnou řadu.
3. V polích **Kód číselné řady** a **Název** zadejte hodnoty definované uživatelem.
4. Na pevné záložce **Odkazy** vyberte **Přidat**.
5. V poli **Oblast** vyberte možnost **Parametry Commerce**.
4. V poli **Odkaz** vyberte možnost **Identifikátoroperace maloobchodního dokladu**.
5. Na pevé záložce **Obecné** v sekci **Nastavení** nastavte možnost **Souvislé** na hodnotu **Ne**, aby se předešlo jakýmkoli problémům s výkonem.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Vytvoření a naplánování dvou dávkových úloh pro zpracování a sledování dokumentů

> [!NOTE]
> V Commerce verze 10.0.13 a novějších nemusíte tyto dávkové úlohy konfigurovat prostřednictvím rámce dávkových úloh. Dávkové procesy lze konfigurovat z nabídky **Retail a Commerce > IT pro Retail a Commerce**. Ke konfiguraci dávkových úloh použijte možnosti nabídky **Sledování operace maloobchodního dokumentu** a **Zpracování operace maloobchodního dokumentu**.

Dávkové úlohy, které vytvoříte, budou použity ke zpracování dokumentů, které selhaly nebo jejichž časový limit vypršel. Použijí se také v případě, že počet aktivních skladových dokladů, které jsou zpracovávány z POS, přesahuje hodnotu konfigurovanou systémem.

1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy**.
2. Na stránce **Dávková úloha** vytvořte dvě dávkové úlohy:

    - Nakonfigurujte jednu úlohu pro spuštění třídy **RetailDocumentOperationMonitorBatch**.
    - Nakonfigurujte další úlohu pro spuštění třídy **RetailDocumentOperationProcessingBatch**.

2. Naplánujte nové dávkové úlohy, aby se opakovaně spouštěly. Nastavte například plán tak, aby byly úlohy spouštěny každých pět minut.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Předpoklad: Přidání příchozí operace do rozvržení obrazovky POS

Aby mohla vaše organizace používat funkci příchozí operace, musí v POS konfigurovat **příchozí operaci** v jednom nebo více [rozloženích obrazovky POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Před nasazením nové operace v provozním prostředí se ujistěte, že jste ji důkladně otestovali a svoje uživatele vyškolili k jejímu používání.

## <a name="overview"></a>Přehled

Příchozí operace umožňuje uživateli POS provádět následující úlohy:

- Přijímat zásoby do obchodního skladu podle potvrzených dokumentů nákupních objednávek nebo dodaných převodních příkazů.
- Zobrazovat informace o historických příjemkách zásob na období sedmi dnů po úplném přijetí dokumentu.
- Vytvářet nové požadavky na příchozí převodní příkazy.

Při spuštění příchozí operace z aplikace POS se zobrazí stránka seznamu. Toto zobrazení obsahuje otevřené dokumenty nákupních objednávek a převodních příkazů, jejichž řádky zásob jsou naplánovány k přijetí aktuálním obchodem. Chcete-li najít a vybrat určitý dokument, mohou uživatelé seznam posunout nebo použít funkci vyhledávání.

Seznam dokumentů příchozích zásob obsahuje tři karty:

- **Aktivní** – Tato karta zobrazuje dokumenty, které jsou zcela nebo částečně otevřené a které obsahují řádky nebo množství na řádcích, které je stále nutné přijmout.
- **Koncept** – Tato karta zobrazuje nové požadavky na příchozí převodní příkazy, které byly v obchodě vytvořeny. Dokumenty však jsou uloženy pouze místně. Dosud nebyly odeslány do Commerce Headquarters ke zpracování.
- **Dokončeno** – Na této kartě je zobrazen seznam dokumentů nákupních objednávek nebo převodních příkazů, které obchod plně přijal během posledních sedmi dnů. Tato karta je určena pouze pro informaci. Všechny informace o dokumentech jsou pro daný obchod určeny pouze pro čtení.

Při zobrazení dokumentů na kterékoli z těchto karet vám pole **Stav** může pomoci pochopit fázi, ve které se dokument nachází.

- **Koncept** – dokument převodního příkazu byl uložen pouze místně do databáze kanálů obchodu. Do Commerce Headquarters nebyly odeslány žádné informace o požadavku na převodní příkaz.
- **Požadováno** – Nákupní objednávka nebo převodní příkaz byly vytvořeny v Commerce Headquarters a jsou plně otevřené. V souvislosti s dokumentem dosud nebyly zpracovány žádné příjemky. Pro dokumenty typu dokumentu nákupní objednávky může příjem začít kdykoli, až bude stav **Požadováno**.
- **Částečně expedováno** – doklad převodního příkazu má jeden nebo více řádků množství nebo částečného množství, které byly zaúčtovány jako expedované výstupním skladem. Tyto expedované řádky jsou dostupné k přijetí prostřednictvím příchozí operace.
- **Expedováno v plném rozsahu** – všechny řádky a celá množství na řádcích převodního příkazu byly zaúčtovány jako expedované výstupním skladem. Celý dokument je dostupný k přijetí prostřednictvím příchozí operace.
- **Částečně přijato** – některé řádky nebo množství na řádcích dokumentu nákupní objednávky nebo převodního příkazu byly přijaty obchodem, ale některé řádky zůstaly otevřené.
- **Plně přijato** – všechny řádky a množství na dokumentu nákupní objednávky nebo převodního příkazu byly plně přijaty. Dokumenty jsou přístupné pouze na kartě **Dokončeno** a jsou určeny pouze pro čtení uživateli obchodu.
- **Probíhá** – tento stav slouží k informování uživatelů zařízení o tom, že dokument aktivně zpracovává jiný uživatel.
- **Pozastaveno** – tento stav se zobrazí po zaškrtnutí políčka **Pozastavit příjem** pro dočasné zastavení procesu příjmu.
- **Zpracování v HQ** – dokument byl odeslán do Commerce Headquarters z aplikace POS, ale dosud nebyl úspěšně zaúčtován do Commerce Headquarters. Dokument prochází procesem asynchronního zaúčtování dokumentů. Po úspěšném zaúčtování dokumentu do Commerce Headquarters by měl být jeho stav aktualizován na **Plně přijato** nebo **Částečně přijato**.
- **Zpracování selhalo** – dokument byl zaúčtován do Commerce Headquarters a odmítnut. V podokně **Podrobnosti** se zobrazuje důvod selhání zaúčtování. Chcete-li opravit problémy s daty, je nutné upravit dokument a poté jej znovu odeslat do Commerce Headquarters ke zpracování.

Pokud vyberete řádek dokumentu v seznamu, zobrazí se podokno **Podrobnosti**. V tomto podokně jsou zobrazeny další informace o daném dokumentu, například informace o dodávce a datu. Indikátor průběhu ukazuje, kolik položek musí být ještě zpracováno. Pokud dokument nebyl úspěšně zpracován do Commerce Headquarters, zobrazí se v podokně **Podrobnosti** také chybové zprávy související s chybou.

Chcete-li zobrazit podrobnosti dokumentu, můžete v zobrazení stránky se seznamem dokumentů vybrat **Podrobnosti objednávky** na panelu aplikací. Zpracování příjmu lze rovněž aktivovat na vhodných řádcích dokladu.

V zobrazení stránky se seznamem dokumentů lze rovněž vytvořit nový požadavek na příchozí převodní příkaz pro obchod. Dokumenty zůstanou ve stavu **Koncept** a lze je upravit nebo odstranit, dokud nebudou odeslány do Commerce Headquarters ke zpracování. Po jejich odeslání do Commerce Headquarters již nelze řádky převodních příkazů měnit z aplikace POS.

## <a name="receiving-process"></a>Proces příjmu

Po výběru dokumentu nákupní objednávky nebo převodního příkazu na kartě **Aktivní** můžete vybrat **Podrobnosti objednávky** a zahájit tak proces příjmu.

Ve výchozím nastavení je aktivní zobrazení **Probíhá příjem**. Toto zobrazení je optimalizováno pro skenování čárových kódů. Lze ji použít k vytvoření seznamu skenovaných položek, aby bylo možné tyto položky přijmout. Chcete-li zahájit proces příjmu, můžete začít skenovat čárové kódy položek.

Pokud jsou čárové kódy položek skenovány v zobrazení **Probíhá příjem**, aplikace ověří tyto položky oproti vybranému dokumentu nákupní objednávky nebo převodního příkazu, aby bylo zajištěno, že se každá naskenovaná položka shoduje s platnou položkou v dokumentu. V zobrazení **Probíhá příjem** je každé skenování čárového kódu považováno za příjemku množství jedné jednotky, pokud není do čárového kódu vloženo množství. Chcete-li vytvořit seznam všech položek a množství pro příjemku, můžete v tomto zobrazení opakovaně skenovat čárové kódy.

### <a name="example-scenario"></a>Příklad

Uživatel obdrží nákupní objednávku, která obsahuje 10 jednotek čárového kódu 5657900266. Uživatel může tento čárový kód 10x naskenovat, aby aktualizoval pole **Probíhá příjem** o jednu jednotku na jedno skenování. Jakmile uživatel dokončí skenování, zobrazí se v poli **Probíhá příjem** pro řádek dané položky, že bylo přijato množství 10.

Případně ve scénáři, kde je množství položky příliš vysoké, může uživatel upřednostnit ruční zadání množství namísto skenování čárového kódu pro každou přijatou položku. V takovém případě může uživatel čárový kód jedním naskenováním přidat položku do seznamu **Probíhá příjem**. Uživatel pak může vybrat přidružený řádek v zobrazení **Probíhá příjem** a potom v podokně **Podrobnosti**, které se nachází na pravé straně stránky, aktualizovat pole **Přijaté množství** pro danou položku.

Přestože je zobrazení **Probíhá příjem** optimalizováno pro skenování čárového kódu, mohou uživatelé také vybrat možnost **Přijmout produkt** na panelu aplikací a zadat ID položky nebo čárový kód prostřednictvím dialogového okna. Po ověření položky, která byla zadána, se uživateli zobrazí výzva k zadání množství na příjemce.

Zobrazení **Probíhá příjem** poskytuje způsob, jak se mohou uživatelé zaměřit přijímané produkty. případně lze použít zobrazení **Úplný seznam objednávek**. Toto zobrazení obsahuje úplný seznam řádků dokumentu pro vybraný dokument nákupní objednávky nebo převodního příkazu. Uživatelé mohou ručně vybrat řádky v seznamu a poté v podokně **Podrobností** aktualizovat pole **Přijaté množství** pro vybraný řádek. V zobrazení **Úplný seznam objednávek** mohou uživatelé skenovat čárové kódy nebo mohou pomocí funkce **Přijmout produkt** zadat ID nebo čárový kód položky a data o přijatém množství, aniž by bylo nutné nejprve vybrat odpovídající řádek položky v seznamu.

### <a name="over-receiving-validations"></a>Ověření nadměrného příjmu

Během procesu příjmu pro řádky dokumentu dochází k jejich ověření. To zahrnuje ověření pro navýšení dodávky. Pokud se uživatel pokusí přijmout více zásob, než bylo objednáno na nákupní objednávce, ale buď není konfigurována nadměrná dodávka, nebo přijaté množství překračuje toleranci nadměrné dodávky, která je konfigurována pro řádek nákupní objednávky, obdrží uživatel chybu a není povoleno obdržet nadměrné množství.

Nadměrný příjem není povolen pro dokumenty převodního příkazu. Uživatelé budou vždy dostávat chyby, pokud se pokusí přijmout více, než bylo expedováno pro řádek převodního příkazu.

### <a name="receiving-location-controlled-items"></a>Příjem položek na základě umístění

Pokud jsou položky přijímány na základě umístění, mohou uživatelé vybrat umístění, kam chtějí položky přijmout během procesu příjmu. Doporučujeme nakonfigurovat výchozí místo příjmu na sklad obchodu, aby byl tento proces efektivnější. I v případě, že je nakonfigurováno výchozí umístění, mohou uživatelé přepsat místo příjmu na vybraných řádcích, jak potřebují.

Operace ctí konfiguraci **Povolen prázdný příjem** v dimenzi úložiště **Umístění** a nevyžaduje, aby byla zadána dimenze umístění, pokud je konfigurován prázdný příjem. Nejsou-li pro položku povolena prázdná místa příjmu, aplikace POS zobrazí chybu a vyžaduje zadání umístění před tím, než bude možné zaúčtovat příjem.

### <a name="receive-all"></a>Přijmout vše

Podle potřeby můžete výběrem možnosti **Přijmout vše** na panelu aplikací rychle aktualizovat množství pole **Probíhá příjem** pro všechny řádky dokumentu na maximální hodnotu, která je k dispozici pro příjem pro tyto řádky.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Příjem neplánovaných položek na nákupních objednávkách

V aplikaci Commerce verze 10.0.14 a novější mohou uživatelé obdržet produkt, který původně nebyl součástí nákupní objednávky. Chcete-li tuto funkci povolit, zapněte volbu **Přidat řádky na nákupní objednávku během příjmu pokladního místa**.  

Tato funkce funguje pouze pro příjem nákupní objednávky. Není možné přijímat položky proti převodním příkazům, pokud položky nebyly dříve objednány a odeslány z odchozího skladu.

Uživatelé nemohou do nákupní objednávky přidávat nové produkty během přijímání POS, pokud není zapnut [pracovní postup správy změn](https://docs.microsoft.com/dynamics365/supply-chain/procurement/purchase-order-approval-confirmation) nákupní objednávky v centrále Commerce. Chcete-li povolit správu změn, musí být všechny změny nákupní objednávky nejprve schváleny, než bude povoleno přijetí. Protože tento proces umožňuje příjemci přidávat do objednávky nové řádky, přijímání se nezdaří, pokud je povolen pracovní postup správy změn. Pokud je povolena správa změn pro všechny nákupní objednávky nebo pro dodavatele propojeného s aktivní objednávkou objednávky v POS, nemůže uživatel během přijímání v POS přidat do objednávky nové produkty.

Funkci, která umožňuje přidávání řádků, nelze použít jako řešení pro příjem dalších množství produktů, které jsou již na nákupní objednávce. Nadměrný příjem je spravován standardním nastavením [nadměrného příjmu](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation#over-receiving-validations) produktové řady na nákupní objednávce.

Pokud je povolena volba **Přidat řádky na nákupní objednávku během příjmu pokladního místa** a uživatel přijímá pomocí **Příchozí operace** v POS, pokud uživatel naskenuje čárový kód produktu nebo číslo produktu, které není rozpoznáno jako položka v aktuální nákupní objednávce, ale je rozpoznáno jako platná položka, obdrží uživatel zprávu o přidání položky do nákupní objednávky. Pokud uživatel přidá položku do nákupní objednávky, zadané množství v poli **Probíhá příjem** se považuje za objednané množství pro řádek nákupní objednávky.

Když je dokončen příjem nákupní objednávky a odeslán do centrály ke zpracování, přidané řádky se vytvoří v hlavním dokumentu nákupní objednávky. Na řádku nákupní objednávky v centrále bude příznak **Přidalo POS** na kartě **Obecné** na řádku nákupní objednávky. Příznak **Přidalo POS** označuje, že řádek nákupní objednávky byl přidán procesem přijímání POS a nejedná se o řádek, který byl na nákupní objednávce před přijetím.

### <a name="cancel-receiving"></a>Zrušit příjem

Funkci **Zrušit příjem** na panelu aplikací použijte pouze v případě, že chcete odejít z dokumentu a nechcete uložit žádné změny. Původně jste například vybrali nesprávný dokument a nechcete, aby byla uložena předchozí data příjmu.

### <a name="pause-receiving"></a>Pozastavit příjem

Pokud přijímáte zásoby, můžete použít funkci **Pozastavit příjem**, pokud chcete pozastavit proces přijímání. Můžete například chtít provést další operaci z POS, jako například zavolat na oddělení prodeje zákazníkům nebo zpozdit zaúčtování příjmu.

Pokud vyberete možnost **Pozastavit příjem**, bude stav dokumentu změněn na **Pozastaveno**. Uživatelé proto budou vědět, že byla zadána data pro daný dokument, ale dokument ještě nebyl potvrzen. Až budete připraveni pokračovat v procesu příjmu, vyberte pozastavený dokument a pak vyberte **Podrobnosti objednávky**. Všechna dříve uložená množství **Probíhá příjem** jsou zachována a lze je zobrazit ze zobrazení **Úplný seznam objednávek**.

### <a name="review"></a>Přehled

Před konečným potvrzením o přijetí do centrály Commerce (HQ) můžete pomocí funkce kontroly ověřit příchozí dokument. Přezkum vás upozorní na chybějící nebo nesprávná data, která mohou způsobit selhání zpracování, a poskytne vám možnost opravit problémy před odesláním žádosti o potvrzení. Chcete-li povolit funkci **Recenze** na panelu aplikací, povolte funkci **Povolit ověření v příchozích a odchozích skladových operacích POS** prostřednictvím pracovního prostoru **Správa funkcí** v centrále Commerce (HQ).

Funkce **Recenze** ověřuje následující problémy v příchozím dokumentu:

- **Nadměrný příjem** - nyní přijímané množství je větší než objednané množství. Závažnost tohoto problému je dána konfigurací navýšení dodávky v centrále Commerce (HQ).
- **Příjem menšího množství** - nyní přijímané množství je menší než objednané množství. Závažnost tohoto problému je dána konfigurací snížení dodávky v centrále Commerce (HQ).
- **Sériové číslo** - sériové číslo není poskytnuto ani ověřeno pro serializovanou položku, která vyžaduje, aby bylo sériové číslo zapsáno do zásob.
- **Místo není nastaveno** - místo není určeno pro položku na základě polohy, kde není povoleno prázdné místo.
- **Odstraněné řádky** - v objednávce jsou odstraněny řádky uživatelem centrály Commerce (HQ), které nejsou POS aplikaci známy.

Nastavte parametr **Povolit automatické ověření** na **Ano** v **Parametry obchodu** > **Zásoby** > **Skladové zásoby**, aby bylo ověření provedeno automaticky, když je vybrána volba **Dokončit příjem**.

### <a name="finish-receiving"></a>Dokončit příjem

Po dokončení zadávání všech množství **Probíhá příjem** je nutné pro zpracování příjmu vybrat možnost **Dokončit příjem** na panelu aplikací.

Když uživatelé dokončí příjem nákupní objednávky, jsou vyzváni k zadání hodnoty do pole **Ćíslo příjemky**, pokud je tato funkce konfigurována. Tato hodnota se obvykle rovná identifikátoru dodacího listu dodavatele. Data **Číslo příjemky** budou uložena do deníku příjemek produktů v Commerce Headquarters. Čísla příjemek nejsou zaznamenána pro žádné příjemky převodního příkazu.

Při použití asynchronního zpracování dokumentu je příjem odeslán prostřednictvím asynchronní architektury dokumentu. Doba potřebná pro zaúčtování dokumentu závisí na velikosti dokumentu (počtu řádků) a na obecném provozu zpracování na serveru. Obvykle k tomuto zpracování dojde v průběhu několika sekund. Pokud se zaúčtování dokumentu nezdaří, bude uživatel upozorněn prostřednictvím seznamu dokumentů **Příchozí operace**, kde se stav dokumentu aktualizuje na **Zpracování selhalo**. Uživatel pak může vybrat neúspěšný dokument v POS, aby zobrazil chybové zprávy a důvod selhání v podokně **Podrobnosti**. Neúspěšný dokument zůstane nezaúčtovaný a vyžaduje, aby se uživatel vrátil k řádkům dokumentu výběrem možnosti **Podrobnosti objednávky** v POS. Uživatel musí poté na základě chyb opravit dokument. Po opravě dokumentu se uživatel může pokusit jej znovu zpracovat výběrem možnosti **Dokončit plnění** na panelu aplikací.

## <a name="create-an-inbound-transfer-order"></a>Vytvoření příchozího převodního příkazu

V aplikaci POS mohou uživatelé vytvářet nové dokumenty převodních příkazů. Chcete-li zahájit proces, vyberte možnost **Nový** na panelu aplikací, zatímco se nacházíte v hlavním seznamu dokumentů **Příchozí operace**. Poté budete vyzváni k výběru skladu nebo obchodu pro možnost **Převést z**, který bude poskytovat zásoby do umístění obchodu. Hodnoty jsou omezeny na výběr, který je definován v konfiguraci skupiny plnění obchodu. V požadavku na příchozí převod bude váš aktuální obchod pro převodní příkaz vždy sklad **Převést do**. Tuto hodnotu nelze změnit.

V případě potřeby můžete zadat hodnoty do polí **Datum expedice**, **Datum příjmu** a **Způsob dodání**. Můžete také přidat poznámku, která bude uložena spolu se záhlavím převodního příkazu jako příloha dokumentu v Commerce Headquarters.

Po vytvoření informací v záhlaví můžete do převodního příkazu přidávat produkty. Chcete-li zahájit proces přidávání položek a požadovaných množství, vyberte možnost **Přidat produkt**. V podokně **Podrobnosti** můžete také přidat poznámku specifickou pro řádek deníku. Tyto poznámky budou uloženy jako příloha k řádku.

Po zadání řádků na příchozí převodní příkaz je nutné vybrat možnost **Uložit** pro uložení dokumentu v místním počítači nebo možnost **Odeslat požadavek** pro odeslání podrobností objednávky do Commerce Headquarters za účelem dalšího zpracování. Pokud vyberete možnost **Uložit**, dokument konceptu je uložen v databázi kanálů a výstupní sklad nemůže dokument spustit, dokud není úspěšně zpracován prostřednictvím funkce **Odeslat požadavek**. Možnost **Uložit** vyberte pouze v případě, že nejste připraveni potvrdit zpracování požadavku v Commerce Headquarters.

Pokud je dokument uložen místně, lze jej najít na kartě **Koncepty** v seznamu dokumentů **Vstupní operace**. Když je dokument ve stavu **Koncept**, můžete jej upravit výběrem možnosti **Upravit**. Řádky můžete podle potřeby aktualizovat, přidávat nebo odstraňovat. Můžete také odstranit celý dokument, který je ve stavu **Koncept**, výběrem možnosti **Odstranit** na kartě **Koncepty**.

Po úspěšném odeslání dokumentu konceptu do Commerce Headquarters se tento dokument zobrazí na kartě **Aktivní** ve stavu **Požadováno**. V tomto okamžiku nemohou uživatelé v příchozím úložišti nebo skladu nadále upravovat požadovaný dokument příchozího převodního příkazu. Dokument mohou upravit pouze uživatelé v odchozím skladu výběrem možnosti **Odchozí operace** v aplikaci POS. Zámek pro úpravy zajišťuje, že nedojde k žádnému konfliktu, kdyby příchozí žadatel změnil převodní příkaz současně s tím, když odchozí přepravce aktivně vyskladňuje a expeduje objednávku. Pokud jsou v příchozím obchodě nebo skladu vyžadovány změny po odeslání převodního příkazu, je třeba se spojit s odchozím přepravcem a požádat jej o zadání změn.

Poté, co je dokument ve stavu **Požadováno**, je viditelný na kartě **Aktivní**. Nelze jej však zatím přijmout v příchozím obchodu nebo skladu. Poté, co výstupní sklad expedoval některé nebo všechny převodní příkazy, vstupní obchod nebo sklad může zaúčtovat příjemky v POS. Když výstupní strana zpracovává dokumenty převodního příkazu, jejich stav je aktualizován ze stavu **Požadováno** na **Expedováno** nebo **Částečně expedováno**. Jakmile jsou dokumenty ve stavu **Expedováno** nebo **Částečně expedováno**, může příchozí obchod nebo sklad podle nich účtovat příjemky pomocí procesu příjmu příchozí operace.

## <a name="related-topics"></a>Související témata

[Odchozí skladová operace v POS](pos-outbound-inventory-operation.md)
