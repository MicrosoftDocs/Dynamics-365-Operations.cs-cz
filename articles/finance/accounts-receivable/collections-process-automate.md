---
title: Automatizace procesů inkasa
description: Tohle téma popisuje, jak vytvořit strategie procesu inkasa, které automaticky identifikují faktury zákazníka, které vyžadují e-mailové připomenutí, aktivitu inkasa (například telefonický hovor) nebo odeslání upomínky zákazníkovi.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a63058904df72a7fda5a67ed1e6a846eed393ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969694"
---
# <a name="collections-process-automation"></a>Automatizace procesů inkasa

[!include [banner](../includes/banner.md)]

Tohle téma popisuje, jak vytvořit strategie procesu inkasa, které automaticky identifikují faktury zákazníka, které vyžadují e-mailové připomenutí, aktivitu inkasa (například telefonický hovor) nebo odeslání upomínky zákazníkovi. 

Organizace tráví značné množství času zkoumáním sestav splatných zůstatků, zákaznických účtů a otevřených faktur, aby určily, které zákazníky je třeba kontaktovat ohledně otevřené faktury nebo zůstatku na účtu. Tento výzkum ubírá čas, který by inkasní agent mohl strávit komunikací se zákazníky za účelem shromažďování zůstatků po splatnosti nebo řešení sporů o faktury. Automatizace procesu inkasa vám umožňuje vytvořit strategický přístup k procesu inkasa. To vám pomůže konzistentně používat inkasní aktivity poskytnutím přizpůsobených e-mailových připomenutí nebo naprogramovaného procesu odesílání upomínek. 

## <a name="collections-process-setup"></a>Nastavení procesu inkasa
Můžete použít stránku **Nastavení procesu inkasa** (**Kredit a inkasa > Nastavení > Nastavení procesu inkasa**) k vytvoření automatizovaného procesu inkasa, který bude plánovat aktivity, odesílat e-mailové zprávy a vytvářet a zaúčtovávat upomínky zákazníka. Kroky procesu jsou založeny na přední nebo nejstarší otevřené faktuře. Každý krok používá tuto fakturu k určení, jaká komunikace nebo aktivita by měla probíhat s konkrétním zákazníkem.  

### <a name="process-hierarchy"></a>Hierarchie procesu
Každý fond zákazníků lze přiřadit pouze jedné hierarchii procesů. Pořadí hierarchie v tomto kroku určuje, který proces bude mít přednost, pokud je zákazník součástí více než jedné skupiny, která má přiřazenu hierarchii procesů. ID fondu určuje, kterým zákazníkům bude proces přiřazen. 

Tiché dny zajišťují, že zákazník není automatizovaným procesem kontaktován příliš často.  Například pokud jsou tiché dny nastaveny na dva, nebude zákazník kontaktován automatizovaným procesem po dobu nejméně dvou dnů, a to ani v případě, že byla původní přední faktura vyrovnána v plném rozsahu. 

Chcete-li vyloučit zákazníky z automatizace procesu, pokud je zůstatek na účtu nebo zůstatek na faktuře menší než definovaná hodnota, nastavte pole **Vyloučit z procesu** na **Ano** a zadejte hodnotu částky.

## <a name="process-details"></a>Podrobnosti o procesu
**Popis** se používá k identifikaci účelu nebo názvu kroku v hierarchii.

**Typ akce** definuje, zda krok vytvoří aktivitu, pošle e-mail nebo vytvoří upomínku.

**Obchodní dokument** definuje šablonu použitou k vytvoření typu akce.  Může to být šablona aktivity, šablona e-mailu nebo upomínka pro zákazníka. 

Typy akcí lze vytvořit buď před, nebo po datu splatnosti faktury, na základě nastavení, které je zobrazeno ve sloupci **Dny ve vztahu k datu splatnosti faktury**.

Když vyberete typ e-mailové akce, podle příjemce se určí, zda se jedná o zákazníka, prodejní skupinu nebo inkasního agenta. Hodnota v poli **Kontakt obchodního účelu** pak určí, který kontakt z účtu daného zákazníka obdrží komunikaci.

## <a name="business-document-details"></a>Podrobnosti obchodního dokumentu
Podrobnosti obchodního dokumentu se budou lišit podle typu akce, který je vybrán v podrobnostech procesu.  Když je typ akce aktivita, zobrazí se podrobnosti šablony aktivity.  Mezi tyto podrobnosti patří název šablony aktivity, typ aktivity, která bude vytvořena, účel aktivity, počet dní naplánovaných na dokončení aktivity a podrobnosti aktivity.  Tato aktivita poté bude odkazovat na přední fakturu, která informuje příjemce o akci, která je k dokončení aktivity nutná.

Pokud je typ akce e-mail v podrobnostech procesu, bude tato část obsahovat dvě záložky s náhledem.  První se používá k definování ID šablony, popisu e-mailu, výchozího jazyka, uživatelského jména, které bude přiřazeno automaticky odesílaným e-mailovým zprávám, a e-mailových adres přidružených odesílatelů. Na druhé lze vytvořit tělo e-mailu po uložení hodnot v polích **Jazyk** a **Předmět** výběrem volby **Upravit**.  Otevře se okno, které umožňuje nahrát obsah HTML. Můžete také ručně zadat zprávu do levého dolního pole okna.  

> [!Note]
> E-mail aplikace Outlook lze uložit s požadovaným tělem komunikace ve formátu HTML. To pak může být nahráno při implementaci šablony. <br> <br> Pokud je vybrán typ akce upomínky, ve formuláři nastavení nebude sekce podrobností obchodního dokumentu.


