---
title: Elektronické zprávy
description: Toto téma poskytuje přehled a informace o nastavení pro elektronické zprávy v Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5326642553c7efcebc6c6af953e2dafe9e62e9ec
ms.sourcegitcommit: f6fc90585632918d9357a384b27028f2aebe9b5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/11/2019
ms.locfileid: "832188"
---
# <a name="electronic-messaging"></a>Elektronické zprávy

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled a informace o nastavení pro elektronické zprávy v Microsoft Dynamics 365 for Finance and Operations.

Nedávno vlády a legislativní orgány různých zemí a regionů na celém světě zavedly požadavky na podávání zpráv pro společnosti, které jsou registrovány v těchto zemích nebo regionech. Účelem požadavků je umožnit získávání údajů z těchto společností v elektronickém formátu přímo ze systémů, kde byly účtovány, uloženy a zpracovány.

Funkce elektronických zpráv v aplikaci Finance and Operations podporuje různé procesy elektronické spolupráce mezi aplikací Finance and Operations a systémy, které vlády a legislativní orgány nabízejí pro podávání zpráv, předkládání a přijímání oficiálních informací

Funkce elektronických zpráv je integrována s modulem **Elektronického výkaznictví**. Můžete tedy nastavit formáty elektronického výkaznictví pro elektronické zprávy. Další informace získáte v tématu [Elektronické výkaznictví](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektronické zprávy jsou založeny na následujících entitách:

- **Elektronická zpráva** – Sestava nebo prohlášení, které mají být vykázány anebo přenášeny interně. Příkladem jsou sestavy, které jsou odesílány daňovému úřadu.
- **Položky elektronických zpráv** – Záznamy, které mají být zahrnuty ve vykazované zprávě.
- **Zpracování elektronické zprávy** – Sled akcí, buď propojený nebo odpojený, který by měl být spuštěn pro shromažďování požadovaných dat, generování sestav, ukládání dat do úložiště objektů blob Microsoft Azure, přenos sestav mimo systém, získání odpovědí mimo systém a aktualizace databáze založené na získaných informacích.

Následující obrázek znázorňuje tok dat pro elektronické zprávy.

![Tok dat elektronických zpráv](media/electronic-messaging-data-flow.png)

Funkce elektronických zpráv podporuje následující situace:

- Ruční vytváření zpráv a generování sestav založených na přidružených exportních formátech elektronického výkaznictví různých typů: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, text a Microsoft Word.
- Automatické vytvoření a zpracování zpráv, které jsou založeny na informacích požadovaných a získaných od úřadu prostřednictvím přidruženého formátu importu elektronického výkaznictví.
- Sběr a zpracování informací z datového zdroje (tabulka Finance and Operations) jako položek zprávy.
- Ukládání dalších informací a vyhodnocování různých hodnot voláním specificky definovaných spustitelných tříd ve vztahu ke zprávám nebo položkám zpráv.
- Agregování informací, které jsou shromážděny v položkách zprávy, rozdělení těchto informací podle zprávy a generování sestav v přidružených exportních formátech elektronického výkaznictví.
- Přenesení sestav, které jsou generovány do webové služby pomocí informací o zabezpečení uložených v Azure Key Vault.
- Získání odpovědi z webové služby, vyhodnocení odpovědi a aktualizace dat v aplikaci Finance and Operations podle potřeby.
- Uložení a kontrola všech sestav, které jsou generovány.
- Uložení a kontrola všech informací o protokolu, souvisejících s akcemi, které jsou spuštěny pro zprávy nebo položky zprávy.
- Kontrola zpracování pomocí různých stavů zpráv a položek zpráv.

## <a name="set-up-electronic-messaging"></a>Nastavení elektronických zpráv

Elektronické zprávy vám pomohou udržovat různé procesy elektronického výkaznictví pro různé typy dokumentů. V některých komplexních scénářích je elektronická zpráva nastavena tak, aby měla kombinaci mnoha stavů zpráv, stavů položek zpráv, akcí, dalších polí a spustitelných tříd. Pro tyto scénáře jsou k dispozici balíčky datových entit pro import. Pokud použijete tyto balíčky datových entit, měli byste je importovat do právnické osoby pomocí nástroje pro správu dat. Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](../../dev-itpro/data-entities/data-entities-data-packages.md).

Pokud neimportujete balíček datových entit, můžete ručně nastavit funkčnost elektronických zpráv. V takovém případě je třeba nastavit následující prvky: 

