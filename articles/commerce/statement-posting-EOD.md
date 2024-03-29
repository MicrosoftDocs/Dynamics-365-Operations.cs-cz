---
title: Vylepšení funkcionality zaúčtování výkazů
description: Tento článek popisuje vylepšení, která byla provedena u funkce zaúčtování výkazu.
author: analpert
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 33b4f17cd46338b62bed96f0a285e7b9634cc87a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067812"
---
# <a name="improvements-to-statement-posting-functionality"></a>Vylepšení funkcionality zaúčtování výkazů

[!include [banner](includes/banner.md)]

Tento článek popisuje první sadu vylepšení, která byla provedena u funkce zaúčtování výkazu. Tato zlepšení jsou k dispozici v aplikaci Microsoft Dynamics 365 Finance 7.3.2.

## <a name="activation"></a>Aktivace

Ve výchozím nastavení při nasazení finanční a provozní aplikace 7.3.2. je aplikace nastavená na používání zastaralé funkce pro zaúčtování výkazů. Pro povolení funkce vylepšeného zaúčtování výkazů zaúčtování musíte zapnout konfigurační klíč.

- Přejděte na **Správa systému** \> **Nastavení** \> **Konfigurace licence** a poté v uzlu **Retail a Commerce** zrušte zaškrtnutí políčka **Výkazy (starší verze)** a zaškrtněte políčko **Výkazy**.

Když je zapnutý konfigurační klíč pro nové **Výkazy**, bude k dispozici nová položka nabídky, s názvem **Výkazy**. Tato položka nabídky umožňuje ručně vytvořit, vypočítat a zaúčtovat výkazy. Všechny výkazy, které způsobují chyby při zaúčtování dávkového zpracování budou také k dispozici prostřednictvím této položky. (Když je zapnutý konfigurační klíč pro nové **Výkazy (zastaralé)**, bude název položky **Otevřené výkazy**.)

Aplikace Commerce zahrnuje následující ověření, která souvisí s těmito konfiguračními klíči:

- Oba konfigurační klíče nelze spustit současně.
- Stejný konfigurační klíč musí být použit pro všechny operace, které se provádí v daném výkazu během jeho cyklu životnosti (vytvořit, vypočítat, vymazat, zaúčtovat a tak dále). Nelze například vytvořit a vypočítat výkaz, když je zapnutý konfigurační klíč **Výkaz (starší verze)** konfigurační a vy se pokusíte o zaúčtování stejného výkazu, když je zapnutý konfigurační klíč **Výkaz**.

> [!NOTE]
> Doporučujeme používat **Výkazy** konfigurační klíč pro zlepšení výkaz zaúčtování, pokud nemáte závažné důvodů pro použití **Výkazy (starší verze)** konfigurační klíč místo. Společnost Microsoft bude dále investovat do nových a vylepšených funkcí zaúčtování výkazů a je důležité, abyste na ně co nejdříve přešli a plně je využívali. Zastaralá funkce zaúčtování výkazů bude od verze 8.0 vyřazena.

## <a name="setup"></a>Nastavení

Jako součást vylepšení funkce zaúčtování výkazu byly zavedeny tři nové parametry na pevné záložce **výkaz** na kartě **zaúčtování** stránky **Parametry Commerce**:

- **Zakázat výkaz vymazání** – tuto možnost lze použít pouze pro funkcí účtování staršího výkazu. Doporučujeme tuto možnost nastavit na **Ne**, abyste uživatelům zabránili mazat výkazy ve stavu nedokončeného zaúčtování. Pokud jsou výkazy, které jsou ve stavu nedokončeného zaúčtování, prázdné, data budou poškozená. Tuto možnost nastavte na **Ano** pouze ve speciálních případech.
- **Rezervovat zásoby při výpočtu** – doporučujeme používat dávkovou úlohu **Zaúčtovat zásoby** pro rezervaci zásob a a nastavit tuto možnost na **ne**. Pokud je tato možnost nastavena na **Ne**, vylepšená funkce zaúčtování se nepokusí vytvořit rezervaci položek zásob v době výpočtu (Pokud položky nebyly vytvořeny prostřednictvím dávkové úlohy **zaúčtování zásob**). Funkce místo toho vytvoří položky rezervace zásob pouze v době zaúčtování. Tato implementace byla volbou návrhu a byla založena na skutečnosti, že je obvykle malá časová prodleva mezi procesem výpočtu a procesem účtování. Pokud však chcete rezervovat zásoby v době výpočtu, můžete tuto možnost nastavit na **Ano**.

    Zastaralá funkce zaúčtování výkazu vždy rezervuje zásoby při výpočtu výkazu (Pokud již nebyla provedena rezervace prostřednictvím dávkové úlohy **zaúčtování zásob**) bez ohledu na nastavení této možnosti.

