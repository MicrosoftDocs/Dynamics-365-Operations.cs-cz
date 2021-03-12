---
title: Elektronické zprávy
description: Toto téma poskytuje přehled a informace o nastavení pro elektronické zprávy v Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d4ecc29e47d68129df424c4212505413cf6c8889
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968972"
---
# <a name="electronic-messaging"></a>Elektronické zprávy

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled a informace o nastavení pro elektronické zprávy.

Nedávno vlády a legislativní orgány různých zemí a regionů na celém světě zavedly požadavky na podávání zpráv pro společnosti, které jsou registrovány v těchto zemích nebo regionech. Účelem požadavků je umožnit získávání údajů z těchto společností v elektronickém formátu přímo ze systémů, kde byly účtovány, uloženy a zpracovány.

Funkce elektronických zpráv v aplikaci Finance podporuje různé procesy elektronické spolupráce mezi aplikací Finance a systémy, které vlády a legislativní orgány nabízejí pro podávání zpráv, předkládání a přijímání oficiálních informací

Funkce elektronických zpráv je integrována s modulem **Elektronického výkaznictví**. Můžete tedy nastavit formáty elektronického výkaznictví pro elektronické zprávy. Další informace získáte v tématu [Elektronické výkaznictví](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektronické zprávy jsou založeny na následujících entitách:

- **Elektronická zpráva** – Sestava nebo prohlášení, které mají být vykázány anebo přenášeny interně. Příkladem jsou sestavy, které jsou odesílány daňovému úřadu.
- **Položky elektronických zpráv** – Záznamy, které mají být zahrnuty ve vykazované zprávě.
- **Zpracování elektronické zprávy** – Sled akcí, buď propojený nebo odpojený, který by měl být spuštěn pro shromažďování požadovaných dat, generování sestav, ukládání dat do úložiště objektů blob Microsoft Azure, přenos sestav mimo systém, získání odpovědí mimo systém a aktualizace databáze. Akce v řetězci mohou být buď propojeny nebo nepropojeny

Následující obrázek znázorňuje tok dat pro elektronické zprávy.

![Tok dat elektronických zpráv](media/electronic-messaging-data-flow.png)

Funkce elektronických zpráv podporuje následující situace:

- Ruční vytváření zpráv a generování sestav založených na přidružených exportních formátech elektronického výkaznictví různých typů: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, text a Microsoft Word.
- Automatické vytvoření a zpracování zpráv, které jsou založeny na informacích požadovaných a přijatých od úřadu prostřednictvím přidruženého formátu importu elektronického výkaznictví.
- Sběr a zpracování informací z datového zdroje jako položek zprávy. Zdrojem dat je tabulka Finance.
- Ukládání dalších informací a vyhodnocování různých hodnot voláním specificky definovaných spustitelných tříd ve vztahu ke zprávám nebo položkám zpráv.
- Agregování informací, které jsou shromážděny v položkách zprávy, rozdělení těchto informací podle zprávy a generování sestav v přidružených exportních formátech elektronického výkaznictví.
- Přenesení sestav, které jsou generovány do webové služby pomocí informací o zabezpečení uložených v Azure Key Vault.
- Příjem odpovědi z webové služby, vyhodnocení odpovědi a aktualizace dat v aplikaci Finance podle potřeby.
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

Nastavte číselné řady pro zprávy a položky zprávy. Číselné řady se používají k automatickému číslování zpráv a položek zpráv. Čísla, která se použije jako jedinečné identifikátory zpráv a položek zpráv v systému. Můžete nastavit číselné řady pro elektronické zprávy na stránce **Parametry hlavní knihy** (**Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**).

### <a name="message-item-types-and-statuses"></a>Stavy a typy položek zprávy

Typy položek zpráv určují typy záznamů, které budou použity v elektronických zprávách. Můžete nastavit typy položek zpráv na stránce **Typy položek zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Typy položek zpráv**).

Stavy položek zpráv určují stavy, které se budou vztahovat na položky zpráv při zpracování, které nastavujete. Můžete nastavit stavy položek zpráv na stránce **Stavy položek zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy položek zpráv**).

Parametr **Povolit odstranění** stavu položky zprávy určuje, zda uživatelům bude povoleno odstranění položek zprávy v tomto stavu prostřednictvím stránky **Elektronické zprávy** nebo stránky **Položky elektronických zpráv**.

### <a name="message-statuses"></a>Stavy zpráv

Nastavte stavy zpráv, které by měly být k dispozici při zpracování zprávy. Můžete nastavit stavy zprávy na stránce **Stavy zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy zpráv**).

Následující tabulka popisuje pole na stránce **Stavy zprávy**.

