---
title: Správa folií
description: Toto téma popisuje, jak pracovat s folii. Folio se obvykle skládá ze zboží jednoho dodavatele pro jednu entitu nebo společnost na zásilku. Zboží ve foliu může být v jednom kontejneru, nebo může být rozloženo mezi více kontejnerů.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5b84237844ec1d8f6c0716a0a13b05c83b358901
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575769"
---
# <a name="manage-folios"></a>Správa folií

[!include [banner](../../includes/banner.md)]

Folio je často určeno celní předpisy. Může se skládat ze zboží jednoho dodavatele pro jednu entitu nebo společnost na zásilku. Zboží ve foliu může být v jednom kontejneru, nebo může být rozloženo mezi více kontejnerů.

Chcete-li otevřít stránku **Všechna folia** přejděte na **Náklady za doručení \> Folia \> Všechna folia**. Tato stránka zobrazuje seznam všech aktuálních folií. Pomocí tlačítek v podokně akcí můžete vytvářet či odstraňovat folia a pracovat s nimi. Vyberte jakékoli folio v seznamu a zobrazte jeho podrobnosti na stránce **Folia**.

## <a name="action-pane"></a>Podokno akcí

Podokno akcí na stránkách **Všechna folia** a **Folia** poskytuje tlačítka, která vám umožní pracovat s vybraným foliem. Každé tlačítko provádí jednu akci. Podokno akcí také obsahuje karty, z nichž každá zase poskytuje sadu souvisejících tlačítek. Není-li uvedeno jinak, jsou všechna tlačítka a karty, které jsou popsány v následujících podsekcích, k dispozici jak v zobrazení seznamu (tj. na stránce **Všechna folia**) a v podrobném zobrazení (tj. na stránce **Folia**).

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Tlačítka, která se zobrazují přímo v podokně akcí

V následující tabulce jsou popsána tlačítka, která jsou k dispozici přímo v podoknu akcí.

| Tlačítko | popis |
|---|---|
| Nová | Vytvoří folio. |
| Odstranit | Odstraní otevřené nebo vybrané folio. |
| Náklady na cestu | Otevře stránku **Náklady na cestu**, kde si můžete prohlédnout a přidat náklady na úrovni folia ke všemu zboží na cestě. Když jsou náklady folia ručně přidány do cesty, automaticky se přidají do stránky dotazu na náklady a rozdělí se ke každému zboží podle metody, která je uvedena na stránce **Náklady na cestu**. |

### <a name="buttons-on-the-manage-tab"></a>Tlačítka na kartě Správa

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Spravovat** podokna akcí.

| Tlačítko | popis |
|---|---|
| Zaúčtovat příjemky | Zaúčtuje seznam příjemek pro všechny řádky nákupní objednávky ve foliu. Pokud se používají zásilky s více společnostmi, otevře se pro každou společnost nové dialogové okno účtování seznamu příjemek. |
| Zaúčtovat příjemku produktu | Zaúčtuje příjemku produktu pro všechny řádky nákupní objednávky ve foliu. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost dialogové okno účtování nové příjemky produktu. |
| Zaúčtovat fakturu | Zaúčtuje fakturu pro všechny řádky nákupní objednávky ve foliu. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost nové dialogové okno účtování faktury. |
| Převodní příkaz expedice | Zaúčtuje převodní příkaz pro všechny řádky převodního příkazu, které souvisejí s aktuálním foliem v související zásilce. |
| Přijmout převodní příkaz | Zaúčtuje příjemku převodního příkazu pro všechny řádky převodního příkazu, které souvisejí s aktuálním foliem v související zásilce. |
| Přijmout přepravované zboží | Přijme všechny řádky objednávky, které jsou ve foliu přepravovány. |
| Přijaté dokumenty | Aktualizuje nastavení možnosti **Doklady přijaty** na *Ano*. Toto tlačítko můžete použít k uzamčení položky nebo řádku nákupu, aby ji nebylo možné dále aktualizovat. |
| Najít automatické náklady | Najde příslušné náklady na cestu. Pokud tyto náklady již byly nalezeny nebo aktualizovány, zobrazí se následující zpráva: „Existují nevyfakturované řádky nákladů. Chcete je přepsat?“ Upozorňujeme, že náklady na cestu spojené s foliem, které byly fakturovány, nebudou přepsány. |
| Vytvořit deník doručení | Generuje deník doručení pro organizace pomocí pokročilých funkcí skladu. Můžete vybrat hodnoty **Inicializovat množství** (doporučeno), **Vytvořit z přepravovaného zboží** anebo **Vytvořit z nákupních objednávek**. Poslední možnost závisí na tom, zda se používá zpracování přepravovaného zboží. |
| Časově rozlišené náklady | Shromáždí náklady, pokud má typ nákladů pro debet zadaný účet hlavní knihy. Toto tlačítko se obvykle používá, když je zboží na cestě, nebo když bylo zboží přijato a fakturováno. |