- **Je vyžadována deaktivace inventur** – při nastavení této možnosti na **Ano** proces zaúčtování výkazů pokračuje i v případě, že rozdíl mezi vypočítanou částkou a částkou transakce na výkazu je mimo prahovou hodnotu, která je definovaná v pevné záložce **Výkaz** pro obchody.

> [!NOTE]
> Od vydání Commerce verze 10.0.14 platí, že když je povolena funkce **Výkazy maloobchodu – Postupné**, dávková úloha **Zaúčtovat zásoby** již není použitelná a nelze ji spustit.

## <a name="processing"></a>Zpracování

Příkazy je možné vypočítávat a zaúčtovat v dávce pomocí položek nabídky **Počítat výkazy v dávce** a **dávkové Zaúčtování výkazů**. Výkazy lze alternativně ručně vypočítávat a zaúčtovat pomocí nabídky **Výkazy**, která poskytuje vylepšené funkce zaúčtování výkazu.

Proces a postup při výpočtu a zaúčtování výkazů v rámci dávky, jsou stejné jako u funkce zaúčtování výkazu ze starší verze. Významná vylepšení však byly provedeny v základním back-endovém zpracování výkazů. Tato zlepšení zajišťují, že je proces více pružný a poskytují lepší přehled o stavech a informace o chybách. Proto mohou uživatelé vyřešit hlavní příčinu chyb a poté pokračovat v procesu zaúčtování, aniž by to způsobilo poškození dat, a bez nutnosti oprav dat.

Následující části popisují některá zásadní vylepšení pro výkazy a zaúčtované výkazy, která se zobrazí v uživatelském rozhraní.

### <a name="status-details"></a>Podrobnosti o stavu

Byl zaveden nový model stavu v rutině zaúčtování výkazů v rámci procesů výpočtu a zaúčtování.

Následující tabulka popisuje různé stavy a jejich pořadí během procesu výpočtu.

| Pořadí stavu | Kraj      | popis |
|-------------|------------|-------------|
| 1           | Zahájeno    | Výkaz byl vytvořen a je připraven k výpočtu. |
| 2           | Označeno     | Transakce, které jsou v rozsahu výkazu, jsou označeny na základě parametrů výkazu a jsou označeny ID výkazu. |
| 3           | Vypočteno | Řádky výkazu se vypočtou a zobrazí. |

Následující tabulka popisuje různé stavy a jejich pořadí během procesu zaúčtování.

| Pořadí stavu | Kraj                   | popis |
|-------------|-------------------------|-------------|
| 1           | Zkontrolováno                 | Provádí se vícenásobné ověřování související s parametry (například dispoziční náklady) a s výkazy a řádky výkazu (například rozdíl mezi spočtenou částkou a částkou transakce). |
| 2           | Agregované              | Prodejní transakce jmenovaných a nejmenovaných odběratelů jsou seskupeny podle konfigurace. Každá agregovaná transakce je nakonec převedena na prodejní objednávku. |
| 3           | Vytvořená objednávka odběratele  | Na základě souhrnné transakce jsou v systému vytvořeny prodejní objednávky. |
| 4           | Objednávka odběratele fakturovaná | Prodejní objednávky jsou fakturované. |
| 5           | Zaúčtované slevy        | Deníky pravidelné slevy se zaúčtovávají na základě konfigurace. |
| 6           | Zaúčtovaný příjem/výdaj   | Transakce příjmů/výdajů se zaúčtovávají jako doklady. |
| 7           | Doklady propojeny         | Deníky plateb se vytvářejí a jsou propojeny s odpovídající fakturou. |
| 8           | Zaúčtované platby         | Deníky plateb jsou zaúčtované. |
| 9           | Zaúčtované dárkové poukazy       | Transakce dárkových karet se zaúčtovávají jako doklady. |
| 10          | Zveřejněno                  | Výkaz je označen jako zaúčtovaný. |

Každý stav v předchozích tabulkách je nezávislý a mezi stavy je vytvořena hierarchická závislost. Tato závislost teče shora dolů. Jestliže systém zaznamená nějaké chyby při zpracování stavu, stav výkazu se vrátí na předchozí stav. Všechny následné opakované pokusy procesu se obnoví ze stavu, který se nezdařil, a pokračují v chodu. Tento přístup má následujících výhody:

- Uživatel má kompletní přehled o stavu, kdy došlo k chybě.
- Je zabráněno poškození dat. Například ve starší funkci zaúčtování výkazu byly instance, kdy byly fakturovány některé prodejní objednávky, ale ostatní zůstaly otevřené. Vyskytly se rovněž instance, kdy některé deníky plateb neměly odpovídající fakturu k vyrovnání, protože při zaúčtování faktury došlo k chybě.
- Uživatelé mohou zobrazit aktuální stav výkazu pomocí tlačítka **podrobnosti o stavu** ve skupině **podrobnosti o spuštění** ve výkazu. Stránka podrobností o stavu obsahuje tři části:

    - První část zobrazuje aktuální stav výkazu, spolu s kódem chyby a podrobnou chybovou zprávou, pokud došlo k chybě.
    - Druhý oddíl se zobrazí různé stavy procesu výpočtu. Vizuální návody určují stavy, které byly úspěšně spuštěn, stavy, které se nepodařilo spustit z důvodu chyb a stavy, které dosud nebyly spuštěny.
    - Třetí oddíl zobrazuje různé stavy procesu zaúčtování. Vizuální návody určují stavy, které byly úspěšně spuštěn, stavy, které se nepodařilo spustit z důvodu chyb a stavy, které dosud nebyly spuštěny.

Kromě toho záhlaví oddíly druhého a třetího oddílu zobrazuje celkový stav příslušného procesu.

### <a name="event-logs"></a>Protokoly událostí

Výkaz prochází různými operacemi (například vytvořit, vypočítat, vymazat a zaúčtovat) a více instancí stejné operace může být voláno během životního cyklu výkazu. Například po vytvoření a vypočítání výkazu ho uživatel může vymazat a vypočítávat znovu. Tlačítko **Protokoly událostí** ve skupině výkazů **Podrobnosti o spuštění** obsahuje úplný kontrolní záznam různých operací, které byly volány ve výkazu, společně s informacemi o tom, kdy byly tyto operace volány.

### <a name="aggregated-transactions"></a>Agregované transakce

Během procesu zaúčtování jsou transakce cash-and-carry agregovány podle zákazníka a produktu. Proto se sníží počet prodejních objednávek a vytvořených řádků. Tyto souhrnné transakce jsou v systému uloženy a slouží k vytváření prodejních objednávek. Každá souhrnná transakce agregační vytvoří jednu odpovídajících prodejní objednávky v systému. 

Pokud výkaz není úplně zaúčtován, můžete si ve výkazu prohlédnout agregované transakce. V podokně akcí na kartě **Výkaz** ve skupině **Podrobnosti o spuštění** vyberte **Agregované transakce**.

![Tlačítko agregovaných transakcí pro výkaz, který není zcela zaúčtován.](media/aggregated-transactions.png)

Pro zaúčtované výkazy můžete zobrazit agregované transakce na stránce **Zaúčtované výkazy**. V podokně akcí vyberte **Dotazy** a pak vyberte **Agregované transakce**.

![Příkaz agregovaných transakcí pro zaúčtované výkazy.](media/aggregated-transactions-posted-statements.png)

Záložka s náhledem **Podrobnosti prodejní objednávky** agregované transakce uvádí následující informace:

- **ID záznamu** – ID záznamu souhrnné transakce.
- **Číslo výkazu** – výkaz, ke kterému souhrnná transakce patří.
- **Datum** – datum vytvoření souhrnné transakce.
- **ID prodeje** – při vytvoření prodejní objednávky ze souhrnné transakce, ID prodejní objednávky. Pokud je toto pole prázdné, odpovídající prodejní objednávka nebyla vytvořena.
- **Počet souhrnných řádků** – celkový počet řádků pro souhrnnou transakci a prodejní objednávku.
- **Stav** – stav poslední souhrnné transakce.
- **ID faktury** – při fakturaci souhrnné prodejní objednávky pro souhrnnou transakci, ID prodejní faktury. Pokud je toto pole prázdné, faktura pro prodejní objednávku nebyla zaúčtována.
- **Chybový kód** – Toto pole je nastaveno, pokud je agregace v chybovém stavu.
- **Chybová zpráva** – Toto pole je nastaveno, pokud je agregace v chybovém stavu. Udává podrobnosti o tom, co způsobilo selhání procesu. K vyřešení problému můžete použít informace v chybovém kódu a poté proces ručně restartovat. V závislosti na typu řešení může být nutné agregované prodeje odstranit a zpracovat na novém výkazu.

![Pole na záložce s náhledem Podrobnosti prodejní objednávky pro agregovanou transakci.](media/aggregated-transactions-error-message-view.png)

