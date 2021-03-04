---
title: Moduly správy přepravy
description: Moduly správy přepravy definují logiku, které slouží ke generování a zpracování přepravní sazby v rámci správy přepravy.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab6667ac02ca55eeb093fa5854a962ac4357aaac
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424182"
---
# <a name="transportation-management-engines"></a>Moduly správy přepravy

[!include [banner](../includes/banner.md)]

Moduly správy přepravy definují logiku, které slouží ke generování a zpracování přepravní sazby v rámci správy přepravy. 

Modul správy přepravy vypočítá úlohy, například sazbu přepravy dopravce. Systém modulu vám umožní změnit strategie výpočtu za běhu, které jsou založeny na údajích v rámci aplikace Supply Chain Management. Modulu správy přepravy se podobá modulu plug-in souvisejícímu s určitou smlouvou dopravce.

## <a name="what-engines-are-available"></a>Které moduly jsou k dispozici?
Následující tabulka obsahuje moduly správy přepravy, které jsou k dispozici.

| Modul správy přepravy | Popis                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modul sazeb**                  | Vypočítá sazby.                                                                                                                                                                                                                                                                                                           |
| **Obecný modul**               | Jednoduché pomocné moduly používané jinými moduly, které nevyžadují data z aplikace Supply Chain Management, například modul pro výpočet rozdělení nákladů. Moduly pro výpočet rozdělení nákladů se používají ke snížení finálních nákladů na přepravu pro určité zakázky a řádky, které jsou založené na dimenzích, jako je například množství a hmotnost. |
| **Modul kilometrovného**               | Vypočítá vzdálenost přepravy.                                                                                                                                                                                                                                                                                     |
| **Modul mezioperačního času**          | Vypočítá potřebný pro cestovní od začátku až do konce.                                                                                                                                                                                                                                       |
| **Modul zóny**                  | Vypočítá zónu na základě aktuální adresy a počet zón, které je třeba překročit při cestě z adresy A na adresu B.                                                                                                                                                                    |
| **Typ účtu dopravného**            | Standardizuje fakturu za přepravu a řádky účtu dopravného a používá se při automatickém párování účtu dopravného.                                                                                                                                                                                                                |


<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Jaké moduly musí být nakonfigurovány pro výpočet sazby dodávky?
---------------------------------------------------

K vypočítání sazby pro určitého dopravce je nutné nakonfigurovat několik modulů správy přepravy. **Výpočet přepravních sazeb** je sice vyžadován, ale pro podporu **Výpočet přepravních sazeb** mohou být nutné také ostatní moduly. Například **Výpočet přepravních sazeb** slouží k načtení dat z **Výpočet kilometrovného** pro výpočet sazby za kilometráž mezi zdrojem a cílem.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Co je zapotřebí pro inicializaci modulu správy přepravy?
Modul správy přepravy vyžaduje určité nastavení dat inicializace. Nastavení může obsahovat následující typy dat:
-   Odkazy na další moduly správy přepravy. Další informace naleznete v příkladu konfigurace v tomto oddílu.
-   Odkazy na typy rozhraní .NET, které jsou používány v modulu správy přepravy.
-   Jednoduchá konfigurační data.

Ve většině případů můžete klepnout na tlačítko **Parametry** ve formuláři pro nastavení modulu správy přepravy a nakonfigurovat tak data inicializace. **Příklad konfigurace modul pro výpočet přepravních sazeb odkazující na modul pro výpočet kilometrovného** Následující příklad ukazuje nastavení, které je nutné pro modul pro výpočet přepravních sazeb, který je založen na typu modulu .NET Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine a odkazuje na modul pro výpočet kilometrovného.