### <a name="buttons-on-the-general-tab"></a>Tlačítka na kartě Obecné

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na kartě **Obecné** podokna akcí.

| Tlačítko | popis |
|---|---|
| Příjemka | Zaúčtuje seznam příjemek pro všechny řádky nákupní objednávky ve foliu. Pokud se používají cesty s více společnostmi, otevře se pro každou společnost nové dialogové okno účtování seznamu příjemek. |
| Příjemka produktu | Zobrazí záznam o příjemce produktu, pokud je použit. |
| Doručení položky | Zobrazí deník doručení zboží, pokud je použit. |
| Dotaz na náklady | Otevře stránku s dotazem na náklady a zobrazí všechny náklady na cestu, včetně přepravního kontejneru, folia a nákupní objednávky. Přesné zobrazení stránky můžete upravit pomocí akce Zobrazit. Na stránce s dotazem na náklady si můžete prohlédnout kteroukoli z oblastí včetně položky a kódu typu nákladů. Odebráním těchto položek můžete stránku upravit seskupením nákladů. Tato funkce může být užitečná, pokud používáte velikosti a barvy. Dimenze, které se zobrazují na stránce, je možné změnit. Stránka **Náklady** zobrazuje pouze kódy typů nákladů, kde pole **MD** na kartě **Zaúčtování** je nastaveno na *Položka*. |

## <a name="header-view"></a>Zobrazení záhlaví

Chcete-li otevřít zobrazení **Záhlaví**, otevřete folio a poté vyberte kartu **Záhlaví** v pravém horním rohu záhlaví folia.

### <a name="settings-on-the-general-fasttab"></a>Nastavení na záložce Obecné

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Obecné** zobrazení **Záhlaví** folia.

