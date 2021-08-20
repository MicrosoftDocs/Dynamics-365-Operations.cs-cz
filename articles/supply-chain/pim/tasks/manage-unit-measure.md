---
title: Správa měrných jednotek
description: Toto téma popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746932"
---
# <a name="manage-units-of-measure"></a>Správa měrných jednotek

[!include [banner](../../includes/banner.md)]

Toto téma popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.

## <a name="open-the-units-page"></a>Otevřete stránku Jednotky.

Chcete-li vytvořit a pracovat s měrnými jednotkami, které jsou k dispozici ve vašem systému, přejděte na **Správa organizace \> Nastavení \> Jednotky \> Jednotky**.

Zbývající části tohoto tématu popisují, co můžete dělat na stránce **Jednotky**.

## <a name="create-standard-units-and-conversions"></a>Vytvoření standardních jednotek a převodů

Pokud váš systém již neobsahuje nejčastěji používané měrné jednotky pro metrický systém nebo americký obvyklý systém (USCS), může vám průvodce nastavením jednotek pomoci rychle začít se základními definicemi jednotek a převody. Chcete-li průvodce projít, vyberte **Průvodce vytvořením jednotky** v podokně Akce a poté postupujte podle pokynů na obrazovce.

## <a name="create-or-edit-a-unit-of-measure"></a>Vytvoření nebo úprava měrné jednotky

Chcete-li vytvořit nebo upravit měrnou jednotku, postupujte takto.

1. Proveďte jeden z následujících kroků:

    - Chcete-li upravit existující jednotku, vyberte ji v podokně seznamu.
    - Chcete-li vytvořit novou jednotku, vyberte **Nová** v podokně Akce.

1. V záhlaví záznamu nastavte následující pole:

    - **Jednotka** – Zadejte ID nebo symbol, který se použije k označení jednotky v systémovém jazyce. Toto ID nebo symbol je obvykle běžná zkratka pro jednotku, například *ks* pro kus nebo *cm* pro centimetr.
    - **Popis** – Zadejte popisný název jednotky v systémovém jazyce. Tento název je obvykle celé jméno jednotky, například *Kus* nebo *Centimetr*.

1. Na pevné záložce **Obecné** zadejte následující pole:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Třída jednotek** – Vyberte vlastnost, kterou jednotka měří (například délku, plochu, hmotnost nebo množství).
    - **Systém jednotek** – Vyberte měřný systém, do kterého jednotka patří (*Metrické jednotky* nebo *Americké obvyklé jednotky*).
    - **Základní jednotka** – Nastavte tuto možnost na *Ano*, chcete-li použít aktuální jednotku jako základní jednotku pro svou třídu jednotek. V tomto případě musíte zadat pouze převodní koeficient mezi základní jednotkou a každou další jednotkou ve třídě jednotek. Systém pak může převádět mezi všemi jednotkami v dané třídě jednotek. Proto je snazší nastavit převody.

        Například pokud je galon základní jednotkou pro třídu jednotek *Objem*, musíte nastavit pouze převodní faktory z litrů na galon a z pinty na galon. Systém pak dokáže také převádět z litrů na pintu.

        Pro každou třídu jednotek můžete mít pouze jednu základní jednotku.

    - **Systémová jednotka** – Nastavte tuto možnost na *Ano*, chcete-li použít aktuální jednotku jako předpokládanou jednotku pro všechna nespecifikovaná měření pro svou třídu jednotek. Například pokud pole, které se používá k zadání množství, neumožňuje specifikovat jednotku (pokud uživatel nevybere jednotku), systém použije jednotku, která je nastavena jako systémová jednotka pro třídu jednotek *Množství*. Pro každou třídu jednotek můžete mít pouze jednu systémovou jednotku.
    - **Desetinná přesnost** – Určete počet desetinných míst, na které mají být zaokrouhleny hodnoty zadané pro aktuální jednotku nebo na ně převedené.

1. V podokně akcí vyberte **Uložit**.

## <a name="define-unit-translations"></a>Definování překladů jednotek

Chcete-li definovat překlady pro ID nebo symbol a popis měrné jednotky, postupujte takto.

