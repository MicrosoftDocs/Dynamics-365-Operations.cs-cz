---
title: Nastavení elektronických zpráv
description: Toto téma poskytuje informace o tom, jak nastavit funkce elektronických zpráv (EM).
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 947170d1db132ca5a6b7caed0e47ee814b9148cc
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433767"
---
# <a name="set-up-electronic-messages"></a>Nastavení elektronických zpráv

[!include [banner](../includes/banner.md)]

Funkce **Elektronické zprávy** (EM) vám pomůže udržovat různé procesy elektronického výkaznictví pro různé typy dokumentů. V některých komplexních scénářích, které podporují [funkce výkaznictví konkrétních zemí](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality), je funkce EM nastavena tak, aby měla kombinaci mnoha stavů zpráv, stavů položek zpráv, akcí, dalších polí a spustitelných tříd. Pro tyto scénáře jsou k dispozici balíčky datových entit pro import. Pokud použijete tyto balíčky datových entit, importujte do právnické osoby pomocí nástroje pro správu dat. Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Pokud neimportujete balíček datových entit, můžete ručně nastavit funkčnost elektronických zpráv. V takovém případě je třeba nastavit následující prvky:

- [Číselné řady](#sequences)
- [Typy položek zpráv](#types)
- [Stavy položky zprávy](#item)
- [Stavy zpráv](#statuses)
- [Dodatečná pole](#additional)
- [Nastavení spustitelné třídy](#executable)
- [Akce naplnění záznamů](#populate)
- [Webové aplikace](#applications)
- [Nastavení webové služby](#settings)
- [Akce zpracování zprávy](#actions)
- [Zpracování elektronické zprávy](#processing)

Další části poskytují více informací o každém z těchto prvků.

## <a name="number-sequences"></a><a id="sequences"></a>Číselné řady

Nastavte číselné řady pro zprávy a položky zprávy. Číselné řady se používají k automatickému číslování zpráv a položek zpráv. Čísla, která se použijí jako jedinečné identifikátory zpráv a položek zpráv v systému. Můžete nastavit číselné řady pro elektronické zprávy na stránce **Hlavní kniha** \> **Nastavení hlavní knihy** \> **Parametry hlavní knihy**.

## <a name="message-item-types"></a><a id="types"></a>Typy položek zpráv

Typy položek zpráv určují typy záznamů, které budou použity v elektronických zprávách. Můžete nastavit typy položek zpráv na stránce **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Typy položek zpráv**.

## <a name="message-item-statuses"></a><a id="item"></a>Stavy položky zprávy

Stavy položek zpráv určují stavy, které se budou vztahovat na položky zpráv při zpracování, které nastavujete. Můžete nastavit stavy položek zpráv na stránce **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy položek zpráv**.

Parametr **Povolit odstranění** stavu položky zprávy určuje, zda vám bude povoleno odstranění položek zprávy v tomto stavu prostřednictvím stránky **Elektronické zprávy** nebo stránky **Položky elektronických zpráv**.

## <a name="message-statuses"></a><a id="statuses"></a>Stavy zpráv

Nastavte stavy zpráv, které by měly být k dispozici při zpracování zprávy. Můžete nastavit stavy položek zpráv na stránce **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy zpráv**.

Následující tabulka popisuje pole na stránce **Stavy zprávy**.

| Název pole          | Popis |
|---------------------|-------------|
| Stav zprávy      | Zadejte jedinečný název stavu zprávy. Stavy zprávy slouží k určení stavu elektronická zprávy v každém okamžiku. Název, který zadáte, se zobrazí na stránce **elektronické zprávy** stránky a v protokolu, který s elektronickými zprávami souvisí. |
| Popis         | Zadejte popis vybraného stavu zprávy. |
| Typ odezvy       | Vyberte typ odpovědi stavu zprávy. Některé akce zpracování mohou mít více než jeden typ odezvy. Například akce typu **Webová služba** mohou vyústit buď v typ odpovědi **Úspěšně provedeno** nebo **Technická chyba** v závislosti na výsledku spuštění. V takovém případě definujte stavy zpráv pro oba typy odezvy. Další informace o typech akcí a s nimi souvisejících typech odezvy získáte v části [Typy akcí zpracování zpráv](#action-types) dále v tomto tématu. |
| Stav položky zprávy | Někdy musí mít stav elektronické zprávy ovlivňovat stav souvisejících položek zprávy. Vyberte stav zprávy položky v tomto poli, abyste ji mohli přidružit ke stavu zprávy. |
| Odstranit vše        | Toto políčko zaškrtněte, pokud uživatelé budou moci odstranit elektronické zprávy s tímto stavem na stránce **elektronické zprávy**. |

## <a name="additional-fields"></a><a id="additional"></a>Dodatečná pole

Funkce EM umožňuje shromažďovat záznamy z transakčních tabulek v Microsoft Dynamics 365 Finance jako položky zprávy. Tímto způsobem lze připravit záznamy pro vykazování a poté je vykázat. Transakční tabulky však někdy nemají dostat informací pro vyplnění záznamů způsobem, který splňuje požadavky na výkazy. Můžete vyplnit všechny informace, které musí být vykázány pro záznam nastavením dalších polí. Další pole lze přidružit ke zprávám i položkám zpráv. Můžete nastavit další pole na stránce **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Další pole**.

Následující tabulka popisuje obecná pole na stránce **Další pole**.

| Pole       | popis |
|-------------|-------------|
| Název pole  | Zadejte název dalšího pole pro elektrické zprávy nebo položky zprávy, které se vztahují k procesu. Tento název se zobrazí v uživatelském rozhraní (UI) při práci s procesem. Název lze také použít v konfiguracích elektronického výkaznictví (ER), které se vztahují k procesu. |
| popis | Zadejte popis dalšího pole. |
| Úpravy uživatele   | Nastavte tuto možnost **Ano**, pokud by uživatelé měli mít možnost změnit hodnotu dalšího pole z UI. |
| Počitadlo     | Nastavte tuto možnost na **Ano**, pokud další pole mělo obsahovat číselnou řadu v elektronické zprávě. Hodnota dalšího pole se vyplní automaticky při spuštění akce typu **Export elektronického výkaznictví**. |
| Skryté      | Tuto možnost nastavte na **Ano**, pokud by mělo být další pole skryté v uživatelském rozhraní na stránce **Elektronické zprávy** nebo **Položky elektronické zprávy**. |

Na rychlé kartě **Hodnoty** můžete předdefinovat hodnoty, které může mít další pole. Tyto hodnoty jsou pak k dispozici uživatelům k výběru. Proto se nemusí během zpracování ručně vyplňovat. Následující tabulka obsahuje popis polí.

| Pole                | popis |
|----------------------|-------------|
| Hodnota pole          | Zadejte hodnotu pole pro použití ve vztahu ke zprávě nebo položce zprávy při vykazování. |
| Popis          | Zadejte popis hodnoty pole. |
| Typ účtu         | Některé hodnoty polí mohou být omezeny na určité typy účtů. Vyberte jednu z následujících hodnot: **Všechny**, **Odběratel**, nebo **Dodavatel**. |
| Kód účtu         | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu**, můžete dále omezit použití hodnot pole na konkrétní skupinu nebo tabulku. |
| Číslo účtu/skupiny | Pokud jste vybrali možnosti **Odběratel** nebo **Dodavatel** v poli **Typ účtu** a zadali jste skupinu nebo tabulku do pole **Kód účtu**, můžete v tomto poli zadat určitou skupinu nebo protistranu. |
| Účinné:            | Zadejte datum, kdy má být hodnota zahájena ke zvažovaní. |
| Vypršení platnosti           | Zadejte datum, kdy má být hodnota ukončena pro zvažování. |

Ve výchozím nastavení kombinací kritérií, která jsou definována podle polí **číslo účtu/skupiny**, **kódu účtu**, **data platnosti**, a **vypršení platnosti** neovlivňují výběr hodnot pro Další pole. Avšak používání těchto kombinací lze použít ve spustitelné třídě k implementaci konkrétní logiky, která vypočítá hodnotu pro další pole.

## <a name="executable-class-settings"></a><a id="executable"></a>Nastavení spustitelné třídy

Spustitelná třída je metoda X ++ nebo třída, kterou může zpracování elektronické zprávy volat ve vztahu k akci, pokud je některé hodnocení vyžadováno pro proces.

Můžete ručně nastavit spustitelnou třídu, která musí být volána během zpracování, přechodem na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Nastavení spustitelné třídy**. Na stránce **Nastavení spustitelné třídy** vytvořte řádek a nastavte následující pole.

| Pole                 | popis |
|-----------------------|-------------|
| Spustitelná třída      | Zadejte název, který bude použit při nastavení akce zpracování zpráv, pro kterou je tato třída volána. |
| Popis           | Zadejte popis spustitelné třídy. |
| Název spustitelné třídy | Výběr spustitelnou třídu X ++. |
| Úroveň spuštění       | Toto pole je nastaveno automaticky, protože by měla být předdefinovaná hodnota pro vybranou spustitelnou třídu. Toto pole omezuje úroveň, na níž probíhá související hodnocení. |
| Popis třídy     | Toto pole je nastaveno automaticky, protože by měla být předdefinovaná hodnota pro vybranou spustitelnou třídu. |
| Typ akce           | Toto pole je k dispozici, když je funkce **\[EM\] typ akce spustitelné třídy** zapnutá v pracovním prostoru **Správa funkcí**. Toto pole slouží k určení typu akce pro spustitelnou třídu. Toto pole poskytuje přesnější kontrolu nad dalšími akcemi, které jsou k dispozici pro elektronickou zprávu na stránce **Elektronické zprávy**. |

Některé spustitelné třídy mohou mít povinné parametry, které musí být definovány před prvním spuštěním spustitelné třídy. Chcete-li definovat tyto parametry, v podokně akcí vyberte **Parametry**. V dialogovém okně, které se zobrazí, nastavte pole a pak vyberte **OK**. Je důležité, abyste vybrali **OK**. V opačném případě parametry nebudou uloženy v databázi a třída spustitelného souboru nebude správně volána.

## <a name="populate-records-actions"></a><a id="populate"></a>Akce naplnění záznamů

Použijete akce naplnění záznamů nastavení akcí, které přidávají záznamy do tabulky položek zpráv tak, aby mohly být přidány do elektronické zprávy. Například pokud vaše elektronická zpráva musí vykazovat faktury odběratele, je nutné nastavit akci Naplnit záznamy, která je propojena s polem **Zdroj dat** v tabulce Deník faktur odběratele.

Můžete nastavit akce naplnění záznamů přechodem **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce naplnění záznamů**. Vytvořte nový záznam pro každou akci, která by měla přidat záznamy do tabulky, a nastavte následující pole.

| Pole       | Popis |
|-------------|-------------|
| Název        | Zadejte název akce, která naplní záznamy ve vašem procesu. |
| Popis | Zadejte popi akce zadání záznamů. |

Na záložce s náhledem **Nastavení datových zdrojů** přidejte řádek pro každý datový zdroj, který se používá pro proces, a nastavte následující pole.

| Pole                  | Popis |
|------------------------|-------------|
| Jméno                   | Zadejte název pro datový zdroj. |
| Typ položky zprávy      | Vyberte typ položky zprávy, která se použije při vytváření záznamů pro datový zdroj. |
| Typ účtu           | Vyberte typ účtu, který se přiřadí k záznamům z datového zdroje. |
| Název hlavní tabulky      | Vyberte tabulku, která bude zdrojem dat. |
| Pole čísla dokumentu  | Zvolte pole, ze kterého bude číslo dokumentu převzato ve vybrané hlavní tabulce. Hodnota tohoto pole se použije jako hodnota parametru **Číslo dokumentu** pole pro položku zprávy. |
| Pole data dokumentu    | Zvolte pole, ze kterého bude datum dokumentu převzato ve vybrané hlavní tabulce. Hodnota tohoto pole se použije jako hodnota parametru **Datum položky zprávy** pro položku zprávy. |
| Pole účtu dokumentu | Zvolte pole, ze kterého bude účet dokumentu převzato ve vybrané hlavní tabulce. Hodnota tohoto pole se použije jako hodnota parametru **Číslo účtu** pole pro položku zprávy. |
| Společnost                | Toto pole je dostupné, když je funkce **Dotazy mezi více společnostmi pro akce naplnění záznamů** zapnutá v pracovním prostoru **Správa funkcí**. Tuto funkci použijte k nastavení zdrojů dat mezi společnostmi pro akce naplnění záznamů. Data lze načíst od několika společností. |
| Dotaz uživatele             | <p>Pokud nastavíte dotaz výběrem **Upravit dotaz** nad mřížkou a určíte kritéria, která musí být použita na vybranou hlavní tabulku, ze které jsou vyplňována data, je toto políčko automaticky zaškrtnuto. V opačném případě budou všechny záznamy vyplněny z vybraného zdroje hlavní tabulky.</p><p>Když je funkce **Dotazy mezi více společnostmi pro akce naplnění záznamů** zapnutá v pracovním prostoru **Správa funkcí** a záznamy musí být shromážděny od několika společností, přidejte řádek pro každou další právnickou osobu, která musí být zahrnuta do vykazování. U každého nového řádku vyberte **Upravit dotaz** a zadejte související kritérium specifické pro právnickou osobu, která je uvedena v poli **Společnost** na řádku. Po dokončení, mřížka **Nastavení zdrojů dat** bude obsahovat řádky pro všechny právnické osoby, které musí být zahrnuty do výkaznictví.</p> |

## <a name="web-applications"></a><a id="applications"></a>Webové aplikace

Nastavení webové aplikace použijte tak, aby podporovala otevřené autorizace (OAuth) 2.0. OAuth je otevřený standard, který umožňuje uživatelům udělit zabezpečeného delegovaného přístupu k aplikaci jejich jménem bez sdílení pověření pro přístup. Z této stránky můžete také projít procesem autorizace získáním autorizačního kódu a přístupového tokenu. Můžete provést nastavení webové aplikace přechodem na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Webové aplikace**.

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
| Token přístupu vyprší za  | Zbývající čas před vypršením platnosti tokenu. Toto pole je automaticky aktualizováno. | 
| Souhlasím                       | Určete vlastnost **Accept** webové žádosti. Zadejte například **application/vnd.hmrc.1.0+json**. |
| Typ obsahu                 | Určete typ obsahu. Například zadejte **application/json**. |

Kromě toho jsou v podokně Akce na stránce **Webové aplikace** k dispozici následující tlačítka na podporu procesu ověřování:

- **Získání autorizačního kódu** - pro inicializaci autorizace webové aplikace. Tato funkce používá formát ER, který je uveden v poli **Mapování formátu autorizace** pro vygenerování žádosti o autorizaci.
- **Získat autorizační token** – pro inicializací získání přístupového tokenu.
- **Aktualizovat přístupový token** – pro obnovení přístupového tokenu. Tato funkce používá formát ER, který je uveden v poli **Importovat mapování modelu tokenu** pro import informací o přijatém přístupovém tokenu.

Pokud je přístupový token k webové aplikaci uložený v databázi systému v zašifrovaném formátu, může být použit pro požadavky na webovou službu. Pro účely zabezpečení musí být přístup k tokenu omezen pouze na ty role zabezpečení, kterým je umožněno tyto požadavky řešit. Pokud se někdo mimo skupinu zabezpečení pokusí řešit žádost, obdrží chybu oznamující, že nemají povoleno komunikovat prostřednictvím vybrané webové aplikace. Chcete-li nastavit role zabezpečení, které mají přístup k přístupovému tokenu, použijte pevnou záložku **Role zabezpečení** na stránce **Webové aplikace**. Pokud nejsou role zabezpečení definovány pro webovou aplikaci, může pouze správce systému spolupracovat pouze prostřednictvím této webové aplikace.

Pro každou akci s vybranou webovou aplikací rychlá karta **Protokol akcí** ukládá informace o uživateli a datu a čase.

Některé webové služby mohou vyžadovat zahrnutí různých hlaviček do požadavků. Správce systému může na serveru nastavit další hlavičky a jejich hodnoty na rychlé kartě **Doplňkové hlavičky** a poté je použít během generování požadavku.

## <a name="web-service-settings"></a><a id="settings"></a>Nastavení webové služby

Pomocí nastavení webových služeb nastavíte přímý přenos dat do webové služby. Můžete provést nastavení webové služby přechodem na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Nastavení webové služby**.

Následující tabulka popisuje pole na stránce **Nastavení webové služby**.

| Pole                          | popis |
|--------------------------------|-------------|
| Webová služba                    | Zadejte název webové služby. |
| popis                    | Zadejte popis webové služby. |
| Internetová adresa               | <p>Zadejte internetovou adresu webové služby. Je-li pro webovou službu zadána webová aplikace a internetová adresa by měla být stejná jako adresa definovaná pro vybranou webovou aplikaci, klikněte na tlačítko **Zkopírovat základní URL adresu**. Do tohoto pole se poté zkopíruje základní adresa URL webové aplikace.</p><p>**Upozornění:** Služby třetích stran nebo jiné služby, které zde nakonfigurujete, nevyžadují certifikaci a nemusí splňovat standardy společnosti Microsoft týkající se ochrany osobních údajů. Měli byste ověřit dokumentaci týkající se ochrany osobních údajů každé služby a kontaktovat poskytovatele každé služby, abyste se dozvěděli více informací o úrovni shody, kterou služba poskytuje. Jste sami zodpovědní za to, že se ujistíte, zda tyto služby splňují vaše bezpečnostní, ochranné a právní standardy. Odpovědnost za používání těchto služeb je pouze na vás. Společnost Microsoft vám nedává žádné výslovné záruky, garance ani podmínky. Důrazně doporučujeme používat pouze služby, které poskytují zabezpečené a autorizované připojení, jako je HTTPS.</p> |
| Certifikát                    | Vyberte certifikát Azure Key Vault, který byl již předtím nastaven. |
| Webová aplikace                | Vyberte webovou aplikaci, která byla již předtím nastavena. |
| Typ odezvy – XML        | Nastavte tuto možnost na **Ano**, pokud je typ odpovědi XML. |
| Metoda požadavku                 | Zadejte způsob požadavku. HTTP definuje sadu metod požadavků, které označují akci, která by měla být provedena pro daný zdroj. Metodou požadavku může být **GET**, **POST**, nebo jiná metoda HTTP. |
| Záhlaví požadavku                | Určete záhlaví požadavku. Hlavička požadavku je hlavička HTTP, kterou lze použít v požadavku HTTP. Nesouvisí s obsahem zprávy. |
| Souhlasím                         | Určete vlastnost přijmout webové žádosti. |
| Přijmout kódování                | Zadejte hodnotu accept-encoding. Záhlaví HTTP požadavku Accept-Encoding oznamuje kódování obsahu, které může klient pochopit. Toto kódování obsahu je obvykle algoritmus komprese. |
| Typ obsahu                   | Určete typ obsahu. Záhlaví HTTP entity Content-Type označuje typ média zdroje. |
| Úspěšný kód odpovědi       | Určete kód stavu HTTP označující, že požadavek byl úspěšný. |
| Mapování formátu záhlaví požadavku | Vyberte formát ER, který bude použit ke generování záhlaví webového požadavku. |

## <a name="message-processing-actions"></a><a id="actions"></a>Akce zpracování zprávy

Pomocí akcí zpracování zpráv vytváříte akce pro své procesy a nastavujete jejich parametry. Můžete nastavit akce zpracování zpráv přechodem **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce zpracování zprávy**.

Následující tabulky popisují pole na stránce **Akce zpracování zpráv**.

### <a name="general-fasttab"></a>Záložka s náhledem Obecné

| Pole                                     | popis |
|-------------------------------------------|-------------|
| Typ akce                               | Vyberte typ akce. Informace o dostupných možnostech naleznete v části [Typy akcí zpracování zpráv](#action-types) dále v tomto tématu. |
| Mapování formátu                            | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví**, **Import elektronického výkaznictví** a **Zpráva exportu elektronického výkaznictví**. |
| Mapování formátu pro cestu URL               | Vyberte formát elektronického výkaznictví, který by měl být volán pro akci. Tento formát slouží k vytvoření cesty adresy URL, která bude přidána k základní internetové adrese zadané pro vybraný webový server. Toto pole je k dispozici pouze pro akce typu **Webová služba**. |
| Typ položky zprávy                         | Vyberte typ záznamů, pro které by měla být akce vyhodnocována. Toto pole je k dispozici pro akce typu **Úroveň spuštění položky zprávy**, **Import elektronického výkaznictví** a **Export elektronického výkaznictví**, **Webová služba** a další typy. Necháte-li toto pole prázdné, vyhodnotí se všechny typy položek zpráv, které jsou definovány pro zpracování zpráv. |
| Spustitelná třída                          | Vyberte existující nastavení spustitelné třídy. Toto pole je k dispozici pouze pro akce typu **Úroveň spuštění zprávy** a **Úroveň spuštění položky zprávy**. |
| Akce naplnění záznamů                   | Vyberte existující akci naplnění záznamů. Toto pole je k dispozici pouze pro akce typu **Naplnit záznamy**. |
| Webová služba                               | Vyberte existující webovou službu. Toto pole je k dispozici pouze pro akce typu **Webová služba**. |
| Název souboru                                 | Zadejte název souboru, který bude výsledkem akce. Tento soubor může být odezva na webový server nebo sestava, která je generována. Toto pole je k dispozici pouze pro akce typu **Webová služba** a **Zpráva exportu elektronického výkaznictví**. |
| Připojit soubory do zdrojových dokumentů          | Zaškrtnutím tohoto políčka připojíte vygenerované soubory k záznamům v odkazované hlavní tabulce pro položky EM. Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví** a **Webová služba**. |
| Připojit soubory z výstupního archivu k položkám | Zaškrtnutím tohoto políčka extrahujete samostatné soubory XML z výstupního archivního souboru a připojíte je k odpovídajícím položkám elektronických zpráv. Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví**. |
| Počet položek zpráv podle exportu        | Zadejte limit počtu položek zprávy, které musí být zahrnuty v jednom souboru (zprávě). Toto pole je k dispozici pouze pro akce typu **Export elektronického výkaznictví**. |
| Použít zdroj ER                             | Zaškrtnutím tohoto políčka použijete pro import parametry zdroje ER. Jinak se použije příloha z elektronické zprávy. Toto pole je k dispozici pouze pro akce typu **Import elektronického výkaznictví**. |
| Zobrazit dialogové okno                               | Nastavte tuto možnost na **Ano**, pokud musí být uživateli před vytvořením sestavy zobrazeno dialogové okno. Toto pole je k dispozici pouze pro akce typu **Zpráva exportu elektronického výkaznictví**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Typy akcí zpracování zprávy

Následující možnosti jsou dostupné v poli **Typ akce**.

- **Vytvořit zprávu** – Použití tohoto typu akce umožní uživatelům ručně vytvořit zprávy na stránce **Elektronická zpráva**. Počáteční stav nemůže být pro akci tohoto typu nastaven.
- **Vyplnit záznamy** – Tento typ akce již musí být nastaven. Přidružte ho k akci vyplnění záznamů, aby mohla být zahrnuta do zpracování. Předpokládá se, že tento typ akce se používá pro první akci ve zpracování zprávy (pokud nebyla předem vytvořena žádná elektronická zpráva) nebo jako akce přidání položek zprávy do dříve vytvořené zprávy (akcí typu **Vytvořit zprávu**). Proto lze pro akci tohoto typu nastavit stav výsledků pouze položek zpráv. Lze nastavit počáteční stav pouze pro zprávy.
- **Úroveň spuštění zprávy** – Tento typ akce slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni zprávy.
- **Úroveň spuštění položky zprávy** – Tento typ akce slouží k nastavení spustitelné třídy, která by měla být vyhodnocována na úrovni položky zprávy.
- **Export elektronického výkaznictví** – Použijte tento typ pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpráva exportu elektronického výkaznictví** – Použijte tento typ akce pro akce, které mají generovat sestavu, která je založena na exportu konfigurace elektronického výkaznictví na úrovni položky zprávy (například když zpráva nemá žádné položky zprávy).
- **Import elektronického výkaznictví** – Použijte tento typ akce pro akce, které mají generovat sestavu, která je založena na importu konfigurace elektronického výkaznictví na úrovni položky zprávy.
- **Zpracování uživatele na úrovni zprávy** – Tento typ akce použijte pro akce, které předpokládají některé ruční akce provedené uživatelem. Uživatel může například aktualizovat stav zpráv.
- **Zpracování uživatele** – Tento typ akce použijte pro akce, které předpokládají některé ruční akce provedené uživatelem. Uživatel může například aktualizovat stav položek zpráv.
- **Webová služba** – Tento typ akce použijte pro akce, které mají přenášet generovanou sestavu do webové služby. Tento typ akce není použit pro italské vykazování komunikace o prodejních a nákupních fakturách. Pro tento typ akce obsahuje stránka **Akce zpracování zprávy** pevnou záložku **Různé detaily**, na níž lze zadat text potvrzení. Tento potvrzovací text se uživatelům zobrazí před vyřešením žádostí o vybranou webovou službu.
- **Požádat o ověření** – Použijte tento typ akce pro vyžádání ověření ze serveru.

### <a name="initial-statuses-fasttab"></a>Záložka s náhledem Počáteční stavy

> [!NOTE]
> Záložka s náhledem **Počáteční stavy** není k dispozici pro akce, které mají počáteční typ akce **Vytvořit zprávu**.

| Pole               | Popis |
|---------------------|-------------|
| Stav položky zprávy | Vyberte stav položky zprávy, pro který by měla být vyhodnocena vybraná akce zpracování zpráv. |
| popis         | Popis vybraného stavu položky zprávy. |

### <a name="result-statuses-fasttab"></a>Záložka s náhledem Výsledné stavy

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

## <a name="electronic-message-processing"></a><a id="processing"></a>Zpracování elektronické zprávy

Zpracování elektronických zpráv je základním konceptem funkčnosti elektronických zpráv. Agreguje akce, které by měly být vyhodnocovány pro elektronickou zprávu. Akce lze propojit prostřednictvím počátečního stavu a výsledného stavu. Popřípadě lze spustit akce **Zpracování uživatele** samostatně. Chcete-li nastavit zpracování elektronických zpráv přejděte na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Zpracování elektronické zprávy**.

Záložka s náhledem **Akce** umožňuje přidat předdefinované akce ke zpracování. Můžete určit, zda má být akce spuštěna odděleně, nebo zda může být zahájena zpracováním. Pro určení, zda může být inicializována akce ve zpracování zahájena pouze uživatelem, nastavte hodnotu v poli **spustit samostatně** na **Ano** pro danou akci. Pokud chcete, aby byla akce spuštěna zpracováním, když jsou zprávy nebo položky zpráv ve stavu definovaném jako počáteční stav této akce, nastavte v poli **Spustit samostatně** hodnotu **Ne**. Akce typu **Akce uživatele** musí být vždy spuštěna samostatně.

Několik operací musí být agregováno, a to i v případě, že je první akci nastavena tak, aby byla spouštěna samostatně. Například uživatel musí inicializovat generování sestav. Jakmile je vygenerovaná zpráva, musí však být okamžitě odeslána webové službě a odpověď z webové služby musí být v systému zohledněna. V takovém případě můžete vytvořit neoddělitelnou sekvenci pro akce, které musejí být spojeny. Na pevné záložce **Akce** vyberte **Neoddělitelné skupiny** nad mřížkou a vyberte skupinu. Potom pro všechny akce, které musí běžet zároveň v jedné sekvenci, vyberte pořadí v poli **Neoddělitelné pořadí**. V tomto případě může být pole **Spustit samostatně** nastaveno na **Ano** pro první akci v řadě, ale na **Ne** pro všechny akce.

Akce typů **Export elektronického výkaznictví** a **Zpráva exportu elektronického výkaznictví** spouštějí formát ER, který má vstupní parametry. Pokud vaše zpracování elektronických zpráv zahrnuje akce některého z těchto typů, musíte před generováním zprávy určit hodnoty vstupních parametrů. Tímto způsobem může systém použít dávkový režim ke generování zprávy. Můžete vybrat **Parametry** nad mřížkou k nastavení parametrů pro vybraný typ akce (**Export elektronických zpráv** nebo **Zpráva exportu elektronických zpráv**). Zaškrtněte políčko **Použít parametry** pro akci, která musí být spuštěna se zadanými parametry v dávkovém režimu.

Použijte záložku s náhledem **Další pole položky zprávy** k přidání dalších předdefinovaných pole, která souvisí s položkami zpráv. Musíte přidat další pole pro každý typ položky zprávy, k níž se tato pole vztahují. Můžete určit výchozí hodnotu, která bude přidělena dalšímu poli během zpracování.

Záložka s náhledem **Další pole položky zprávy** umožňuje přidat předdefinovaná další pole, která souvisí se zprávami. Můžete určit výchozí hodnotu, která bude přidělena dalšímu poli během zpracování.

Záložka s náhledem **Role zabezpečení** umožňuje nastavit role zabezpečení, které jsou předem definovány v systému pro konkrétní zpracování. Uživatelé, kteří mají určitou roli, uvidí pouze zpracování, které je definováno pro danou roli.

Záložka s náhledem **Dávka** umožňuje nastavit zpracování tak, aby fungovalo v režimu dávky. Doporučujeme nastavit dávkový režim pro vaše zpracování přímo na stránce **Elektronické zprávy** nebo **Položky elektronické zprávy**, když vyberete **Spustit zpracování** v podokně Akce k zahájení zpracování.