| Název pole          | Popis |
|---------------------|-------------|
| Stav zprávy      | Zadejte jedinečný název stavu zprávy. Stavy zprávy slouží k určení stavu elektronická zprávy v každém okamžiku. Název, který zadáte, se zobrazí na stránce **elektronické zprávy** stránky a v protokolu, který s elektronickými zprávami souvisí. |
| Popis         | Zadejte popis vybraného stavu zprávy. |
| Typ odezvy       | Vyberte typ odpovědi stavu zprávy. Některé akce zpracování mohou mít více než jeden typ odezvy. Například akce typu **Webová služba** mohou vyústit buď v typ odpovědi **Úspěšně provedeno** nebo **Technická chyba** v závislosti na výsledku spuštění. V takovém případě musíte definovat stav zprávy pro oba typy odezvy. Další informace o typech akcí a s nimi souvisejících typech odezvy získáte v tématu [Typy akcí zpracování zpráv](#message-processing-action-types). |
| Stav položky zprávy | Někdy musí mít stav elektronické zprávy ovlivňovat stav souvisejících položek zprávy. Vyberte stav zprávy položky v tomto poli, abyste ji mohli přidružit ke stavu zprávy. |
| Odstranit vše        | Toto políčko zaškrtněte, pokud uživatelé budou moci odstranit elektronické zprávy s tímto stavem na stránce **elektronické zprávy**. |

### <a name="additional-fields"></a>Dodatečná pole

Funkce elektronických zpráv umožňuje naplnit záznamy z transakční tabulky. Tímto způsobem lze připravit záznamy pro vykazování a poté je vykázat. Transakční tabulky však někdy nemají dostat informací pro vyplnění záznamů způsobem, který splňuje požadavky na výkazy. Můžete vyplnit všechny informace, které musí být vykázány pro záznam nastavením dalších polí. Další pole lze přidružit ke zprávám i položkám zpráv. Můžete nastavit další pole na stránce **Další pole** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Další pole**).

Následující tabulka popisuje obecná pole na stránce **Další pole**.

| Pole       | Popis |
|-------------|-------------|
| Název pole  | Zadejte název dalšího atributu položek zprávy, které se vztahují k procesu. Tento název se zobrazí v uživatelském rozhraní (UI) při práci s procesem. Lze jej rovněž použít v konfiguracích elektronického výkaznictví, které se vztahují k procesu. |
| Popis | Zadejte popis dalšího pole. |
| Úpravy uživatele   | Nastavte tuto možnost **Ano**, pokud by uživatelé měli mít možnost změnit hodnotu dalšího pole z UI. |
| Počitadlo     | Nastavte tuto možnost na **Ano**, pokud další pole mělo obsahovat číselnou řadu v elektronické zprávě. Hodnota dalšího pole se vyplní automaticky při spuštění akce typu **Export elektronického výkaznictví**. |
| Skryté      | Nastavte možnost na **Ano**, pokud má být další pole skryto v uživatelském rozhraní. |

Každé další pole může mít pro zpracování odlišné hodnoty. Tyto hodnoty můžete definovat na pevné záložce **Hodnoty**. Následující tabulka obsahuje popis polí.

| Pole                | Popis |
|----------------------|-------------|
| Hodnota pole          | Zadejte hodnotu pole pro použití ve vztahu ke zprávě nebo položce zprávy při vykazování. |
| Popis          | Zadejte popis hodnoty pole. |
| Typ účtu         | Některé hodnoty polí mohou být omezeny na určité typy účtů. Vyberte jednu z následujících hodnot: **Všechny**, **Odběratel**, nebo **Dodavatel**. |
| Kód účtu         | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu**, můžete dále omezit použití hodnot pole na konkrétní skupinu nebo tabulku. |
| Číslo účtu/skupiny | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu** a zadali jste skupinu nebo tabulku do pole **Kód účtu**, můžete v tomto poli zadat určitou skupinu nebo protistranu. |
| Účinné:            | Zadejte datum, kdy má být hodnota zahájena ke zvažovaní. |
| Vypršení platnosti           | Zadejte datum, kdy má být hodnota ukončena pro zvažování. |

Ve výchozím nastavení kombinací kritérií, která jsou definována podle polí **číslo účtu/skupiny**, **kódu účtu**, **data platnosti**, a **vypršení platnosti** neovlivňují výběr hodnot pro Další pole. Avšak používání těchto kombinací lze použít ve spustitelné třídě k implementaci konkrétní logiky, která vypočítá hodnotu pro další pole.

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

Některé spustitelné třídy mohou mít povinné parametry, které musí být definovány před prvním spuštěním spustitelné třídy. K definování těchto parametrů vyberte **parametry** v podokně akcí, nastavte pole v dialogovém okně, které se zobrazí a poté vyberte **OK**. Je důležité, abyste vybrali **OK**. V opačném případě parametry nebudou uloženy v databázi a třída spustitelného souboru nebude správně volána.