- [Číselné řady](#number-sequences)
- [Stavy a typy položek zprávy](#message-item-types-and-statuses)
- [Stavy zpráv](#message-statuses)
- [Dodatečná pole](#additional-fields)
- [Nastavení spustitelné třídy](#executable-class-settings)
- [Akce naplnění záznamů](#populate-records-actions)
- [Webové aplikace](#web-applications)
- [Nastavení webové služby](#web-service-settings)
- [Akce zpracování zprávy](#message-processing-actions)
- [Zpracování elektronické zprávy](#electronic-message-processing)

Další části poskytují více informací o každém z těchto prvků.

### <a name="number-sequences"></a>Číselné řady

Nastavte číselné řady pro zprávy a položky zprávy. Číselné řady se používají k automatickému číslování zpráv a položek zpráv a přiřazená čísla se použijí jako jedinečné identifikátory zpráv a položek zpráv v systému. Můžete nastavit číselné řady pro elektronické zprávy na stránce **Parametry hlavní knihy** (**Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**).

### <a name="message-item-types-and-statuses"></a>Stavy a typy položek zprávy

Typy položek zpráv určují typy záznamů, které budou použity v elektronických zprávách. Můžete nastavit typy položek zpráv na stránce **Typy položek zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Typy položek zpráv**).

Stavy položek zpráv určují stavy, které se budou vztahovat na položky zpráv při zpracování, které nastavujete. Můžete nastavit stavy položek zpráv na stránce **Stavy položek zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy položek zpráv**).

Parametr **Povolit odstranění** stavu položky zprávy určuje, zda uživateli bude povoleno odstranění položky zprávy v tomto stavu prostřednictvím formuláře **Elektronické zprávy** nebo formuláře **Položky elektronických zpráv**. 

### <a name="message-statuses"></a>Stavy zpráv

Nastavte stavy zpráv, které by měly být k dispozici při zpracování zprávy. Můžete nastavit stavy zprávy na stránce **Stavy zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy zpráv**).

Popis polí:

| Název pole           | Popis |
|----------------------|-------------|
|Stav zprávy        | Jedinečný název stavu elektronické zprávy, který určuje stav zprávy v každém okamžiku. Tento název je zobrazen ve formuláři elektronických zpráv a v protokolu souvisejícím s elektronickou zprávou. |
|Popis           | Popis týkající se stavu elektronické zprávy      |
|Typ odezvy         | Některé akce zpracování mohou mít za následek více než jeden typ odezvy. Jako například akce typu **Webová služba** může vyústit buď v typ odpovědi **Úspěšně provedeno** nebo **Technická chyba** v závislosti na výsledku spuštění. V takovém případě musí být definován stav zprávy pro oba typy odezvy. V části [Typy akcí zpracování zprávy](#message-processing-action-types) naleznete další informace o typech akcí a s nimi souvisejících typech odezvy. |
|Stav položky zprávy   |Existují případy, kdy stav elektronické zprávy musí mít vliv na stavy souvisejících položek zprávy. Přidružte takový stav položky zprávy v tomto poli jeho výběrem z vyhledávání. |
|Odstranit vše          | Parametr **Povolit odstranění** stavu elektronické zprávy určuje, zda uživateli bude povoleno odstranění elektronické zprávy v tomto stavu prostřednictvím formuláře **Elektronické zprávy**.            |

### <a name="additional-fields"></a>Dodatečná pole

Funkce elektronických zpráv umožňuje naplnit záznamy z transakční tabulky. Tímto způsobem lze připravit záznamy pro vykazování a poté je vykázat. V některých případech není dostatek informací v transakční tabulce pro vykázání záznamu podle požadavků sestavy. Můžete vyplnit všechny informace, které musí být vykázány pro záznam nastavením dalších polí. Další pole lze přidružit ke zprávám i položkám zpráv. Můžete nastavit další pole na stránce **Další pole** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Další pole**).

Následující tabulka popisuje obecná pole na stránce **Další pole**:

| Pole                | Popis |
|----------------------|-------------|
| Název pole           | Zadejte název dalšího atributu položek zprávy, které se vztahují k procesu. Tento název se zobrazí v uživatelském rozhraní při práci s procesem. Lze jej rovněž použít v konfiguracích elektronického výkaznictví, které se vztahují k procesu. |
| Popis          | Zadejte popis dalšího atributu položek zprávy, které se vztahují k procesu. |
| Úpravy uživatele            | V případě, že uživatel musí být schopen změnit hodnotu dalšího pole z uživatelského rozhraní, nastavte toto pole na **Ano**, v opačném případě na **Ne**. |
| Počitadlo              | Když musí dodatečné pole obsahovat pořadové číslo v rámci elektronické zprávy, zaškrtněte toto políčko. Hodnoty dodatečného pole se vyplní automaticky při spuštění akce typu Export elektronického výkaznictví.  |
| Skryté               | Pokud musí být další pole skryto z uživatelského rozhraní, zaškrtněte toto políčko.  |

Každé další pole může mít pro zpracování odlišné hodnoty. Tyto hodnoty můžete definovat na pevné záložce Hodnoty:

| Pole                | Popis |
|----------------------|-------------|
| Hodnota pole          | Zadejte hodnotu pole pro použití ve vztahu ke zprávě nebo položce zprávy při vykazování. |
| Popis pole    | Zadejte popis hodnoty pole pro použití ve vztahu ke zprávě nebo položce zprávy při vykazování. |
| Typ účtu         | Některé další hodnoty polí mohou být omezeny na určité typy účtů. Vyberte jednu z následujících hodnot: **Všechny**, **Odběratel**, nebo **Dodavatel**. |
| Kód účtu         | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu**, můžete dále omezit použití hodnot polí na konkrétní skupinu nebo tabulku. |
| Číslo účtu/skupiny | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu** a zadali jste skupinu nebo tabulku do pole **Kód účtu**, můžete v tomto poli zadat určitou skupinu nebo protistranu. |
| Účinné:            | Zadejte datum, kdy má být hodnota zahájena ke zvažovaní. |
| Vypršení platnosti           | Zadejte datum, kdy má být hodnota ukončena pro zvažování. |

Kombinace kritérií **Číslo účtu/skupiny**, **Kód účtu**, **Účinné** a **Vypršení platnosti** neovlivňují ve výchozím nastavení výběr hodnot pro dodatečné pole, ale lze je použít ve spustitelné třídě pro implementaci některé konkrétní logiky výpočtu hodnoty dodatečného pole.

### <a name="executable-class-settings"></a>Nastavení spustitelné třídy

Spustitelná třída je metoda X ++ nebo třída, kterou může zpracování elektronické zprávy volat ve vztahu k akci, pokud je některé hodnocení vyžadováno pro proces.

Spustitelnou třídu lze ručně nastavit na stránce **Nastavení spustitelné třídy** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Nastavení spustitelné třídy**). Vytvořte řádek a nastavte následující pole.

| Pole                 | popis |
|-----------------------|-------------|
| Spustitelná třída      | Zadejte název, který bude použit při nastavení akce zpracování zpráv, pro kterou je tato třída volána. |
| Popis           | Zadejte popis spustitelné třídy. |
| Název spustitelné třídy | Výběr spustitelnou třídu X ++. |
| Úroveň spuštění       | Toto pole je nastaveno automaticky, protože by měla být předdefinovaná hodnota pro vybranou spustitelnou třídu. Toto pole omezuje úroveň, na níž probíhá související hodnocení. |
| Popis třídy     | Toto pole je nastaveno automaticky, protože by měla být předdefinovaná hodnota pro vybranou spustitelnou třídu. |

Některé spustitelné třídy mohou mít povinné parametry, které musí být definovány před prvním spuštěním spustitelné třídy. Pro definování těchto parametrů klikněte na tlačítko **Parametry** v podokně akcí, nastavte odpovídající hodnoty a pole v dialogovém okně a klikněte na tlačítko **OK**. Je důležité kliknout na tlačítko **OK**, protože jinak nebudou parametry uloženy do základu a spustitelná třída nebude správně vyvolána.

### <a name="populate-records-actions"></a>Akce naplnění záznamů

Použijete akce naplnění záznamů nastavení akcí, které přidávají záznamy do tabulky položek zpráv tak, aby mohly být přidány do elektronické zprávy. Například pokud vaše elektronická zpráva musí vykazovat faktury odběratele, je nutné nastavit akci **Naplnit záznamy**, která je propojena na tabulku **Deník faktur odběratele** (v poli **Zdroj dat**). Můžete nastavit akce naplnění záznamů na stránce **Akce naplnění záznamů** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce naplnění záznamů**). Vytvořte nový záznam pro každou akci, která by měla přidat záznamy do tabulky, a nastavte následující pole.

| Pole       | Popis                                                               |
|-------------|---------------------------------------------------------------------------|
| Jméno        | Zadejte název akce, která naplní záznamy ve vašem procesu.       |
| Popis | Zadejte popis akce, která naplní záznamy ve vašem procesu. |

Na záložce s náhledem **Nastavení datových zdrojů** přidejte řádek pro každý datový zdroj, který se používá pro proces, a nastavte následující pole.

| Pole                  | Popis |
|------------------------|-------------|
| Jméno                   | Zadejte název pro datový zdroj. |
| Typ položky zprávy      | Vyberte typ položky zprávy, která by měla být použita při vytváření záznamů pro datový zdroj. |
| Typ účtu           | Vyberte typ účtu, který má být přiřazen k záznamům z datového zdroje. |
| Název hlavní tabulky      | Vyberte tabulku v aplikaci Finance and Operations, která by měla být datovým zdrojem. |
| Pole čísla dokumentu  | Zvolte pole, ze kterého má být číslo dokumentu převzato ve vybrané tabulce. |
| Pole data dokumentu    | Zvolte pole, ze kterého má být datum dokumentu převzato ve vybrané tabulce. |
| Pole účtu dokumentu | Zvolte pole, ze kterého má být účet dokumentu převzat ve vybrané tabulce. |
| Dotaz uživatele             | Je-li toto políčko zaškrtnuto, můžete nastavit dotazu výběrem možností **Upravit dotaz** nad mřížkou. V opačném případě budou všechny záznamy vyplněny z datového zdroje. |

### <a name="web-applications"></a>Webové aplikace

Stránka webových aplikací slouží k nastavení parametrů webové aplikace pro podporu otevřeného standardu OAuth 2.0, který umožňuje uživatelům udělit bezpečný delegovaný přístup k aplikaci v jejich zastoupení bez sdílení přístupových pověření. Z této stránky můžete také projít procesem autorizace získáním autorizačního kódu a přístupového tokenu. Můžete provést nastavení webové aplikace na stránce **Webové aplikace** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Webové aplikace**) .

Následující tabulka popisuje pole na stránce **Webové aplikace**.

| Pole                         | Popis |
|-------------------------------|-------------|
| Název aplikace              | Zadejte název webové aplikace. |
| Popis                   | Zadejte popis webové aplikace. |
| Základní adresa URL                      | Zadejte základní internetovou adresu webové aplikace. |
| URL cesta autorizace        | Zadejte cestu k vytvoření adresy URL pro autorizaci.  |
| URL cesta tokenu                | Zadejte cestu k vytvoření adresy URL pro token.  |
| Přesměrovací adresa URL                  | Zadejte přesměrovací adresu URL.  |
| ID klienta                     | Zadejte ID klienta webové aplikace.  |
| Tajný klíč klienta                 | Zadejte tajný klíč klienta webové aplikace.  |
| Token serveru                  | Zadejte token serveru webové aplikace.  |
| Mapování formátu autorizace  | Vyberte formát elektronického výkaznictví, který má být použit pro vygenerování požadavku na autorizaci.   |
| Import mapování modelu tokenu    | Vyberte mapování modelu importu ER, který bude použit pro ukládání přístupového tokenu.  |
| Udělený rozsah      Přístupový token vyprší za  | Toto pole se aktualizuje automaticky. Jeho hodnota ukazuje udělený rozsah požadavků na webovou aplikaci.  |
| Přijmout                        | Určete vlastnost přijetí webového požadavku. Například "application/vnd.hmrc.1.0+json".  |
| Typ obsahu           | Určete typ obsahu. Například "aplikace/json".  |

Následující funkce jsou k dispozici ze stránky **Webové aplikace** pro podporu procesu autorizace:
-   **Získání autorizačního kódu** - pro inicializaci autorizace webové aplikace.
-   **Obdržení autorizačního kódu** – pro inicializací získání přístupového tokenu.
-   **Obnovení přístupového tokenu** – pro obnovení přístupového tokenu.

Pokud je přístupový token k webové aplikaci uložený v databázi systému v zašifrovaném formátu, může být použit pro požadavky na webovou službu. Pro účely zabezpečení musí být přístup k přístupovému tokenu omezen pouze na ty role zabezpečení, kterým musí být umožněno tyto požadavky řešit. Pokud se uživatel mimo skupinu zabezpečení pokouší adresovat požadavek, výjimka bude informovat uživatele o tom, že není dovoleno spolupracovat prostřednictvím vybrané webové aplikace.
Použijte záložku s náhledem **Role zabezpečení** stránky Daň > Nastavení > Elektronické zprávy > Webové aplikace pro nastavení rolí, které musí mít přístup k přístupovému tokenu. Pokud nejsou role zabezpečení definovány pro webovou aplikaci, bude správce systému schopen spolupracovat pouze prostřednictvím této webové aplikace.

### <a name="web-service-settings"></a>Nastavení webové služby

Pomocí nastavení webových služeb nastavíte přímý přenos dat do webové služby. Můžete provést nastavení webové služby na stránce **Nastavení webové služby** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Nastavení webové služby**) .

Následující tabulka popisuje pole na stránce **Nastavení webové služby**.

| Pole                   | popis |
|-------------------------|-------------|
| Webová služba             | Zadejte název webové služby. |
| popis             | Zadejte popis webové služby. |
| Internetová adresa        | Zadejte internetovou adresu webové služby. Je-li pro webovou službu zadána webová aplikace a internetová adresa by měla být stejná jako adresa definovaná pro vybranou webovou aplikaci, klikněte na tlačítko **Zkopírovat základní URL adresu** a zkopírujte dresu **Základní adresu URL** z webové aplikace do pole **Internetová adresa** webové služby.  |
| Certifikát             | Vyberte certifikát Key Vault, který byl již předtím nastaven. |
| Webová aplikace         | Vyberte certifikát Key Vault, který byl již předtím nastaven. |
| Typ odezvy – XML | Nastavte tuto možnost na **Ano**, pokud je typ odpovědi XML. |
| Metoda požadavku          | Zadejte způsob požadavku. HTTP definuje sadu metod požadavků, které označují akci, která by měla být provedena pro daný zdroj. Metodou může být **GET**, **POST**, nebo jiná metoda HTTP. |
| Záhlaví požadavku         | Určete záhlaví požadavku. Záhlaví požadavku je záhlaví HTTP, které lze použít v požadavku HTTP, a které nesouvisí s obsahem zprávy. |
| Přijmout                  | Určete vlastnost přijetí webového požadavku. |
| Přijmout kódování         | Zadejte Accept-Encoding. Záhlaví HTTP požadavku Accept-Encoding oznamuje kódování obsahu, které může klient pochopit. Toto kódování obsahu je obvykle algoritmus komprese. |
| Typ obsahu            | Určete typ obsahu. Záhlaví entity Content-Type označuje typ média zdroje. |
| Úspěšný kód odpovědi   | Určete kód stavu HTTP označující, že požadavek byl úspěšný. |
| Mapování formátu záhlaví požadavku  | Vyberte formát ER pro generování záhlaví webového požadavku. |

### <a name="message-processing-actions"></a>Akce zpracování zprávy

Pomocí akcí zpracování zpráv vytváříte akce pro své procesy a nastavujete jejich parametry. Můžete nastavit akce zpracování zpráv na stránce **Akce zpracování zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce zpracování zpráv**).

Následující tabulky popisují pole na stránce **Akce zpracování zpráv**.

#### <a name="general-fasttab"></a>Záložka s náhledem Obecné

| Pole                   | popis |
|-------------------------|-------------|
| Typ akce             | Vyberte typ akce. Informace o dostupných možnostech naleznete v části [Typy akcí zpracování zpráv](#message-processing-action-types). |
| Mapování formátu          | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví**, **Import elektronického výkaznictví** a **Zpráva exportu elektronického výkaznictví**. |
| Mapování formátu pro cestu URL | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Toto pole je dostupné pouze pro akce typu **Webová služba** a slouží k vytvoření cesty adresy URL, která bude přidána k základní internetové adrese určené pro vybraný webový server. |
| Typ položky zprávy       | Vyberte typ záznamů, pro které by měla být akce vyhodnocována. Toto pole je k dispozici pro akce typu **Úroveň spuštění položky zprávy**, **Import elektronického výkaznictví** a **Export elektronického výkaznictví**, **Webová služba** a rovněž některé další typy. Necháte-li toto pole prázdné, vyhodnotí se všechny typy položek zpráv, které jsou definovány pro zpracování zpráv. |
| Spustitelná třída        | Vyberte nastavení spustitelné třídy, která již byla vytvořena. Toto pole je k dispozici pouze pro akce typu **Úroveň spuštění zprávy** a **Úroveň spuštění položky zprávy**. |
| Akce naplnění záznamů | Vyberte akci naplnění záznamů, která již byla nastavena. Toto pole je k dispozici pouze pro akce typu **Naplnit záznamy**. |
| Webová služba  | Vyberte webovou službu, která již byla nastavena. Toto pole je k dispozici pouze pro akce typu **Webová služba**.  |
| Název souboru  | Zadejte název souboru, který bude mít za následek akci jako odpověď z webového serveru nebo generování sestavy. Toto pole je k dispozici pouze pro akce typu **Webová služba** a **Zpráva exportu elektronického výkaznictví**.   |
| Zobrazit dialogové okno  | Zaškrtněte toto políčko, pokud musí být uživateli před vytvořením sestavy zobrazeno dialogové okno. Toto pole je k dispozici pouze pro akce typu **Zpráva exportu elektronického výkaznictví**.   |

##### <a name="message-processing-action-types"></a>Typy akcí zpracování zprávy

Následující možnosti jsou dostupné v poli **Typ akce**.

- **Vytvořit zprávu** – Použití tohoto typu umožní uživatelům ručně vytvořit zprávy na stránce **Elektronická zpráva**. Počáteční stav nemůže být pro akci tohoto typu nastaven.
- **Naplnit záznamy** – Akce **Naplnit záznamy** musí být nastavena dříve. Přidružte ji k akci typu **Naplnit záznamy**, aby mohla být zahrnuta do zpracování. Předpokládá se, že tento typ akce se používá buď pro první akci ve zpracování zprávy (pokud není předem vytvořena žádná elektronická zpráva) nebo jako akce přidání položek zprávy do dříve vytvořené zprávy (akcí typu **Vytvořit zprávu**). Proto lze pro akci tohoto typu nastavit stav výsledků pouze položek zpráv. Lze nastavit počáteční stav pouze pro zprávu.
- **Úroveň spuštění zprávy** – Tento typ slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni zprávy.
- **Úroveň spuštění položky zprávy** – Tento typ slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni položky zprávy.
- **Export elektronického výkaznictví** – Použijte tento typ pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpráva exportu elektronického výkaznictví** – Použijte tento typ pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy (například když zpráva nemá žádné položky zprávy).
- **Import elektronického výkaznictví** – Použijte tento typ pro akce, které mají generovat sestavu, která je založena na importu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpracování uživatele na úrovni zprávy** – Tento typ použijte pro akce, které předpokládají některé ruční akce provedené uživatelem. Uživatel může například aktualizovat stav zpráv.
- **Zpracování uživatele** – Tento typ použijte pro akce, které předpokládají některé ruční akci provedenou uživatelem. Uživatel může například aktualizovat stav položek zpráv.
- **Webová služba** – Tento typ použijte pro akce, které mají přenášet generovanou sestavu do webové služby. Tento typ akce není použit pro italské vykazování komunikace o prodejních a nákupních fakturách. Pro akce typu **Webová služba** můžete určit **Text potvrzení** na záložce s náhledem **Různé podrobnosti** možnosti **Akce zpracování zprávy**. Tento potvrzovací text bude uživateli zobrazen před adresováním požadavku na vybranou webovou službu.
- **Požádat o ověření** – Použijte tento typ pro vyžádání ověření ze serveru.

#### <a name="initial-statuses-fasttab"></a>Záložka s náhledem Počáteční stavy

> [!NOTE]
> Záložka s náhledem **Počáteční stavy** není k dispozici pro akce, které mají počáteční typ **Vytvořit zprávu**.

| Pole               | Popis                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Stav položky zprávy | Vyberte stav položky zprávy, pro který by měla být vyhodnocena vybraná akce zpracování zpráv. |
| popis         | Popis vybraného stavu položky zprávy.                                                  |

#### <a name="result-statuses-fasttab"></a>Záložka s náhledem Výsledné stavy

| Pole               | popis |
|---------------------|-------------|
| Stav zprávy      | Vyberte stavy zprávy, pro který by měla být vyhodnocena vybraná akce zpracování zpráv. Toto pole je k dispozici pouze pro akce zpracování zpráv, které jsou vyhodnocovány na úrovni zprávy. Například je k dispozici pro akce typu **Export elektronického výkaznictví** a **Import elektronického výkaznictví**. Není k dispozici pro akce typu **Zpracování uživatele** a **Úroveň spuštění položky zprávy**. |
| popis         | Popis vybraného stavu zprávy. |
| Typ odezvy       | Typ odpovědi vybraného stavu zprávy. |
| Stav položky zprávy | Vyberte výsledné stavy, které by měly být k dispozici po vyhodnocení vybrané akce zpracování zpráv. Toto pole je k dispozici pouze pro akce zpracování zpráv, které jsou vyhodnocovány na úrovni položky zprávy. Například je k dispozici pro akce typu **Zpracování uživatele** a **Úroveň spuštění položky zprávy**. U akcí zpracování zpráv, které jsou vyhodnoceny na úrovni zprávy, toto pole zobrazuje stav položky zprávy, který byl nastaven pro vybraný stav zprávy. |

Následující tabulka ukazuje, jaké stavy výsledků musí být nastaveny s ohledem na typy akcí:

| Typ akce elektronické zprávy \ Typ odezvy  | Úspěšně provedeno  | Obchodní chyba  | Technická chyba  | Definovaný uživatelem  | Storno  |
|-------------------------------------------------|--------------|---------|-------|-----|-----------------|
| Vytvořit zprávu                                  | X            |         |       |     |                 |
| Export elektronického výkaznictví                     | X            |         |       |     |                 |
| Import elektronického výkaznictví                     |              |         |       |     |                 |
| Webová služba                                     | X            |         | X     |     |                 |
| Zpracování uživatele                                 |              |         |       |     |                 |
| Úroveň spuštění zprávy                         |              |         |       |     |                 |
| Naplnit záznamy                                |              |         |       |     |                 |
| Úroveň spuštění položky zprávy                    |              |         |       |     |                 |
| Požádat o ověření                            | X            |  X      | X     |     |                 |
| Zpráva exportu elektronického výkaznictví             | X            |         |       |     |                 |
| Zpracování uživatele na úrovni zprávy                   |              |         |       |     |                 |

### <a name="electronic-message-processing"></a>Zpracování elektronické zprávy

Zpracování elektronických zpráv je základním konceptem funkčnosti elektronických zpráv. Agreguje akce, které by měly být vyhodnocovány pro elektronickou zprávu. Akce lze propojit prostřednictvím počátečního stavu a výsledného stavu. Popřípadě lze spustit akce **Zpracování uživatele** samostatně. Na stránce **Zpracování elektronických zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Zpracování elektronických zpráv**), můžete také vybrat další pole, která mají být podporována pro zpracování buď na úrovni zprávy nebo položek zprávy.

Záložka s náhledem **Akce** umožňuje přidat předdefinované akce ke zpracování. Můžete určit, zda má být akce spuštěna odděleně, nebo zda může být zahájena zpracováním. Chcete-li definovat, zda akce může být inicializována pouze uživatelem, označte zaškrtávací políčko **Spustit odděleně** pro akci ve zpracování. Pokud chcete, aby byla akce spuštěna zpracováním, když jsou zprávy nebo položky zpráv ve stavu definovaném jako počáteční stav této akce, zrušte označení parametru **Spustit samostatně**. Akce typu **Akce uživatele** musí být spuštěna samostatně. 

Někdy může být nutné agregovat několik akcí do posloupnosti, i když je první z nich definována tak, aby byl spuštěna odděleně. Když je například požadováno, aby generování sestavy bylo inicializováno uživatelem, ale jakmile je vygenerovaná zpráva, musí být okamžitě odeslána webové službě a odpověď z webové služby musí být v systému zohledněna. Pro takový účel můžete použít **neoddělitelnou posloupnost**. Chcete-li tak učinit, klikněte na tlačítko**Neoddělitelná posloupnost** v podokně akcí na záložce s náhledem **Akce** stránky **Zpracování elektronické zprávy**, vytvořte posloupnost a vyberte ji ve sloupci **Neoddělitelná posloupnost** pro ty akce, které je nutné spustit vždy společně. První akci v tomto případě lze nastavit jako **Spustit samostatně**, ale všechny ostatní nikoliv.

Záložka s náhledem **Další pole položky zprávy** umožňuje přidat předdefinovaná další pole, která souvisí s položkami zpráv. Musíte přidat další pole pro každý typ položky zprávy, k níž se tato pole vztahují.

Záložka s náhledem **Další pole položky zprávy** umožňuje přidat předdefinovaná další pole, která souvisí se zprávami.

Záložka s náhledem **Role zabezpečení** umožňuje nastavit role zabezpečení, které jsou předem definovány v systému pro konkrétní zpracování. Uživatelé, kteří mají určitou roli, uvidí pouze zpracování, které je definováno pro danou roli.

Záložka s náhledem **Dávka** umožňuje nastavit zpracování tak, aby fungovalo v režimu dávky.

## <a name="work-with-electronic-messages-functionality"></a>Práce s funkcemi elektronických zpráv

Při práci na úrovni zprávy je užitečnější stránka **Elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Elektronické zprávy**). Při práci na úrovni sbírání dat (položky zprávy) je užitečnější stránka **Položky elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Položky elektronické zprávy**).