Záložka s náhledem **Podrobnosti o transakcích** agregované transakce zobrazuje všechny transakce, které byly převedeny do agregované transakce. Agregované řádky agregované transakce zobrazují všechny agregované záznamy z transakce. Agregované řádky také zobrazují podrobné informace, jako je položka, varianta, množství, cena, čistá částka, jednotka a sklad. Každý agregovaný řádek v zásadě odpovídá jednomu řádku prodejní objednávky.

![Podrobnosti o transakci na záložce s náhledem agregované transakce.](media/aggregated-transactions-sales-details.png)

V některých situacích mohou agregované transakce selhat při zaúčtování jejich konsolidované prodejní objednávky. V těchto situacích bude ke stavu výkazu přidružen chybový kód. Chcete-li zobrazit pouze agregované transakce, které obsahují chyby, zaškrtnutím příslušného políčka v zobrazení agregovaných transakcí můžete povolit filtr **Zobrazit pouze selhání**. Povolením tohoto filtru omezíte výsledky na agregované transakce, které obsahují chyby vyžadující řešení. Informace, jak opravit tyto chyby, najdete v části [Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků](edit-order-trans.md).

![Zaškrtávací políčko pro filtr Zobrazit pouze selhání v zobrazení agregovaných transakcí.](media/aggregated-transactions-failure-view.png)

Na stránce **Agregované transakce** si můžete stáhnout soubor XML pro určitou agregovanou transakci výběrem možnosti **Exportovat agregovaná data**. Soubor XML si můžete prohlédnout v libovolné aplikaci pro soubory XML, abyste viděli samotné podrobnosti dat, které zahrnují vytvoření a zaúčtování prodejní objednávky. Funkce pro stažení souboru XML pro agregované transakce není k dispozici pro výkazy, které byly zaúčtovány.

![Tlačítko Exportovat agregovaná data na stránce Agregované transakce.](media/aggregated-transactions-export.png)

V případě, že nemůžete chybu opravit opravou dat na prodejní objednávce nebo dat, která podporují prodejní objednávku, k dispozici je tlačítko **Odstranit objednávku odběratele**. Chcete-li odstranit objednávku, vyberte agregovanou transakci, která selhala, a poté vyberte **Odstranit objednávku odběratele**. Bude odstraněna jak agregovaná transakce, tak odpovídajících prodejní objednávka. Nyní můžete transakce zkontrolovat pomocí funkce pro úpravy a auditování. Případně je lze znovu zpracovat prostřednictvím nového výkazu. Po odstranění všech selhání můžete pokračovat v účtování výkazu spuštěním funkce pro zaúčtování příslušného výkazu.

![Tlačítko Odstranit objednávku odběratele v zobrazení agregovaných transakcí.](media/aggregated-transactions-delete-cust-order.png)

Zobrazení agregovaných transakcí poskytuje následující výhody:

- Uživatel má vhled do souhrnných transakcí, které selhaly při vytváření prodejní objednávky, a prodejních objednávek, které selhaly při fakturaci.
- Uživatel má přehled o způsobu, jakým budou transakce agregovány.
- Uživatel dokončil revizní záznam, z transakcí do prodejních objednávek, do prodejních faktur. Tento záznam pro audit nebyl k dispozici ve funkci zaúčtování výkazu ze starší verze.
- Agregovaný soubor XML usnadňuje určit problémy při vytváření prodejní objednávky a fakturaci.

> [!NOTE]
> Když jsou transakce agregovány, zaměstnanec přiřazený k transakci již není k dispozici v **Sestavě nejlepších zaměstnanců prodeje**, což znamená, že **Sestava nejlepších zaměstnanců prodeje** nezobrazí všechny transakce. Doporučujeme, abyste nepoužívali **Sestavu nejlepších zaměstnanců prodeje** s agregovanými transakcemi.

### <a name="journal-vouchers"></a>Doklady deníku

Tlačítko **Doklady deníků** ve skupině **podrobnosti o spuštění** zobrazí všechny různé transakce dokladů vytvořené pro výkaz a které se vztahují ke slevám, účtům příjmů/výdajům, dárkovým kartám a tak dále.

Program v současné době tato data zobrazuje pouze pro zaúčtované výkazy.

### <a name="payment-journals"></a>Deníky plateb

Tlačítko **Deníky plateb** ve skupině výkazu **Podrobnosti o spuštění** zobrazuje všechny různé platební deníky, které jsou vytvořeny pro výkazy.

Program v současné době tato data zobrazuje pouze pro zaúčtované výkazy.

## <a name="other-improvements"></a>Další zlepšení