### <a name="populate-records-actions"></a>Akce naplnění záznamů

Použijete akce naplnění záznamů nastavení akcí, které přidávají záznamy do tabulky položek zpráv tak, aby mohly být přidány do elektronické zprávy. Například pokud vaše elektronická zpráva musí vykazovat faktury odběratele, je nutné nastavit akci Naplnit záznamy, která je propojena s polem **Zdroj dat** v tabulce Deník faktur odběratele. Můžete nastavit akce naplnění záznamů na stránce **Akce naplnění záznamů** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce naplnění záznamů**). Vytvořte nový záznam pro každou akci, která by měla přidat záznamy do tabulky, a nastavte následující pole.

| Pole       | Popis |
|-------------|-------------|
| Název        | Zadejte název akce, která naplní záznamy ve vašem procesu. |
| Popis | Zadejte popi akce zadání záznamů. |

Na záložce s náhledem **Nastavení datových zdrojů** přidejte řádek pro každý datový zdroj, který se používá pro proces, a nastavte následující pole.

| Pole                  | Popis |
|------------------------|-------------|
| Jméno                   | Zadejte název pro datový zdroj. |
| Typ položky zprávy      | Vyberte typ položky zprávy, která by měla být použita při vytváření záznamů pro datový zdroj. |
| Typ účtu           | Vyberte typ účtu, který má být přiřazen k záznamům z datového zdroje. |
| Název hlavní tabulky      | Vyberte tabulku, která má být zdrojem dat. |
| Pole čísla dokumentu  | Zvolte pole, ze kterého má být číslo dokumentu převzato ve vybrané tabulce. |
| Pole data dokumentu    | Zvolte pole, ze kterého má být datum dokumentu převzato ve vybrané tabulce. |
| Pole účtu dokumentu | Zvolte pole, ze kterého má být účet dokumentu převzat ve vybrané tabulce. |
| Dotaz uživatele             | Je-li toto políčko zaškrtnuto, můžete nastavit dotazu výběrem možností **Upravit dotaz** nad mřížkou. V opačném případě budou všechny záznamy vyplněny z vybraného datového zdroje. |

### <a name="web-applications"></a>Webové aplikace

Nastavení webové aplikace můžete použít tak, aby podporovala otevřené autorizace (OAuth) 2.0. OAuth je otevřený standard, který umožňuje uživatelům udělit zabezpečeného delegovaného přístupu k aplikaci jejich jménem bez sdílení pověření pro přístup. Z této stránky můžete také projít procesem autorizace získáním autorizačního kódu a přístupového tokenu. Můžete provést nastavení webové aplikace na stránce **Webové aplikace** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Webové aplikace**) .

Následující tabulka popisuje pole na stránce **Webové aplikace**.

| Pole                        | Popis |
|------------------------------|-------------|
| Název aplikace             | Zadejte název webové aplikace. |
| Popis                  | Zadejte popis webové aplikace. |
| Základní adresa URL                     | Zadejte základní internetovou adresu webové aplikace. |
| URL cesta autorizace       | Zadejte cestu k vytvoření adresy URL pro autorizaci. |
| URL cesta tokenu               | Zadejte cestu k vytvoření adresy URL pro token. |
| Přesměrovací adresa URL                 | Zadejte přesměrovací adresu URL. |
| ID klienta                    | Zadejte ID klienta webové aplikace. |
| Tajný klíč klienta                | Zadejte tajný klíč klienta webové aplikace. |
| Token serveru                 | Zadejte token serveru webové aplikace. |
| Mapování formátu autorizace | Vyberte formát ER, který bude použit ke generování požadavku na autorizaci. |
| Import mapování modelu tokenu   | Vyberte mapování modelu importu ER, který bude použit pro ukládání přístupového tokenu. |
| Garantovaný rozsah                | Rozsah udělený požadavku na aplikaci. Toto pole je automaticky aktualizováno. |
| Token přístupu vyprší za  | Zbývající čas před vypršením platnosti tokenu. | 
| Přijmout                       | Určete vlastnost **Accept** webové žádosti. Zadejte například **application/vnd.hmrc.1.0+json**. |
| Typ obsahu                 | Určete typ obsahu. Například zadejte **application/json**. |

Kromě toho jsou v podokně Akce na stránce **Webové aplikace** k dispozici následující tlačítka na podporu procesu ověřování:

- **Získání autorizačního kódu** - pro inicializaci autorizace webové aplikace.
- **Získat autorizační token** – pro inicializací získání přístupového tokenu.
- **Aktualizovat přístupový token** – pro obnovení přístupového tokenu.