### <a name="electronic-messages"></a>Elektronické zprávy

Stránka **Elektronické zprávy** představuje zpracování, které je vám dostupné na základě vaší role. Role zabezpečení jsou přidruženy ke zpracování v jeho nastavení. Pro každé zpracování, které je vám k dispozici, stránka zobrazuje elektronické zprávy a informace, které s nimi souvisejí.

Pevná záložka **Zprávy** zobrazuje elektronické zprávy pro vybrané zpracování. V závislosti na stavu vybrané zprávy a předdefinovaném zpracování můžete některé akce provést výběrem tlačítek nad mřížkou:

- **Nový** – Toto tlačítko je přidruženo k akcím typu **Vytvoření zprávy**.
- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené zprávy.
- **Shromažďovat data** -Toto tlačítko je přidružen k akci typu **Naplnit záznamy**.
- **Generovat sestavu** – Toto tlačítko je přidruženo k akcím typu **Zpráva exportu elektronického výkaznictví**.
- **Odeslat sestavu** – Toto tlačítko je přidruženo k akcím typu **Webová služba**.
- **Importovat odezvu** – Toto tlačítko je přidruženo k akcím typu **Import elektronického výkaznictví**.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele na úrovni zprávy**.
- **Položky zprávy** – Otevřete stránku **Pokožky elektronické zprávy**.