| Pole | popis |
|---|---|
| Folio | Název folia. Tento název se automaticky generuje při vytvoření folia.|
| Cesta | Cesta, která je přiřazena k foliu. |
| Celní deklarant | Vyberte celního makléře pro folio. Celní makléři jsou definováni u dodavatele. Umožňují automatické stanovení vytvořených nákladů. |
| Letecký nákladní list / přepravní doklad | Uveďte domovský letecký nákladní list nebo přepravní doklad, který platí pro folio. |
| Společnost | ID právnické osoby (společnosti), která je přidružena k foliu. |
| Kontrolní číslo nákladu | Toto pole používají celní oddělení v některých zemích nebo regionech. |
| Měrný systém | Toto pole umožňuje specifikovat měrný systém v modulu **Náklady za doručení**. Měrné systémy často používají organizace, které neznají individuální objem nebo hmotnost zboží, ale které vyžadují přesnější rozdělení, než jaké dovolují částky nebo množství. Spedice zajistí měření hmotnosti nebo objemu, a vy změřené údaje zapíšete na úrovni položky nebo nákupní objednávky. Může být automaticky aktualizováno, pokud je parametr vybrán nebo zadán ručně. |
| Měrná jednotka | Jednotka, která se vztahuje na zadaný měrný systém. |
| Počet kartonů | Počet kartonů ve foliu. Toto pole lze automaticky aktualizovat v závislosti na výběru parametru. |
| Účet dodavatele | Vyberte dodavatele, který je přidružený k foliu. Toto pole je určeno pouze pro informaci. Neovlivňuje žádnou funkčnost. |
| Jméno | Název aktuálně vybraného účtu dodavatele. |
| Poznámky | Zadejte veškeré doplňující informace související s foliem. |
| Popis zboží | Vyberte popis zboží, který pomůže identifikovat folio. Více informací naleznete v tématu [Popis zboží](shipping-information-setup.md#description-of-goods). |
| Datum ocenění | Toto pole souvisí se stránkou pro zadávání cel. Modul **Náklady za doručení** použije celní směnný kurz pro datum, které zde nastavíte. Výchozí hodnota je datum na stránce zadání cla. |
| ID cla | Zadejte ID cla. Toto ID poskytují celní oddělení v zemích nebo regionech. |
| Tarifní kód | Zadejte tarifní kód, který se přidruží k foliu. Tento kód je obvykle vyžadován (a definován) cílovou zemí nebo regionem. |

### <a name="settings-on-the-delivery-fasttab"></a>Nastavení na záložce Dodání

Následující tabulka popisuje nastavení, která jsou k dispozici na záložce **Dodání** zobrazení **Záhlaví** folia.

| Pole | popis |
|---|---|
| Datum folia | Vyberte datum, které chcete přidružit k foliu. Výchozí hodnota je datum vytvoření cesty. |
| Odhadovaný čas doručení do přístavu | Odhadovaný čas příjezdu (ETA) do cílového přístavu (přístav „do“). |
| Odhadované datum doručení | Obvykle datum, kdy má zboží dorazit do skladu. Toto pole se nepoužívá, když se počítá odhadované datum dodání. (Místo toho se používá odhadované datum dodání řízení sledování.) Chcete-li toto pole nastavit tak, aby se hodnota shodovala s odhadovaným datem dodání řízení sledování, použijte [Řídicí centrum sledování](delivery-information-setup.md#tracking-control-center). |
| Přijaté původní dokumenty | Datum přijetí původních dokladů. |
| Doporučeno zprostředkovatelem | Datum informování makléře. |
| Byl odeslán původní přepravní doklad | Datum, kdy byl odeslán původní nákladní list. |
| Uvolněné zboží | Datum propuštění zboží. |
| Schůzka zákazníka | Datum schůzky se zákazníkem. |
| Doručeno na sklad | Datum, kdy bylo zboží doručeno do skladu. |
| Datum ověření | Datum ověření. |
| Instrukce k doručení | Datum přijetí pokynů pro doručení. |
| Výchozí přístav | Přístav, ze kterého cesta vychází. |
| Cílový přístav | Přístav, kam cesta dorazí. Přepravní kontejner může mít jiný přístav, protože loď se může zastavit ve více přístavech. |

### <a name="settings-on-the-export-fasttab"></a>Nastavení na záložce Export

Následující tabulka popisuje nastavení, která jsou k dispozici na záložce **Export** zobrazení **Záhlaví** folia.

| Pole | popis |
|---|---|
| Vývozce | Vývozce může být uložen ve foliu. V mezinárodním obchodě můžete odeslat nákupní objednávku jedné společnosti, ale zboží obdržíte od jiné společnosti. Sledování a dokumentace jsou vyžadovány celními orgány. Zde lze uložit název a adresu vývozce. |
| Jméno | Název vybraného vývozce. |

## <a name="lines-view"></a>Zobrazení řádků

Chcete-li otevřít zobrazení **Řádky**, otevřete folio a poté vyberte kartu **Řádky** v pravém horním rohu záhlaví folia.

### <a name="information-on-the-folio-fasttab"></a>Informace na záložce Folio

Záložka **Folio** v zobrazení **Řádky** zobrazuje informace o foliu. Většina z těchto informací se také objevuje v zobrazení **Záhlaví**, jak je popsáno výše v tomto tématu.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informace a tlačítka na záložce Řádky

Záložka **Řádky** v zobrazení **Řádky** ukazuje podrobnosti o každém úplném nebo částečném řádku nákupní objednávky, který je zahrnut v aktuálním foliu.

V následující tabulce jsou popsána tlačítka, která jsou k dispozici na záložce **Řádky** v zobrazení **Řádky**.

| Tlačítko | popis |
|---|---|
| Odebrat | Odebere z cesty vybraný řádek nákupní objednávky. |
| Zásoby \> Transakce | Zobrazí transakce zásob pro vybraný řádek nákupní objednávky. Pokud používáte přepravované zboží, zobrazí se také původní objednávka a objednávky přepravovaného zboží. |
| Zásoby \> Zobrazit dimenze | Otevře dialogové okno, kde můžete vybrat dimenze zásob pro zobrazené transakce. |
| Znovu načíst | Aktualizuje informace, které souvisejí s množstvím, hmotností nebo objemem vybraného řádku nákupní objednávky. |

### <a name="information-on-the-lines-details-fasttab"></a>Informace na záložce Podrobnosti řádků

Záložka **Podrobnosti řádků** v zobrazení **Řádky** ukazuje podrobnosti o řádku nákupní objednávky, který je aktuálně vybrán na záložce **Řádky**.