Ostatní backendová vylepšení, která uživatel vidí byla provedena u funkce zaúčtování výkazu. Několik příkladů:

- Agregace nebere v úvahu zaměstnance, terminál a entity směny. Vzhledem k tomu, že je méně souhrnných parametrů, je nutné zpracovat méně řádků prodejní objednávky.
- Výskyt zablokování v tabulkách transakcí se sníží zavedením dalších tabulek rozšíření další a provedením operace vložení namísto operace úpravy tabulek transakcí.
- Počet spuštěných dávkových úloh obsahuje parametry a je omezen. Toto číslo lze tedy upravit tak, aby odpovídalo konkrétnímu prostředí zákazníka. Ve funkci starších výkazů zaúčtování byl vytvořen neomezený počet dávkových úloh současně. Výsledky byly nezvládnutelným náklady, režie a kritická místa v dávkovém serveru.
- Výkazy jsou efektivně zařazeny do fronty ke zpracování pomocí určení priority výkazů, které mají maximální počet transakcí.
- Dávkové procesy, například **Vypočítat výkazy v dávce** a **Zaúčtování výkazů v dávce** jsou spuštěny jen v dávkovém režimu. U starší funkce zaúčtování výkazu uživatelé mohli vybrat interaktivní režim ke spuštění těchto dávkových procesů s jedinou posloupností operací na rozdíl od dávkových procesů, které jsou s několika spuštěními.
- Ve starší funkci zaúčtování výkazu jakákoli chyba dávkové úlohy způsobila, že celá dávková úloha byla v chybovém stavu. Ve vylepšené funkci selhání dávkové úlohy nezpůsobila chybový stav dávkové úlohy, když byly ostatní dávkové úlohy úspěšně dokončeny. Měli byste posoudit stav zaúčtování pro spuštění dávky pomocí stránky **Výkazy**, kde můžete zobrazit všechny výkazy, které nebyly zaúčtovány z důvodu chyb.
- Ve starší funkci zaúčtování výkazu způsobí první výskyt chyb výkazu neúspěšnost celé dávkové objednávky. Zbývající výkazy nebudou zpracovány. Ve vylepšené funkci dávkového zpracování bude pokračovat zpracování všech výkazů i v případě selhání některého z výkazů. Jednou výhodou je, že uživatelé získají přehled o přesném počtu výkazů, které mají chyby. Z toho vyplývá, že uživatelé nemusí neustále opravovat chyby a spouštět proces zaúčtování výkazů, dokud nebudou zaúčtovány všechny výkazy.

## <a name="general-guidance-about-the-statement-posting-process"></a>Obecné informace o procesu zaúčtování výkazu

- Doporučujeme spouštět zaúčtování výkazu v dávce, protože dávkové zpracování využívá výhod výkonu systému dávek z hlediska multithreadingu. Multithreading je požadován za účelem zpracování velkých množství transakcí, které se běžně zobrazují při zaúčtování výkazu.
- Doporučujeme, abyste zapnuli zápornou fyzickou inventuru u modelové skupiny položek tak, aby zaúčtování bylo bezproblémové. V některých případech se nebudou moci negativní výkazy zaúčtovat, pokud neexistují záporné fyzické zásoby. Například teoreticky, pokud existuje pouze jedna jednotka zboží na skladě a byly provedeny transakce prodeje a vrácení transakce pro položku, transakce by se měly být schopné zaúčtovat, i v případě, že není povoleno záporné zásoby. Nicméně vzhledem k tomu, že proces zaúčtování výkazu vyžaduje jednu prodejní transakci a transakci vrácení v jedné objednávce, neexistuje záruka, že bude nejprve zaúčtována řádka prodeje a potom řádka vrácení. Tak může dojít k chybám. Jsou-li v tomto případě zapnuty záporné zásoby, zaúčtování transakce není negativně ovlivněno a systém bude správně odrážet zásoby.
- Doporučujeme použít agregaci, zatímco budete vypočítávat a účtovat výkazy. Proto pro některé parametry agregace doporučujeme následující nastavení:

    - Přejděte na možnost **Retail a Commerce** \> **Nastavení Headquarters** \> **Parametry** \> **Parametry Commerce**. Poté na kartě **zaúčtování** na pevné záložce **aktualizace zásob** v poli **úroveň podrobností** vyberte **Souhrn**.
    - Přejděte na možnost **Retail a Commerce** \> **Nastavení Headquarters** \> **Parametry** \> **Parametry Commerce**. Poté na kartě **zaúčtování** na pevné záložce **Agregace** nastavte možnost **transakce dokladu** na **Ano**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