Záložka s náhledem **Protokol akce** zobrazuje informace o všechny akcích spuštěných pro vybranou zprávu. Pokud akce vyústila v chybu, budou informace o chybě připojeny k příslušnému řádku protokolu akcí. Vyberte řádek a klikněte na tlačítko **sponky** v pravém horním rohu stránky, abyste zkontrolovali informace o chybě.

Záložka s náhledem **Další pole zprávy** zobrazuje všechna další pole, která jsou definována pro zprávy v nastavení zpracování. Také jsou zde uvedeny hodnoty těchto polí.

Záložka s náhledem **Položky zprávy** zobrazuje všechny položky zpráv související s vybranou zprávou. Pro každou položku zprávy lze použít následující funkci v závislosti na stavu této položky zprávy:

- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené položky zprávy.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele**.
- **Původní dokument** - Toto tlačítko umožňuje uživateli otevřít stránku s původním dokumentem vybrané zprávy.

Můžete zkontrolovat všechny přílohy pro vybranou zprávu. Tyto přílohy jsou sestavy, které již byly vygenerovány a přijaty. Vyberte zprávu pro kontrolu příloh a poté vyberte tlačítko **Příloha** v podokně akcí.

![Tlačítko Příloha](media/attachment-icon.png)

Stránka **Přílohy** zobrazuje všechny přílohy, které souvisí se zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