Pokud je přístupový token k webové aplikaci uložený v databázi systému v zašifrovaném formátu, může být použit pro požadavky na webovou službu. Pro účely zabezpečení musí být přístup k přístupovému tokenu omezen pouze na ty role zabezpečení, kterým musí být umožněno tyto požadavky řešit. Pokud se uživatelé mimo skupinu zabezpečení pokusí řešit žádost, obdrží chybu oznamující, že nemají povoleno komunikovat prostřednictvím vybrané webové aplikace. Chcete-li nastavit role zabezpečení, které musí mít přístup k přístupovému tokenu, použijte pevnou záložku **Role zabezpečení** na stránce **Webové aplikace**. Pokud nejsou role zabezpečení definovány pro webovou aplikaci, může pouze správce systému spolupracovat pouze prostřednictvím této webové aplikace.

### <a name="web-service-settings"></a>Nastavení webové služby

Pomocí nastavení webových služeb nastavíte přímý přenos dat do webové služby. Můžete provést nastavení webové služby na stránce **Nastavení webové služby** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Nastavení webové služby**) .

Následující tabulka popisuje pole na stránce **Nastavení webové služby**.

| Pole                          | popis |
|--------------------------------|-------------|
| Webová služba                    | Zadejte název webové služby. |
| popis                    | Zadejte popis webové služby. |
| Internetová adresa               | Zadejte internetovou adresu webové služby. Je-li pro webovou službu zadána webová aplikace a internetová adresa by měla být stejná jako adresa definovaná pro vybranou webovou aplikaci, klikněte na tlačítko **Zkopírovat základní URL adresu** a zkopírujte dresu Základní adresu URL z webové aplikace do pole Internetová adresa webové služby. |
| Certifikát                    | Vyberte certifikát Key Vault, který byl již předtím nastaven. |
| Webová aplikace                | Vyberte certifikát Key Vault, který byl již předtím nastaven. |
| Typ odezvy – XML        | Nastavte tuto možnost na **Ano**, pokud je typ odpovědi XML. |
| Metoda požadavku                 | Zadejte způsob požadavku. HTTP definuje sadu metod požadavků, které označují akci, která by měla být provedena pro daný zdroj. Metodou požadavku může být **GET**, **POST**, nebo jiná metoda HTTP. |
| Záhlaví požadavku                | Určete záhlaví požadavku. Záhlaví požadavku je záhlaví HTTP, které lze použít v požadavku HTTP, a které nesouvisí s obsahem zprávy. |
| Přijmout                         | Určete vlastnost **Accept** webové žádosti. |
| Přijmout kódování                | Zadejte hodnotu **Accept-Encoding**. Záhlaví HTTP požadavku Accept-Encoding oznamuje kódování obsahu, které může klient pochopit. Toto kódování obsahu je obvykle algoritmus komprese. |
| Typ obsahu                   | Určete typ obsahu. Záhlaví HTTP entity Content-Type označuje typ média zdroje. |
| Úspěšný kód odpovědi       | Určete kód stavu HTTP označující, že požadavek byl úspěšný. |
| Mapování formátu záhlaví požadavku | Vyberte formát ER, který bude použit ke generování záhlaví webového požadavku. |

### <a name="message-processing-actions"></a>Akce zpracování zprávy

Pomocí akcí zpracování zpráv vytváříte akce pro své procesy a nastavujete jejich parametry. Můžete nastavit akce zpracování zpráv na stránce **Akce zpracování zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce zpracování zpráv**).

Následující tabulky popisují pole na stránce **Akce zpracování zpráv**.

#### <a name="general-fasttab"></a>Záložka s náhledem Obecné