1. Vytvořte nebo vyberte jednotku, pro kterou chcete vytvořit překlad.
1. V podokně akcí zvolte **Texty jednotky**.

    Zobrazí se stránka **Texty jednotek**. Tato stránka slouží k definování překladů pro ID nebo symbol pro vybranou jednotku. Tyto překlady lze poté použít na externí dokumenty v jazycích specifických pro zákazníka nebo pro dodavatele.

1. V podokně akcí zvolte **Nový**.
1. V poli **Jednotka** vyberte jazyk, do kterého se má ID nebo symbol jednotky přeložit.
1. Do pole **Text** zadejte překlad ID jednotky nebo symbolu do vybraného jazyka.
1. V podokně akcí vyberte **Uložit**.
1. Zavřete stránku.
1. V **podokně akcí** vyberte možnost **Popisy přeložené jednotky**.

    Zobrazí se stránka **Přeložené popisy jednotek**. Tato stránka slouží k definování specifických jazykových popisů pro vybranou jednotku.

1. V podokně akcí zvolte **Nový**.
1. V poli **Jednotka** vyberte jazyk, do kterého se má popis jednotky přeložit.
1. Do pole **Popis** zadejte překlad popisu jednotky do vybraného jazyka.
1. V podokně akcí vyberte **Uložit**.
1. Zavřete stránku.

## <a name="define-unit-conversion-rules"></a>Definování pravidel pro převod jednotek

Chcete-li definovat pravidla pro převody mezi měrnými jednotkami, postupujte takto.

1. Vytvořte nebo vyberte jednotku, pro kterou chcete vytvořit převod.
1. V podokně akcí zvolte **Převody jednotek**.

    Zobrazí se stránka **Převody jednotek**. Tuto stránku můžete použít k definování pravidel pro převod vybrané jednotky jiných jednotek v třídě jednotky a z nich.

1. Vyberte jednu z následujících karet v závislosti na typu převodu, který chcete nastavit:

    - **Standardní převody** – Nastavte standardní pravidla převodu pro všechny produkty.
    - **Konverze uvnitř třídy** – Nastavte pravidla převodu pro konkrétní produkt pro jednotky ve stejné třídě jednotek.
    - **Konverze mezi třídami** – Nastavte pravidla převodu pro konkrétní produkt pro jednotky mezi třídami jednotek.

1. Proveďte jeden z následujících kroků:

    - Chcete-li vytvořit nový převod, vyberte **Nová** na panelu nástrojů.
    - Chcete-li upravit existující převod, vyberte převod v mřížce a poté vyberte **Upravit** na panelu nástrojů.

1. V zobrazeném rozevíracím dialogovém okně nastavte následující pole:

    - **Produkt** – Vyberte konkrétní produkt, kterého se převod týká. Toto pole je k dispozici pouze pro převody v rámci třídy a mezi třídami.
    - **Rozložení vzorce** – Nechte toto pole nastaveno na *Jednoduchý*, chcete-li určit jednoduchou konverzi, která má jediný koeficient. Nastavte ho na *Pokročilý*, chcete-li nastavit složitější rovnici. Formát pokročilých rovnic se liší v závislosti na třídě jednotek.
    - **Z jednotky** – Toto pole zobrazuje vybranou jednotku. Obvykle byste neměli měnit hodnotu. (Pokud změníte hodnotu, musíte otevřít stránku **Převody jednotek** pro vybranou jednotku, aby se po uložení zobrazil nový převod.)
    - **Do jednotky** – Vyberte jednotku, na kterou chcete převést.
    - **Zaokrouhlování** – Vyberte způsob zaokrouhlování zlomků na základě hodnoty **Desetinná přesnost** vybrané jednotky (*Na nejbližší*, *Nahoru*, nebo *Dolů*).
    - **Převodní vzorec** – Pomocí zbývajících polí v horní části rozevíracího dialogového okna zadejte vzorec pro převod mezi těmito dvěma jednotkami. Dostupná pole se liší v závislosti na vybrané třídě jednotek a rozložení vzorců.

1. Vyberte **OK**.
1. Zavřete stránku.

> [!TIP]
> Můžete také nastavit převody jednotek na variantu produktu. Další informace naleznete v tématu [Převod měrné jednotky pro variantu produktu](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