![Tlačítko Otevřít](media/open-button.png)

Chcete-li zkontrolovat přílohu, která se vztahuje ke konkrétní akci, která byla dříve spuštěna pro zprávu, vyberte zprávu na stránce **Elektronické zprávy** a poté na záložce s náhledem **Protokol akce** vyberte akci. Pak vyberte tlačítko **Příloha** v podokně akcí.

Můžete také spustit buď celé zpracování nebo pouze určitou akci výběrem možnosti **Spustit zpracování** v podokně akcí.

### <a name="electronic-message-items"></a>Položky elektronické zprávy

Stránka **Položky elektronické zprávy** představuje všechny položky zprávy a protokol akcí, které byly spuštěny pro každou položku zprávy. Zobrazuje také další pole definovaná pro položky zprávy a hodnoty těchto dalších polí.

Následující tabulka popisuje pole na kartě **Položky zprávy**.

<table>
<thead>
<tr>
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Zpracování</td>
<td>Název zpracování použitý k vytvoření položky zprávy.</td>
</tr>
<tr>
<td>Položka zprávy</td>
<td>ID položky zprávy. Toto ID je přiřazeno automaticky na základě číselné řady <strong>Položky zprávy</strong>, která je definována na stránce <strong>Parametry hlavní knihy</strong>.</td>
</tr>
<tr>
<td>Datum položky zprávy</td>
<td>Datum vytvoření položky zprávy.</td>
</tr>
<tr>
<td>Typ položky zprávy</td>
<td>Typ položky zprávy. Několik typů položek zpráv lze nastavit pro stejné zpracování (například <strong>Příchozí faktury</strong> a <strong>Odchozí faktury</strong>). Toto pole může být vyplněno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Stav položky zprávy</td>
<td>Skutečný stav položky zprávy. Dostupné stavy se liší v závislosti na typu položky zprávy. Několik příkladů:
<ul>
<li><strong>Naplněno</strong> – Záznam byl přidán do tabulky položek zprávy.</li>
<li><strong>Vyhodnoceno</strong> – Další atributy byly vypočteny pro položku zprávy.</li>
<li><strong>Vykázáno</strong> – Položka zprávy byla úspěšně přidána do sestavy.</li>
<li><strong>Vyloučeno</strong> – Tento stav lze využít, pokud musíte vyloučit některé položky zprávy ze sestavy před jejich exportem.</li>
</ul>
</td>
</tr>
<tr>
<td>Datum přenosu</td>
<td>Pro zpracování, které automaticky přenáší vygenerovanou sestavu mimo systém, je to datum, kdy byla položka zpráva přenesena.</td>
</tr>
<tr>
<td>Číslo dokumentu</td>
<td>Toto pole se vyplní automaticky na základě nastavení akce naplnění záznamů. Toto pole může být vyplněno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Číslo účtu</td>
<td>Číslo účtu odběratele nebo dodavatele (nebo jiná hodnota pole, v závislosti na poli, které je definováno pro akci <strong>Naplnit záznamy</strong>). Toto pole může být vyplněno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Zpráva</td>
<td>Číslo zprávy. Toto číslo je přiřazeno automaticky na základě číselné řady <strong>Zpráva</strong>, která je definována na stránce <strong>Parametry hlavní knihy</strong>.</td>
</tr>
<tr>
<td>Stav zprávy</td>
<td>Skutečný stav elektronické zprávy.</td>
</tr>
<tr>
<td>Další akce</td>
<td>Další akce, které lze spustit pro aktuální stav položky zprávy.</td>
</tr>
</tbody>
</table>