## <a name="fasttab-reference"></a>Odkaz na záložku s náhledem
V následujících tabulkách je uveden seznam stránek a polí, ze kterých lze získat přístup k zadaným záložkám s náhledem spolu s popisem informací na této kartě. 

### <a name="process-hierarchy"></a>Hierarchie procesu

|     Strana                                                  |     Pole                         |     popis                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Nastavení procesu inkasa <br> Automatizace procesů       |                                   |     Vytvářejte a spravujte procesy inkasa na základě přiřazených fondů zákazníků.                                                                                                                             |
|     Nastavení procesu inkasa <br> Automatizace procesů       |     Hierarchie                     |     Definuje prioritu automatizace procesů přiřazení zákazníka, pokud patří do více fondů.                                                                                                   |
|     Nastavení procesu inkasa <br> Automatizace procesů       |     ID fondu                       |     Dotazy, které definují skupinu záznamů zákazníků.                                                                                                                                                        |
|     Nastavení procesu inkasa <br> Automatizace procesů       |     Dny klidu                    |     Určuje, jak často lze provést krok procesu. Například pokud jsou nastaveny dva tiché dny, další krok procesu nenastane po dobu alespoň dvou dnů, pokud se změní přední faktura.     |
|     Nastavení procesu inkasa <br> Automatizace procesů       |     Vyloučení z procesu        |     Výběrem voleb **Splatný zůstatek zákazníka je nižší než** nebo **Částka faktury je nižší než** vyloučí zákazníka z automatizace procesů, pokud nejsou splněna kritéria hodnoty.                                   |

### <a name="process-details"></a>Podrobnosti o procesu
|     Strana                                                  |     Pole                                         |      popis                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Nastavení procesu inkasa <br> Automatizace procesů       |                                                   |     Definuje kroky na základě přední faktury.                                                                                                |
|                                                           |     popis                                   |     Pole neformátovaného textu pro zadání názvu a/nebo popisu kroku.                                                                           |
|                                                           |     Typ akce                                   |     Aktivita, e-mail nebo upomínka, která bude vytvořena v kroku procesu.                                                                     |
|                                                           |     Obchodní dokument                           |     Definuje šablonu aktivity nebo e-mailu, která se použije během kroku procesu.                                                                        |
|                                                           |     Kdy                                          |     Definuje, zda bude krok procesu probíhat před nebo po datu splatnosti přední faktury spolu s polem **Dny ve vztahu k datu splatnosti faktury**.        |
|                                                           |     Dny ve vztahu k datu splatnosti faktury        |     Spolu s polem **Když** určuje načasování kroku procesu.                                                                          |
|                                                           |     Příjemce                                     |     Určuje, zda bude e-mail zaslán na adresu kontaktu zákazníka, prodejní skupiny nebo inkasního agenta.                                                   |
|                                                           |     Kontakt obchodního účelu                    |     Určuje, která e-mailová adresa příjemce se použije v e-mailové komunikaci.                                                                                 |

### <a name="business-process-activity-template-details"></a>Podrobnosti o šabloně aktivity obchodního procesu 
|     Strana                                                  |     Pole                     |      popis                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Nastavení procesu inkasa <br> Automatizace procesů       |                               |     Část procesu nastavení, která určuje podrobnosti šablony aktivity.                                                                      |
|     Nastavení procesu inkasa <br> Automatizace procesů       |     Šablona aktivit       |     Určuje typ, účel, počet dní do dokončení a poskytuje podrobnosti o aktivitě, která bude vytvořena během kroku procesu aktivity.       |

### <a name="business-document-email-template-details"></a>Podrobnosti o šabloně e-mailu obchodního dokumentu 
|     Strana                                                  |     Pole     |      popis                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Nastavení procesu inkasa <br> Automatizace procesů       |               |     Určuje popis e-mailu, výchozí jazyk, jméno odesílatele a e-mailovou adresu, které budou vytvořeny během kroku procesu e-mailu.        |


### <a name="collections-history"></a>Historie inkas 
|     Strana                              |     Pole     |      popis                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Nastavení procesu inkasa       |               |     Zobrazí nedávnou historii pro vybranou hierarchii procesů.     |

### <a name="collection-process-assignment"></a>Přiřazení procesu inkasa
|     Strana                              |     Pole     |      popis                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Nastavení procesu inkasa       |               |     Zobrazí zákazníky přiřazené k procesu inkasa.  
|     Ruční přiřazení               |               |     Zobrazení zákazníků, kteří byli ručně přiřazeni k procesu, nebo výběr zákazníků, kteří mají být přiřazeni k procesu. |
|     Verze Preview přiřazení procesu      |               |     Náhled zákazníků, kteří budou přiřazeni ke strategii, jakmile bude spuštěna.   |
|     Verze Preview přiřazení zákazníka     |               |     Zobrazení strategie, ke které je přiřazen konkrétní zákazník.    |
 
### <a name="parameters"></a>Parametry
|     Strana                                                                  |     Pole                                             |      popis                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Parametry pohledávek > Automatizace procesu inkasa     |     Procento zákazníků na dávkový úkol          |     Nastavení určující počet dávkových úloh na proces automatizace.                                          |
|     Parametry pohledávek > Automatizace procesu inkasa     |     Automatické zaúčtování upomínek           |     Typy akcí upomínek, které zaúčtují upomínku během automatizace.                                      |
|     Parametry pohledávek > Automatizace procesu inkasa     |     Vytváření aktivit pro automatizaci                |     Vytváření a uzavírání aktivit pro typy akcí bez aktivity, abyste mohli zobrazit všechny automatické kroky provedené v účtu.        |
|     Parametry pohledávek > Automatizace procesu inkasa     |     Dny uchování automatizace procesu inkasa     |     Definuje počet dní, po které je uchována historie inkas.                                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]