| Pole                       | popis |
|-----------------------------|-------------|
| Typ akce                 | Vyberte typ akce. Informace o dostupných možnostech naleznete v části [Typy akcí zpracování zpráv](#message-processing-action-types). |
| Mapování formátu              | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví**, **Import elektronického výkaznictví** a **Zpráva exportu elektronického výkaznictví**. |
| Mapování formátu pro cestu URL | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Toto pole je k dispozici pouze pro akce typu **Webová služba**. Slouží k vytvoření cesty adresy URL, která bude přidána k základní internetové adrese zadané pro vybraný webový server. |
| Typ položky zprávy           | Vyberte typ záznamů, pro které by měla být akce vyhodnocována. Toto pole je k dispozici pro akce typu **Úroveň spuštění položky zprávy**, **Import elektronického výkaznictví** a **Export elektronického výkaznictví**, **Webová služba** a rovněž některé další typy. Necháte-li toto pole prázdné, vyhodnotí se všechny typy položek zpráv, které jsou definovány pro zpracování zpráv. |
| Spustitelná třída            | Vyberte nastavení spustitelné třídy, která již byla vytvořena. Toto pole je k dispozici pouze pro akce typu **Úroveň spuštění zprávy** a **Úroveň spuštění položky zprávy**. |
| Akce naplnění záznamů     | Vyberte akci naplnění záznamů, která již byla nastavena. Toto pole je k dispozici pouze pro akce typu **Naplnit záznamy**. |
| Webová služba                 | Vyberte webovou službu, která již byla nastavena. Toto pole je k dispozici pouze pro akce typu **Webová služba**. |
| Název souboru                   | Zadejte název souboru, který bude výsledkem akce. Tento soubor může být odezva na webový server nebo sestava, která je generována. Toto pole je k dispozici pouze pro akce typu **Webová služba** a **Zpráva exportu elektronického výkaznictví**. |
| Zobrazit dialogové okno                 | Nastavte tuto možnost na **Ano**, pokud musí být uživateli před vytvořením sestavy zobrazeno dialogové okno. Toto pole je k dispozici pouze pro akce typu **Zpráva exportu elektronického výkaznictví**. |

##### <a name="message-processing-action-types"></a>Typy akcí zpracování zprávy

Následující možnosti jsou dostupné v poli **Typ akce**.

- **Vytvořit zprávu** – Použití tohoto typu akce umožní uživatelům ručně vytvořit zprávy na stránce **Elektronická zpráva**. Počáteční stav nemůže být pro akci tohoto typu nastaven.
- **Naplnit záznamy** – Akce typu **Naplnit záznamy** musí být nastavena dříve. Tento typ akce přidružte k akci naplnění záznamů, aby bylo povoleno zahrnutí této akce do zpracování. Předpokládá se, že tento typ akce se používá buď pro první akci ve zpracování zprávy (pokud nebyla předem vytvořena žádná elektronická zpráva) nebo jako akce přidání položek zprávy do dříve vytvořené zprávy (akcí typu **Vytvořit zprávu**). Proto lze pro akci tohoto typu nastavit stav výsledků pouze položek zpráv. Lze nastavit počáteční stav pouze pro zprávy.
- **Úroveň spuštění zprávy** – Tento typ akce slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni zprávy.
- **Úroveň spuštění položky zprávy** – Tento typ akce slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni položky zprávy.
- **Export elektronického výkaznictví** – Použijte tento typ akce pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpráva exportu elektronického výkaznictví** – Použijte tento typ akce pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy (například když zpráva nemá žádné položky zprávy).
- **Import elektronického výkaznictví** – Použijte tento typ akce pro akce, které mají generovat sestavu, která je založena na importu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpracování uživatele na úrovni zprávy** – Tento typ akce použijte pro akce, které předpokládají některé ruční akce provedené uživatelem. Uživatel může například aktualizovat stav zpráv.
- **Zpracování uživatele** – Tento typ akce použijte pro akce, které předpokládají některé ruční akce provedené uživatelem. Uživatel může například aktualizovat stav položek zpráv.
- **Webová služba** – Tento typ akce použijte pro akce, které mají přenášet generovanou sestavu do webové služby. Tento typ akce není použit pro italské vykazování komunikace o prodejních a nákupních fakturách. Pro akce typu **Webová služba** obsahuje stránka **Akce zpracování zprávy** pevnou záložku **Různé detaily**, na níž lze zadat text potvrzení. Tento potvrzovací text se uživatelům zobrazí před vyřešením žádostí o vybranou webovou službu.
- **Požádat o ověření** – Použijte tento typ akce pro vyžádání ověření ze serveru.

#### <a name="initial-statuses-fasttab"></a>Záložka s náhledem Počáteční stavy

> [!NOTE]
> Záložka s náhledem **Počáteční stavy** není k dispozici pro akce, které mají počáteční typ akce **Vytvořit zprávu**.

| Pole               | Popis |
|---------------------|-------------|
| Stav položky zprávy | Vyberte stav položky zprávy, pro který by měla být vyhodnocena vybraná akce zpracování zpráv. |
| popis         | Popis vybraného stavu položky zprávy. |

#### <a name="result-statuses-fasttab"></a>Záložka s náhledem Výsledné stavy

| Pole               | popis |
|---------------------|-------------|
| Stav zprávy      | Vyberte stavy zprávy, pro který by měla být vyhodnocena vybraná akce zpracování zpráv. Toto pole je k dispozici pouze pro akce zpracování zpráv, které jsou vyhodnocovány na úrovni zprávy. Je například k dispozici pro akce typu **Export elektronického výkaznictví** a **Import elektronického výkaznictví**, ale není k dispozici pro akce **Zpracování uživatele** a **Úroveň provedení položky zprávy**. |
| popis         | Popis vybraného stavu zprávy. |
| Typ odezvy       | Typ odpovědi vybraného stavu zprávy. |
| Stav položky zprávy | Vyberte výsledné stavy, které by měly být k dispozici po vyhodnocení vybrané akce zpracování zpráv. Toto pole je k dispozici pouze pro akce zpracování zpráv, které jsou vyhodnocovány na úrovni položky zprávy. Například je k dispozici pro akce typu **Zpracování uživatele** a **Úroveň spuštění položky zprávy**. U akcí zpracování zpráv, které jsou vyhodnoceny na úrovni zprávy, toto pole zobrazuje stav položky zprávy, který byl nastaven pro vybraný stav zprávy. |

Následující tabulka ukazuje stavy výsledků, které musí být nastaveny pro různé akce a typy odezvy.

| Typ akce elektronické zprávy / Typ odezvy | Úspěšně provedeno | Obchodní chyba | Technická chyba | Definovaný uživatelem | Storno |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Vytvořit zprávu                               | X                     |                |                 |              |        |
| Export elektronického výkaznictví                  | X                     |                |                 |              |        |
| Import elektronického výkaznictví                  |                       |                |                 |              |        |
| Webová služba                                  | X                     |                | X               |              |        |
| Zpracování uživatele                              |                       |                |                 |              |        |
| Úroveň spuštění zprávy                      |                       |                |                 |              |        |
| Naplnit záznamy                             |                       |                |                 |              |        |
| Úroveň spuštění položky zprávy                 |                       |                |                 |              |        |
| Požádat o ověření                         | X                     | X              | X               |              |        |
| Zpráva exportu elektronického výkaznictví          | X                     |                |                 |              |        |
| Zpracování uživatele na úrovni zprávy                |                       |                |                 |              |        |

### <a name="electronic-message-processing"></a>Zpracování elektronické zprávy

Zpracování elektronických zpráv je základním konceptem funkčnosti elektronických zpráv. Agreguje akce, které by měly být vyhodnocovány pro elektronickou zprávu. Akce lze propojit prostřednictvím počátečního stavu a výsledného stavu. Popřípadě lze spustit akce **Zpracování uživatele** samostatně. Na stránce **Zpracování elektronických zpráv** (**Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Zpracování elektronických zpráv**), můžete také vybrat další pole, která mají být podporována pro zpracování buď na úrovni zprávy nebo položek zprávy.

Záložka s náhledem **Akce** umožňuje přidat předdefinované akce ke zpracování. Můžete určit, zda má být akce spuštěna odděleně, nebo zda může být zahájena zpracováním. Pro určení, zda může být inicializována akce ve zpracování zahájena pouze uživatelem, nastavte hodnotu v poli **spustit samostatně** na **Ano** pro danou akci. Pokud chcete, aby byla akce spuštěna zpracováním, když jsou zprávy nebo položky zpráv ve stavu definovaném jako počáteční stav této akce, nastavte v poli **Spustit samostatně** hodnotu **Ne**. Akce typu **Akce uživatele** musí být vždy spuštěna samostatně.

Několik operací musí být agregováno, a to i v případě, že je první akci nastavena tak, aby byla spouštěna samostatně. Uživatel musí například spustit generování sestavy, ale jakmile je vygenerovaná zpráva, musí být okamžitě odeslána webové službě a odpověď z webové služby musí být v systému zohledněna. V takovém případě můžete vytvořit neoddělitelnou sekvenci pro akce, které musejí být spojeny. Na pevné záložce **Akce** vyberte **Neoddělitelné skupiny** nad mřížkou a vyberte skupinu. Potom pro všechny akce, které musí běžet zároveň, vyberte pořadí v poli **Neoddělitelné pořadí**. V tomto případě může být pole **Spustit samostatně** nastaveno na **Ano** pro první akci v řadě, ale na **Ne** pro všechny akce.

Záložka s náhledem **Další pole položky zprávy** umožňuje přidat předdefinovaná další pole, která souvisí s položkami zpráv. Musíte přidat další pole pro každý typ položky zprávy, k níž se tato pole vztahují.

Záložka s náhledem **Další pole položky zprávy** umožňuje přidat předdefinovaná další pole, která souvisí se zprávami.

Záložka s náhledem **Role zabezpečení** umožňuje nastavit role zabezpečení, které jsou předem definovány v systému pro konkrétní zpracování. Uživatelé, kteří mají určitou roli, uvidí pouze zpracování, které je definováno pro danou roli.

Záložka s náhledem **Dávka** umožňuje nastavit zpracování tak, aby fungovalo v režimu dávky.

## <a name="work-with-the-electronic-messages-functionality"></a>Práce s funkcemi elektronických zpráv

Při práci na úrovni zprávy je užitečnější stránka **Elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Elektronické zprávy**). Při práci na úrovni sbírání dat (položky zprávy) je užitečnější stránka **Položky elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Položky elektronické zprávy**).

