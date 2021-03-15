---
title: Nalezení informací pomocí vyhledávání
description: Mnoho polí má vyhledávací pole umožňující snadné vyhledávání správných a požadovaných hodnot. Vyhledávání bylo několika způsoby vylepšeno – ovládací prvky jsou nyní užitečnější a uživatelé díky nim mohou být produktivnější. V tomto tématu se dozvíte o těchto nových funkcích a užitečných tipech k optimálnímu využití vyhledávání v systému.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75e66e8fb9f1a227c9dd15f92ca5db433c0db4a
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798135"
---
# <a name="find-information-by-using-lookups"></a>Nalezení informací pomocí vyhledávání

[!include [banner](../includes/banner.md)]

Mnoho polí má vyhledávací pole umožňující snadné vyhledávání správných a požadovaných hodnot. Vyhledávání bylo několika způsoby vylepšeno – ovládací prvky jsou nyní užitečnější a uživatelé díky nim mohou být produktivnější. V tomto tématu se dozvíte o těchto nových funkcích a užitečných tipech k optimálnímu využití vyhledávání v systému.

## <a name="responsive-lookups"></a>Lépe reagující vyhledávání

V předchozích verzích museli uživatelé při práci s ovládacími prvky vyhledávání provádět explicitní úkony, aby se otevřela rozevírací nabídka. K těmto úkonům patří zadání hvězdičky (\*) k filtrování podle aktuální hodnoty ovládacího prvku, kliknutí na tlačítko rozevíracího seznamu nebo použití klávesové zkratky **Alt**+**Šipka dolů**. Ovládací prvky vyhledávání byly upraveny následujícími způsoby, aby lépe vyhovovaly současné praxi při používání webu:

- Rozevírací nabídky vyhledávání se nyní automaticky otevírají po krátké pauze při zadávání a jejich obsah se filtruje podle aktuální hodnoty vyhledávacího ovládacího prvku.

    Původní chování – automatické otevření rozevíracího seznamu po zadání hvězdičky (\*) – se již nepoužívá.

- Po otevření rozevírací nabídky vyhledávání se stane toto:

    - Kurzor zůstane ve vyhledávacím ovládacím prvku (místo přesunutí do rozevírací nabídky), abyste mohli hodnotu ovládacího prvku dále upravovat. Uživatel však stále může pomocí kláves **Šipka nahoru** a **Šipka dolů** měnit řádky v rozevírací nabídce a vybírat aktuální řádky klávesou Enter.
    - Obsah rozevírací nabídky bude reagovat na jakoukoli změnu hodnoty vyhledávacího ovládacího prvku.

Jak příklad si uveďme vyhledávací pole s názvem **Město**.

Pokud je výběr nastaven na pole **Město**, můžete začít hledat požadované město zadáním několika písmen, například „col“. Jakmile přestanete psát, vyhledávání se automaticky otevře a zobrazí města začínající na „col“.

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

V tomto okamžiku je kurzor stále ve vyhledávacím poli. Pokud budete pokračovat v psaní a zadáte hodnotu „colum“, obsahu vyhledávání se tomuto zadání automaticky přizpůsobí.

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

I když je stále vybrán vyhledávací ovládací prvek, můžete pomocí kláves **Šipka nahoru** a **Šipka dolů** vybírat požadované řádky. Pokud stisknete klávesu **Enter**, zvýrazněný řádek se ve vyhledávání vybere a hodnota ovládacího prvku se aktualizuje.

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Zadání dalších údajů kromě ID

Při zadávání dat se uživatelé přirozeně snaží určit entity (například odběratele nebo dodavatele) pomocí názvu, nikoli identifikátorů, které tyto entity zastupují. Existuje mnoho (ale ne všechna) vyhledání, které umožňuje kontextovou zadávání dat. Díky této užitečné funkci může uživatel vyhledávat pomocí ID nebo odpovídajícího názvu.

Příkladem je pole **Účet odběratele** při vytváření prodejní objednávky. V tomto poli se zobrazuje **ID účtu** odběratele, ale uživatelé při tvorbě prodejních objednávek zadávají spíše **název účtu** než **ID účtu**, například „Forest Wholesales“ místo „US-003“.

Pokud uživatel začne do vyhledávacího ovládacího prvku zadávat **ID účtu**, rozevírací nabídka se automaticky otevře (podle popisu v předchozí části) a vyhledávání se zobrazí jako níže.

[![Kontextové vyhledávání při zadání ID účtu odběratele](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Uživatel však může zadat také začátek **názvu účtu**. Pokud to udělá, zobrazí se následující vyhledávání. Všimněte si, že sloupec **Název** se ve vyhledávání přesunul na první místo a že celé vyhledávání je seřazeno a filtrováno podle sloupce **Název**.

[![Kontextové vyhledávání při zadání jména odběratele](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Rozšířené filtrování a řazení pomocí záhlaví sloupců mřížky

Vylepšení vyhledávání popsaná v předchozích dvou částech značně zlepšují možnosti procházení řádků při vyhledávání typu „začíná na“, které se týká polí **ID** nebo **Název**. Existují však situace, ve kterých je k nalezení správného řádku nutné použít pokročilejší filtrování nebo řazení. V těchto případech musí uživatel použít možnosti filtrování a řazení v záhlavích sloupců mřížky vyhledávání. Jako příklad si uvedeme zaměstnance, který zadává řádek prodejní objednávky a potřebuje jako produkt najít správnou položku typu „cable“ (kabel). Pokud do pole **Číslo položky** zadá „cable“, správnou položku nenajde, protože žádné názvy produktů začínající na „cable“ neexistují.

![emptyitemlookup](./media/emptyitemlookup.png)

Místo toho je třeba hodnotu ovládacího prvku vyhledávání vymazat, otevřít rozevírací nabídku vyhledávání a filtrovat ji pomocí záhlaví sloupce mřížky, jak je uvedeno níže. Možnosti filtrování a řazení lze zobrazit jednoduchým kliknutím (nebo klepnutím) na požadované záhlaví sloupce. Na klávesnici stačí stisknout podruhé zkratku **Alt**+**Šipka** **dolů** a přesunout tak výběr do rozevírací nabídky. Potom lze pomocí tabulátoru vybrat správný sloupec a stisknutím klávesové zkratky **Ctrl**+**G** otevřít rozevírací nabídku záhlaví sloupce mřížky.

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Po použití filtru (viz následující obrázek) může uživatel najít a vybrat řádek jako obvykle.

![filtereditemlookup](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]