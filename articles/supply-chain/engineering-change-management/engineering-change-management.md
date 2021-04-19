---
title: Správa změn technických produktů
description: Toto téma poskytuje informace o správě technických změn. Správa technických změn poskytuje strukturované procesy pro správu změn technických produktů, od navrhování, vyžádání a provádění změn, přes kontrolu a schvalování změn, hodnocení jejich dopadu na existující transakce a jejich následné sledování.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fb71d941a5cd58701f723e56a07c6b6cca6689bb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830021"
---
# <a name="manage-changes-to-engineering-products"></a>Správa změn technických produktů

[!include [banner](../includes/banner.md)]

Správa technických změn poskytuje strukturované procesy pro správu změn technických produktů. Můžete použít proces *požadavek na technickou změnu* k navržení a požadování změn a poté pomocí procesu *pořadí technických změn* tyto změny provést. Uživatelé mohou vytvářet žádosti o technické změny nebo objednávky technických změn a pak následuje proces jejich kontroly a schválení, posouzení jejich dopadu na existující transakce a následné kontroly.

## <a name="engineering-change-requests"></a>Požadavky na technickou změnu

Proces žádosti o technickou změnu vám umožní zachytit žádosti o změny ze všech příslušných oddělení ve vaší společnosti. Nezáleží na tom, zda pracujete jako inženýr, nebo v oddělení Výroba, Zajištění zdrojů, Sklad nebo Prodej: každý může použít žádost o technickou změnu a požádat o změnu. Touto změnou může být nápad na nový produkt, problém, který jste objevili při práci se stávajícím produktem, návrh na vylepšení stávajícího produktu nebo něco jiného.

Poté, co někdo podá žádost o změnu, je proces *kontroly a schválení* řízen pracovním tokem, který identifikuje, kdo musí změnu schválit (například vlastník produktu).

Chcete-li nastavit pracovní postup pro objednávky technických změn nebo žádosti o technické změny, přejděte na **Řízení technických změn \> Technické pracovní postupy**. Vyberte **Nový**, vyberte, zda bude pracovní postup použit ke kontrole objednávek technických změn nebo požadavků na technické změny, a poté nakonfigurujte pracovní postup.