### <a name="electronic-messages"></a>Elektronické zprávy

Stránka **Elektronické zprávy** představuje zpracování, které je vám dostupné na základě vaší role. Role zabezpečení jsou přidruženy ke zpracování v jeho nastavení. Pro každé zpracování, které je vám k dispozici, stránka zobrazuje elektronické zprávy a informace, které s nimi souvisejí.

Pevná záložka **Zprávy** zobrazuje elektronické zprávy pro vybrané zpracování. V závislosti na stavu vybrané zprávy a předdefinovaném zpracování můžete některé akce provést výběrem tlačítek nad mřížkou:

- **Nový** – Toto tlačítko je přidruženo k akcím typu **Vytvoření zprávy**.
- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené zprávy.
- **Shromažďovat data** -Toto tlačítko je přidružen k akcím typu **Naplnit záznamy**.
- **Generovat sestavu** – Toto tlačítko je přidruženo k akcím typu **Zpráva exportu elektronického výkaznictví**.
- **Odeslat sestavu** – Toto tlačítko je přidruženo k akcím typu **Webová služba**.
- **Importovat odezvu** – Toto tlačítko je přidruženo k akcím typu **Import elektronického výkaznictví**.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele na úrovni zprávy**.
- **Položky zprávy** – Otevřete stránku **Pokožky elektronické zprávy**.