|          Parametr           |                                                                                  Popis                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>PřidělovatelZákladuSazby</em>   | Typ rozhraní .NET, který interpretuje data pro přiřazení základní sazby v konkrétním schématu. Syntaxe hodnoty parametru se skládá ze dvou segmentů oddělených svislou čárou ( |
|  <em>KódRegistruUjetéVzdálenosti</em>  |                       Modul pro výpočet kilometrovného, který identifikuje záznam v modulu kilometrovného v databázi.                        |
| <em>PřidělovacíStroj</em> |                        Modul pro výpočet rozdělení nákladů, který identifikuje záznam ve výpočtu rozdělení nákladů v databázi.                        |

<a name="how-is-metadata-used-in-transportation-management-engines"></a>Jaké je použití metadat v modulech správy přepravy?
----------------------------------------------------------

Moduly správy přepravy, které pracují s daty, která jsou definovány v rámci Supply Chain Management, mohou používat různá datová schémata. Systém správy přepravy umožňuje různým modulům správy přepravy používat stejné obecné fyzické databázové tabulky. Abyste byla zajištěna správnost výkladu běhových dat modulu, můžete definovat metadata pro databázové tabulky. Tím lze snížit náklady na sestavení nových modulů správy přepravy, protože další struktury tabulky a formuláře nejsou v rámci operací zapotřebí.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Co lze použít jako vyhledávací data ve výpočtech sazby?
Data, která lze použít při výpočtu sazby, jsou řízena prostřednictvím konfigurace metadat. Například pokud chcete vyhledávat sazby podle PSČ, nastavte metadata podle typu vyhledávání poštovního směrovacího čísla.

## <a name="do-all-engine-configurations-require-metadata"></a>Vyžadují všechny konfigurace modulu metadata?
Ne. Moduly správy přepravy, které slouží k načtení dat, která jsou vyžadována pro výpočet sazby z externích systémů, nebudou metadat požadovat. Data sazby pro tyto moduly lze získávat z externích přepravních systémů dopravce, obvykle pomocí webové služby. Například můžete používat modul pro výpočet kilometrovného načítající data přímo z map služby Bing a metadata pro tento modul tak nepotřebujete.

| **Poznámka**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moduly správy přepravy, které jsou dodávány s aplikací Supply Chain Management pracují s daty, která se načítají z aplikace. Moduly, které se připojují k externím systémům, nejsou součástí operací. Model rozšíření využívající moduly však umožňují sestavení rozšíření pomocí nástrojů Visual Studio. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Jak mohu nastavit metadata pro modul správy přepravy?
Metadata pro moduly správy přepravy jsou nakonfigurovány odlišně pro různé typy modulů.

| Modul správy přepravy               | Konfigurace metadat                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modul sazeb**                                | Vyžaduje **typ základní sazby**. Základní typ sazby obsahuje metadata pro základní data sazby a základní data přiřazení sazby. Struktura metadat pro základní sazbu se určuje podle typu modulu pro výpočet přepravních sazeb. Struktura základních metadat pro přiřazení sazby je definována typem základní sazby přiřaditele, který je přidružený k modulu pro výpočet přepravních sazeb. Podle potřeby můžete nastavit základní typ modulu pro výpočet přepravních sazeb na stránce **Výpočet přepravních sazeb** a na stránce **Hlavní sazba**. |
| **Modul zóny**                                | Vyžaduje nastavení metadat přímo pro hlavní zónu.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Modul mezioperačního času** a **Modul kilometrovného** | Načte metadata přímo z formuláře pro nastavení konfigurace modulu pro výpočet kilometrovného.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Příklad metadat v modulu pro výpočet přepravních sazeb** Modul správy přepravy vyžaduje identifikaci původní adresy, cílového státu a země/oblasti a počáteční a koncový bod dodávky. Po použití těchto požadavků budou metadata vypadat jako údaje v následující tabulce. Tabulka obsahuje také informace o tom, jaký typ vstupních dat je zapotřebí.
-   Definujte tuto informaci pod **Správa přepravy** &gt; **Nastavení** na stránce **Typ základu sazby**.

| Klasifikace | Jméno                          | Typ pole | Datový typ | Typ vyhledávání    | Povinné |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Původní PSČ            | Přiřazení | Řetězec    | PSČ    | Vybrané  |
| 2        | Cílový stát             | Přiřazení | Řetězec    | Státní          |           |
| 3        | Cílové PSČ | Přiřazení | Řetězec    | PSČ    | Vybrané  |
| 4        | Cílové koncové PSČ   | Přiřazení | Řetězec    | PSČ    | Vybrané  |
| 5        | Cílová země           | Přiřazení | Řetězec    | Země / oblast |           |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]