Další informace o práci s pracovními postupy naleznete v tématu [Přehled systému workflow](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) Další informace o vlastnících produktů získáte v části [Vlastníci produktu](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Vytvořit nový požadavek na technickou změnu

Chcete-li vytvořit žádost o technickou změnu, proveďte některý z těchto kroků.

- Jděte na **Správa technických změn \> Společné \> Správa technických změn \> Žádost o technickou změnu** a pak v podokně akcí vyberte **Nový**.
- Otevřete stránku **Podrobnosti o produktu** pro existující technický produkt. Pak v podokně akcí na kartě **Technik** ve skupině **Správa technických změn** vyberte **Požadavek na technickou změnu \> Nový požadavek na technickou změnu**.

Je vytvořen nový požadavek na změnu. Nyní můžete nastavit pole na každé pevné záložce, jak je popsáno v následujících pododdílech.

#### <a name="general-fasttab"></a>Záložka s náhledem Obecné

Na pevné záložce **Obecné** je možné zadat základní popis požadavku na změnu. Následující tabulka popisuje pole na této pevné záložce.

| Pole | popis |
|---|---|
| Změnit požadavek | Zadejte název požadavku na technickou změnu. |
| Druh práce | Zadejte text, který stručně popisuje nebo identifikuje změny v požadavku. |
| Priorita | Vyberte hodnotu, která udává, jak vysoká je priorita změny. Podle potřeby můžete upravit dostupné hodnoty pro vaši společnost. (Další informace viz [Nastavení společných hodnot pro správu technických změn](engineering-change-management-setup.md).) |
| Kategorie | Vyberte hodnotu popisující typ změny, kterou požadujete. Podle potřeby můžete upravit dostupné hodnoty pro vaši společnost. (Další informace viz [Nastavení společných hodnot pro správu technických změn](engineering-change-management-setup.md).) |
| Závažnost | Vyberte hodnotu označující závažnost problému, který by měl být vyřešen implementací požadavku. Podle potřeby můžete upravit dostupné hodnoty pro vaši společnost. (Další informace viz [Nastavení společných hodnot pro správu technických změn](engineering-change-management-setup.md).) |
| Požaduje | Jméno uživatele, který požadavek vytvořil. |
| Dne | Datum vytvoření požadavku. |
| Stav | Stav požadavku. Při prvním vytvoření požadavku je stav *Vytvořeno*. Po schválení požadavku se stav změní na *Schváleno*. Pokud byl pro požadavek vytvořen související příkaz ke změně, změní se stav na *Navazující*. |
| Příkaz ke změně | Číslo změnového příkazu, pokud byla žádost o změnu vyřízena prostřednictvím změnového příkazu. |

#### <a name="information-fasttab"></a>Pevná záložka Informace

Na pevné záložce **Informace** můžete přidat další informace o požadavku.

Chcete-li do mřížky přidat řádek, vyberte **Nový** na panelu nástrojů nad mřížkou a poté vyberte jednu z následujících možností:

- **Soubor** – Nahrání souboru.
- **Obrázek** - Nahrajte soubor s obrázkem.
- **Poznámka** - Zadejte poznámku přímo do mřížky.
- **URL** - Zadejte adresu URL přímo do mřížky.

Následující tabulka popisuje pole na každém řádku.

| Pole | popis |
|---|---|
| Datum a čas vytvoření | Datum a čas vytvoření řádku. |
| Typ | Typ informací, pro které byl řádek vytvořen (soubor, obrázek, poznámka nebo adresa URL). |
| popis | Zadejte popis řádku. |
| Omezení | Hodnota, která označuje, zda informace, které byly přidány, pocházejí z interního nebo externího zdroje. |
| Připojeno | Vybrané zaškrtávací políčko označuje, že řádek obsahuje přílohu (soubor nebo obrázek). Chcete-li stáhnout přílohu, vyberte řádek a poté vyberte **Otevřít** na panelu nástrojů nad mřížkou. |

#### <a name="products-fasttab"></a>Pevná záložka Produkty

Pevná záložka **Produkty** umožňuje zobrazit seznam všech produktů, kterých se požadavek na změnu týká. Tlačítka na panelu nástrojů můžete používat k přidání produktů do mřížky nebo jejich odstranění z mřížky.

Tento seznam slouží pouze pro informaci. Proto můžete přidat tolik souvisejících produktů, kolik považujete za relevantní. Pokud vytvoříte žádost o změnu ze stránky **Detaily produktu** pro existující produkt, tento produkt by měl být uveden na pevné záložce **Produkty** po uložení záznamu požadavku.

#### <a name="source-fasttab"></a>Pevná záložka Zdroj

Pevná záložka **Zdroj** umožňuje sledovat počáteční bod požadavku na změnu. To je užitečné, pokud například chcete zjistit, zda byl požadavek na změnu vytvořen z prodejní objednávky, kdo ji vytvořil a ve které společnosti byl vytvořen.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Vyhodnoťte obchodní dopad požadavku na změnu

Když zkontrolujete požadavek na změnu, můžete vyhledat závislosti. Tímto způsobem můžete posoudit dopad požadované změny na otevřené transakce, jako jsou prodejní objednávky, výrobní objednávky a okamžité zásoby.

1. Přejděte na **Správa technických změn \> Společné \> Správa technických změn \> Požadavky na technickou změnu**.
1. Otevřete existující požadavek na změnu nebo vyberte **Nový** v podokně akcí a vytvořte nový požadavek na změnu.
1. V podokně akcí na kartě **Požadavek na změnu** ve skupině **Dopad na podnikání** vyberte jedno z následujících tlačítek:

    - **Vyhledávání** - Naskenuje všechny otevřené transakce a poté otevře dialogové okno **Dopad podnikání na otevřené transakce**, kde je uveden seznam všech transakcí, které budou změnou ovlivněny.
    - **Zobrazit předchozí vyhledávání** - Otevře dialogové okno **Dopad podnikání na otevřené transakce**, ve kterém je uveden seznam předchozích výsledků vyhledávání. (Nové vyhledávání není provedeno.)

1. Pokud se problém, který vyžaduje změnu, považuje za kritický, můžete blokovat otevřené transakce nebo upozornit odpovědného uživatele pomocí tlačítek na panelu nástrojů v dialogovém okně **Dopad podnikání na otevřené transakce**.

### <a name="create-a-change-order-from-a-change-request"></a>Vytvoření změnového příkazu z požadavku na změnu

Technik, který kontroluje žádost o technickou změnu, může vytvořit objednávku technické změny přímo ze stránky **Požadavky na technické změny**. V podokně akcí na kartě **Změnit požadavek** ve skupině **Pořadí technických změn** vyberte **Kopírovat odkaz a produkty**.

## <a name="engineering-change-orders"></a>Příkazy k technických změnám

Příkazy technických změn poskytují strukturovaný proces pro správu změn technických produktů. Navrhujete změny pomocí kopie technických dat. Skutečná kmenová data nejsou ovlivněna. Další informace o relevantních technických datech najdete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

Můžete vytvořit objednávku technické změny, která je založena na schváleném požadavku na technickou změnu. Technici mohou také vytvářet technické změny od začátku. Podle jednoho z těchto kroků můžete do jedné objednávky technické změny zahrnout více produktů:

- Ručně vyberte produkty.
- Pomocí kusovníku (BOM) zahrňte produkty, které jsou nižší ve struktuře produktu (tj. podřízené).
- Pomocí vyhledávání podle místa můžete zahrnout produkty, které jsou ve struktuře produktů vyšší (tj. nadřazené).

Po dokončení návrhu změn bude proces kontroly a schválení zpracován pracovním tokem. Můžete nastavit různé pracovní postupy na základě priority a závažnosti.

Chcete-li nastavit pracovní postup pro objednávky technických změn nebo žádosti o technické změny, přejděte na **Řízení technických změn \> Technické pracovní postupy**. Vyberte **Nový**, vyberte, zda bude pracovní postup použit ke kontrole objednávek technických změn nebo požadavků na technické změny, a poté nakonfigurujte pracovní postup.

Další informace o práci s pracovními postupy naleznete v tématu [Přehled systému workflow](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)

Zde jsou některé typické zúčastněné strany, které možná budou muset schválit objednávku technické změny:

- **Vlastníci produktu** – Další informace o vlastnících produktů získáte v části [Vlastníci produktu](product-owner.md).
- **Zodpovědný vedoucí týmu** – pole **Technik** v zobrazení **záhlaví** příkazu k technické změně zobrazuje technika, který je za příkaz ke změně odpovědný. Pokud technik patří k týmu, který je definován v systému, v poli **Odpovědný** je uveden vedoucí týmu.
- **Finanční oddělení** - Finanční oddělení možná bude muset přezkoumat případy, kdy změna vyžaduje vysoké náklady.

Můžete si vybrat, zda má být objednávka technické změny zpracována přímo po schválení, jako součást pracovního postupu, nebo zda má být zpracování provedeno později, jako ruční krok. Během zpracování objednávky technické změny jsou aktualizována technická data o skutečném produktu.

Během kontroly žádosti o změnu v podokně akcí na kartě **Změnit požadavek** ve skupině **Dopad na podnikání** vyberte **Vyhledávání** k posouzení dopadu navrhované změny na otevřené transakce, jako jsou prodejní objednávky, výrobní objednávky a zásoby na skladě. Výsledky jsou uvedeny v dialogovém okně **Dopad podnikání na otevřené transakce**, kde můžete vybrat ovlivněné transakce a poté pomocí příkazů na panelu nástrojů zobrazit další informace, upozornit odpovědného uživatele nebo blokovat transakci.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Objednávky technických změn ve strojírenských nebo provozních společnostech

Jak je popsáno v tématu [Pravidla technických společností a vlastnictví dat](engineering-org-data-ownership-rules.md), údaje o produktu, které můžete upravit, se liší v závislosti na typu právnické osoby, ve které pracujete (strojírenská společnost versus provozní společnost). Pravidla vlastnictví dat se také použijí na objednávky technických změn. Proto můžete v závislosti na právnické osobě, kde vytvoříte objednávku technické změny, provést různé typy změn. Několik příkladů:

- Pro objednávky technických změn v **technické společnosti** můžete provést základní změny technických dat. Můžete například vytvořit nové verze produktu, změnit strukturu produktu pomocí kusovníku a změnit hodnoty technických atributů. U každého ovlivněného produktu vyberte jednu z následujících hodnot v poli **Dopad** :

    - **Žádný** - Aktualizujte stávající verzi produktu (aktualizace ve verzi).
    - **Nová verze** - Vytvořte novou verzi založenou na vybrané verzi produktu.
    - **Nový produkt** - Vytvořte zcela nový produkt nebo variantu produktu, která je založena na vybrané verzi produktu.

- Pro objednávky technických změn v **provozní společnost** můžete změnit logistická data produktu. Můžete například obohatit stávající kusovník nastavením pro získávání zdrojů, přidat místní trasy nebo místní kusovníky a dokonce obohatit kusovník přidáním nových řádků kusovníku pro místní obalový materiál, mazací kapaliny nebo pokyny v místním jazyce. Obohacení, která uživatelé provádějí v provozní společnosti, budou zachována, když budou zaslány nové aktualizace od technické společnosti. Další informace viz [Pravidla technických společností a vlastnictví dat](engineering-org-data-ownership-rules.md).

    Když jsou objednávky technické změny zpracovávány v technické společnosti, produkty jsou vytvářeny a/nebo aktualizovány pouze v technické společnosti. Pokud by se tedy měla aktualizovat také kmenová data produktu, musíte produkty také vydat provozním společnostem.

- Produkty můžete vydávat přímo z objednávek technických změn. Otevřete pořadí změn a poté v podokně akcí na kartě **Změnit objednávku** ve skupině **Vydání produktu** vyberte **Vydat strukturu produktu**. Tento proces funguje stejně, jako když vydáváte produkty ze stránky **Vydané produkty**. Další informace naleznete v tématu [Vydání struktur produktu](release-product-structure.md).
- Můžete nechat produkty automaticky vydat z objednávek technických změn na základě následujících faktorů:

    - Opětovné vydání společnostem, kde byly dříve vydány produkty. Vyberte **Vyhledávání** k prohledání všech předchozích vydání a poté vyberte **Zobrazit** k zobrazení výsledků. Stránka **Zobrazení** ukazuje předchozí vydání produktu a vy si můžete vybrat, které produkty chcete znovu vydat. Poté zavřete stránku **Zobrazení** a vyberte **Proces** k opětovnému vydání vybraných produktů.
    - Nastavení automatického vydání v řízení uvolnění kategorie technického produktu. Toto vydání můžete provést jako součást pracovního postupu. Při použití bloku **Shromáždit návrh na vydání** bude návrh na vydání vyplněn návrhy na opětovné vydání (viz předchozí položka seznamu) a produkty budou vydány společnostem, pokud je v ovládacím prvku vydání kategorie technického produktu zaškrtnuto políčko **Automatické vydání**. Můžete vybrat **Zobrazení** k zobrazení výsledků, jak je popsáno v předchozí položce seznamu. Produkty budou také vydány, když bude použit blok **návrh na vydání procesu**. Pokud se rozhodnete shromáždit návrh vydání jen jako součást pracovního postupu, můžete vydání spustit ručně výběrem **Proces**, jak je popsáno v předchozí položce seznamu.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>V návaznosti na požadavek technické změny prostřednictvím objednávky technické změny

Objednávku technické změny můžete vytvořit hned po schválení požadavku na technickou změnu. Můžete kombinovat více požadavků na technické změny do jednoho příkazu technických změn. Jedna objednávka technických změn může dokonce zahrnovat více produktů. (Obvykle používáte tento přístup, když musí být stejná změna použita pro více produktů.) Nelze však vytvořit více objednávek technických změn z jednoho požadavku na technickou změnu.

Chcete-li navázat na žádost o změnu prostřednictvím objednávky změn, otevřete žádost o změnu a poté v podokně akcí na kartě **Změnit objednávku** ve skupině **Pořadí technických změn** vyberte **Kopírovat odkaz a produkty**. Poté můžete vybrat existující objednávku technické změny, ke které chcete připojit požadavek na změnu, nebo můžete vytvořit novou objednávku technické změny pro tento konkrétní požadavek.

## <a name="engineering-change-order-report"></a>Sestava příkazu k technické změně

Výkazy pořadí technických změn popisují změny, které byly provedeny v pořadí technických změn. Jsou užitečné jak během, tak po procesu kontroly a schválení.

Chcete-li zobrazit sestavu objednávky technické změny, otevřete příslušnou objednávku změny a poté v podokně akcí na kartě **Změnit objednávku** ve skupině **Zobrazení** vyberte **Zpráva o objednávce technických změn**.

## <a name="fields-on-an-engineering-change-order"></a>Pole s objednávkou technických změn

Většina polí u objednávek technických změn je stejná jako pole pro vydané produkty, technické verze, dokumenty, kusovníky (řádky) a trasy (operace). Pole v následující tabulce jsou však jedinečná pro změnu pořadí.

| Pole | popis |
|---|---|
| Důvody technických změn | Vyberte důvod změny dotčeného produktu. |
| Popis změny | Zadejte popis změny. |
| Vyžadovány speciální nástroje | Určete, zda je k provedení změny nutné použít speciální nástroje. |
| Dispozice technického materiálu | Vyberte kód dispozice materiálu pro veškerý odpad, který vznikne při uplatnění změny. |
| Vyžaduje se souhlas zákazníka | Určete, zda je před provedením změny vyžadován souhlas zákazníka. |
| Přijatý souhlas zákazníka | Určete stav schválení zákazníka. |
| Bezpečnost, ochrana zdraví a životního prostředí | Uveďte, zda se na změnu vztahují pravidla ochrany životního prostředí a bezpečnosti. Pokud ano, můžete vybrat příslušná pravidla. |

Můžete použít tlačítko **Údržba / kopírování informací o změně** ke kopírování informací o změně mezi ovlivněnými produkty.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]