Záložka s náhledem **Protokol akce** zobrazuje informace o všechny akcích spuštěných pro vybranou zprávu. Pokud akce způsobila chybu, budou informace o chybě připojeny k příslušnému řádku protokolu akcí. Podrobné informace o chybě zobrazíte tak, že vyberete v mřížce řádek a vyberete tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

Záložka s náhledem **Další pole zprávy** zobrazuje všechna další pole, která jsou definována pro zprávy v nastavení zpracování. Také jsou zde uvedeny hodnoty těchto polí.

Záložka s náhledem **Položky zprávy** zobrazuje všechny položky zpráv související s vybranou zprávou. V závislosti na stavu vybrané položky zprávy a předdefinovaném zpracování můžete některé akce provést výběrem tlačítek nad mřížkou:

- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené položky zprávy.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele**.
- **Původní dokument** - Otevřete stránku obsahující původní dokument pro vybranou položku zprávy.

Všechny sestavy, které již byly generovány a přijaty pro zprávu, jsou připojeny k této zprávě. Pokud chcete zobrazit přílohy související se zprávou, vyberte zprávu a potom vyberte tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

![Tlačítko Příloha](media/attachment-icon.png)

Stránka **Přílohy** zobrazuje všechny přílohy, které souvisí s vybranou zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

![Tlačítko Otevřít](media/open-button.png)

Můžete také zkontrolovat přílohy, které se vztahují k určité akci, která byla provedena u předchozí zprávy. Na stránce **Elektronické zprávy** vyberte zprávu na pevné záložce **Zprávy**, vyberte akci na pevné záložce **protokol akcí** a vyberte tlačítko **Příloha** v pravém horním rohu stránky.

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
<td>Číslo účtu odběratele nebo dodavatele (nebo jiná hodnota pole, v závislosti na poli, které je definováno pro akci Naplnit záznamy). Toto pole může být vyplněno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
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

Vyberte **Spustit zpracování** v podokně akcí a spustíte zpracování pro položky zprávy. Ke spuštění určité akce nastavte v dialogovém okně **Spustit zpracování** možnost **Zvolit akci** na **Ano** a pak vyberte akci. Ke spuštění celého zpracování ponechte možnost **Zvolit akci** nastavenou na **Ne**.

#### <a name="generate-report"></a>Generovat sestavu

Vyberte **Generovat sestavu** v podokně akcí pro vygenerování sestavy. Toto tlačítko je přidruženo k akcím typu **Export elektronického výkaznictví**.

#### <a name="update-status"></a>Aktualizovat stav

Vyberte **Aktualizovat stav** v podokně akcí pro aktualizaci stavu jedné nebo více položek zprávy. V dialogovém okně **Aktualizovat stav** použijte záložku s náhledem **Záznamy k zahrnutí** a vyberte položky zprávy pro aktualizaci. Ujistěte se, že jste správně definovali kritéria výběru, protože stavy položky zprávy budou aktualizovány podle těchto kritérií, počátečního stavu vybrané akce a hodnoty **Nový stav**, kterou zadáte. Po dokončení aktualizace stavu bude obtížné určit, které položky byly právě aktualizovány. Proto bude obtížné vrátit zpět aktualizaci stavu.

#### <a name="electronic-messages"></a>Elektronické zprávy

Vyberte **Elektronické zprávy** v podokně akcí a zkontrolujte elektronickou zprávu, která souvisí s vybranou položkou zprávy.