Karta **Další pole** zobrazuje další pole pro vybranou položku zprávy a jejich hodnoty.

#### <a name="run-processing"></a>Spustit zpracování

Vyberte **Spustit zpracování** v podokně akcí a spustíte zpracování pro položky zprávy. Ke spuštění určité akce nastavte v dialogovém okně **Spustit zpracování** možnost **Vybrat akci** na **Ano** a pak vyberte akci. Ke spuštění celého zpracování ponechte možnost **Vybrat akci** nastavenou na **Ne**.

#### <a name="generate-report"></a>Generovat sestavu

Vyberte **Generovat sestavu** v podokně akcí pro vygenerování sestavy. Toto tlačítko je přidruženo k akcím typu **Export elektronického výkaznictví**.

#### <a name="update-status"></a>Aktualizovat stav

Vyberte **Aktualizovat stav** v podokně akcí pro aktualizaci stavu jedné nebo více položek zprávy. V dialogovém okně **Aktualizovat stav** použijte záložku s náhledem **Záznamy k zahrnutí** a vyberte položky zprávy pro aktualizaci. Ujistěte se, že jste správně definovali kritéria výběru, protože stavy položky zprávy budou aktualizovány podle těchto kritérií, počátečního stavu vybrané akce a hodnoty **Nový stav**, kterou nastavíte. Po dokončení aktualizace stavu bude obtížné určit, které položky byly právě aktualizovány.. Proto bude obtížné vrátit zpět aktualizace stavu.