Můžete také zkontrolovat všechny soubory, které odpovídají konkrétní položce zprávy. Vyberte pole **Zpráva** položky zprávy nebo vyberte **Elektronické zprávy** v podokně akcí. Potom na stránce **Elektronická zpráva** vyberte zprávu, jejíž soubory chcete zkontrolovat, a potom vyberte tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

![Tlačítko Příloha](media/attachment-icon.png)

Stránka **Přílohy** zobrazuje všechny přílohy, které souvisí se zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

![Tlačítko Otevřít](media/open-button.png)

#### <a name="original-document"></a>Původní dokument

Vyberte **Původní dokument** v podokně akcí a otevřete původní dokument pro vybranou položku zprávy.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Příklad: Nastavení a spuštění zpracování pro volání jednoduchého formátu elektronického výkaznictví pro vygenerování sestavy v aplikaci Excel

Po vytvoření formátu elektronického výkaznictví, jeho namapování na datové zdroje jeho dokončení ho můžete spustit pomocí pracovního prostoru **Elektronické výkaznictví**. Vygeneruje se sestava, kterou můžete uložit místně.

Chcete-li řídit následující aspekty procesu vykazování, musíte nastavit zpracování elektronických zpráv:

- Zaprotokolování informací o tom, kdo vygeneroval sestavu.
- Zaprotokolujte informace o tom, kdo vygeneroval sestavu.
- Uložte sestavy, které byly vygenerovány za předchozí období.

Tato část obsahuje příklad, který ukazuje, jak můžete nastavit elektronické zprávy a vygenerovat sestavu založenou na formátu exportu elektronického výkaznictví pro aplikaci Excel. Pokud chcete postupovat podle tohoto příkladu, formát exportu elektronického výkaznictví v Excelu musí být již vytvořen, namapován na zdroje dat a dokončen. Dále platí, že číselná řada již musí být nastavena pro elektronické zprávy.

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
3. Vytvořte akci, která se nazývá **Aktualizovat na Připraveno** a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Nový**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Připraveno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

4. Vytvořte akci, která se nazývá **Generovat sestavu** a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Export elektronického výkaznictví**. V poli **Mapování formátu** vyberte formát exportu elektronického výkaznictví. Možnosti jsou **Excel**, **XML**, **JSON**, **Text** a **Jiné**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Připraveno**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Vygenerováno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

    ![Generování akce sestavy](media/generate-report-action.png)

5. Volitelné: Abyste umožnili uživatelům vygenerovat sestavu několikrát, můžete vytvořit akci **Aktualizovat na počáteční stavu** a nastavit následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Vygenerováno**.
    - Na pevné záložce **Výsledně stavy** přidejte samostatný řádek pro každý ze dvou stavů zprávy (**Připraveno** a **Nový**). Pro oba řádky nastavte pole **typ odezvy** na **úspěšně spuštěno**.

#### <a name="electronic-message-processing"></a>Zpracování elektronické zprávy

V tomto příkladu by všechny akce měly být nastaveny tak, aby se spouštěly samostatně. Předpokladem je, že každá akce bude inicializována uživatelem.

1. Přejděte na **Daň \> Nastavení \> Elektronické zprávy \> Zpracování elektronické zprávy**.
2. Přidejte záznam pro zpracování a přidejte všechny dříve definované akce a další pole.
3. Volitelné: Na záložce s náhledem **Role zabezpečení** definujte role zabezpečení pro vaše zpracování, abyste omezili přístup ke konkrétnímu vykazování.
4. Přejděte na **Daň \> Dotazy a sestavy \> Elektronické zprávy \> Elektronické zprávy**.
5. Zvolte **Nová** pro vytvoření zprávy. Nyní můžete přidat data a popis. Můžete také aktualizovat hodnotu dalšího pole podle potřeby.

    ![Vytvoření elektronické zprávy](media/create-electronic-message.png)

Mřížka na záložce s náhledem **Protokol akce** je automaticky vyplněna protokolem všech akcí, které jsou provedeny na zprávě.

Nyní můžete buď odstranit nebo aktualizovat stav zprávy. Chcete-li aktualizovat stav zprávy, vyberte **Aktualizovat stav**. V poli **nový stav** vyberte **Připraveno** a poté vyberte **OK**.

![Aktualizace stavu zprávy](media/update-status.png)

Stav zprávy je aktualizován na **Připraveno** a nyní můžete vygenerovat sestavu výběrem možnosti **Generovat sestavu**. Sestava se vygeneruje a aktualizuje se stav zprávy a protokol akce. Chcete-li zobrazit generovanou sestavu, vyberte tlačítko **Příloha** (ikona papírové svorky) v pravém horním rohu stránky.