#### <a name="electronic-messages"></a>Elektronické zprávy

Vyberte **Elektronická zpráva** v podokně akcí a zkontrolujte elektronickou zprávu, která souvisí s vybranou položkou zprávy.

Můžete také zkontrolovat všechny soubory, které odpovídají položce zprávy. Vyberte pole **Zpráva** položky zprávy nebo vyberte **Elektronická zpráva** v podokně akcí. Na stránce **Elektronická zpráva** vyberte zprávu, pro kterou zkontrolujete sestavu, a pak vyberte tlačítko **Příloha** v podokně akcí.

![Tlačítko Příloha](media/attachment-icon.png)

Stránka **Přílohy** zobrazuje všechny přílohy, které souvisí se zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

![Tlačítko Otevřít](media/open-button.png)

#### <a name="original-document"></a>Původní dokument

Vyberte **Původní dokument** v podokně akcí a otevřete původní dokument pro vybranou položku zprávy.

## <a name="example"></a>Příklad

Po vytvoření formátu elektronického výkaznictví, jeho namapování na datové zdroje jeho dokončení ho můžete spustit pomocí pracovního prostoru **Elektronické výkaznictví**. Vygeneruje se sestava, kterou můžete uložit místně.

Chcete-li řídit následující aspekty procesu vykazování, musíte nastavit zpracování elektronických zpráv:

- Zaprotokolování informací o tom, kdo vygeneroval sestavu.
- Zaprotokolování času, kdy byla sestava vygenerována.
- Uložte sestavy, které byly vygenerovány za předchozí období.

Tato část poskytuje příklad, který vám ukáže, jak nastavit funkci elektronických zpráv pro vytvoření procesu vykazování.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Nastavení a spuštění zpracování pro volání jednoduchého formátu elektronického výkaznictví pro vygenerování sestavy v aplikaci Excel

Tato část obsahuje příklad, který ukazuje, jak můžete nastavit elektronické zprávy a vygenerovat sestavu založenou na formátu exportu elektronického výkaznictví pro aplikaci Excel. Abyste mohli postupovat podle tohoto příkladu, formát exportu elektronického výkaznictví v Excelu musí být již vytvořen, namapován na zdroje dat a dokončen. Číselná řada již musí být nastavena pro elektronické zprávy.

Při vytváření zpracování je užitečné, pokud nejprve definujete akce a stavy zpracování, které budou vytvořeny. Následující obrázek znázorňuje, jak vypadá zpracování v tomto příkladu.

![Schéma zpracování](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Vytvoření stavů zpráv

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Stavy zprávy**.
2. Vytvořte následující stavy zprávy:

    - Nová
    - Připraveno
    - Vytvořeno

    ![Stavy zpráv](media/message-statuses.png)

3. Na řádku stavu **Nový** vyberte zaškrtávací políčko **Povolit odstranění** a umožněte uživatelům odstranit zprávy s tímto stavem.

#### <a name="create-additional-fields"></a>Vytvoření dalších polí

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Další pole**.
2. Přidejte další pole a jeho hodnoty. Následuje příklad.

    ![Dodatečná pole](media/additional-fields.png)

3. Nastavte možnost **Úpravy uživatele** na **Ano**, čímž umožníte uživatelům upravit pole.

#### <a name="create-message-processing-actions"></a>Vytvoření akcí zpracování zprávy

V tomto příkladu vytvoříte následující akce:

- **Vytvořit zprávu**
- **Aktualizovat na Připraveno**
- **Generovat sestavu**
- **Aktualizovat na počáteční stav** (volitelné)

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Akce zpracování zprávy**.
2. Vytvořte akci, která se nazývá **Vytvořit zprávu**. Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Vytvořit zprávu**.
3. Vytvořte akci, která se nazývá **Aktualizovat na Připraveno**a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Nový**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Připraveno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

4. Vytvořte akci, která se nazývá **Generovat sestavu**a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Export elektronického výkaznictví**. V poli **Mapování formátu** vyberte formát exportu elektronického výkaznictví. Možnosti jsou **Excel**, **XML**, **JSON**, **Text** a **Jiné**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Připraveno**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Vygenerováno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

    ![Generování akce sestavy](media/generate-report-action.png)

5. Volitelné: Abyste umožnili uživatelům vygenerovat sestavu několikrát, můžete vytvořit akci **Aktualizovat na počáteční stavu** a nastavit následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Vygenerováno**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Připraveno** nebo (a) **Nový**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

#### <a name="electronic-message-processing"></a>Zpracování elektronické zprávy

V tomto příkladu by všechny akce měly být nastaveny tak, aby se spouštěly samostatně. Předpokladem je, že každá akce bude inicializována uživatelem.

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Zpracování elektronické zprávy**.
2. Přidejte záznam pro zpracování a přidejte všechny dříve definované akce a další pole.
3. Volitelné: Na záložce s náhledem **Role zabezpečení** definujte role zabezpečení pro vaše zpracování, abyste omezili přístup ke konkrétnímu vykazování.
4. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
5. Zvolte **Nová** pro vytvoření zprávy. Nyní můžete přidat data a popis. Můžete také aktualizovat hodnotu dalšího pole podle potřeby.

    ![Vytvoření elektronické zprávy](media/create-electronic-message.png)

Mřížka na záložce s náhledem **Protokol akce** je automaticky vyplněna protokolem všech akcí, které jsou provedeny na zprávě.

Nyní můžete buď odstranit nebo aktualizovat stav zprávy. Pokud chcete aktualizovat stav zprávy, vyberte **Aktualizovat stav**a poté v poli **Nový stav** vyberte **Připraveno**. Pak vyberte **OK**.

![Aktualizace stavu zprávy](media/update-status.png)

Stav zprávy je aktualizován na **Připraveno** a nyní můžete vygenerovat sestavu výběrem možnosti **Generovat sestavu**. Sestava se vygeneruje a aktualizuje se stav zprávy a protokol akce. Chcete-li zobrazit vygenerovanou sestavu, zvolte tlačítko **Příloha** v podokně akcí.
