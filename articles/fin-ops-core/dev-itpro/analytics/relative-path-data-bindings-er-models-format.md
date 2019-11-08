---
title: Použití relativní cesty v datových vazbách modelů a formátů elektronického výkaznictví
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a026eec379f98fd32080df50b5e114b423db34ad
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182800"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a>Použití relativní cesty v datových vazbách modelů a formátů elektronického výkaznictví

[!include[banner](../includes/banner.md)]

Nástroj elektronické výkaznictví umožňuje uživatelům definovat struktury elektronického formátu a pak popsat, jak by tyto struktury měly být vyplněny pomocí dat a algoritmů, které existují. Další informace získáte v tématu [Vytvoření konfigurací elektronického výkaznictví](electronic-reporting-configuration.md). Chcete-li určit datový tok pro načítání dat aplikace Finance and Operations a použít jej k vygenerování elektronického dokumentu, je nutné provést následující kroky:

- Navažte nakonfigurované zdroje dat na prvky navrženého datového modelu specifického pro určitou doménu. Struktura modelu a vybrané zdroje dat mohou být součástí komplexní hierarchické struktury. Z tohoto důvodu mohou být konečné vazby poměrně velké a obsahovat mnoho prvků různých typů (například vztahy, tabulky a metody). Vazby mohou být méně čitelné a poměrně složité pro kontrolu a pochopení, zejména pro nevlastníky. 
- Provažte prvky datového modelu s komponentami formátu pro definování toho, jaká data budou naplněna z datového modelu do výstupu generovaného formátu.

Pro zlepšení použitelnosti návrhářů mapování elektronického výkaznictví byla vydána funkce relativní cesty. Ve výchozím nastavení je možnost zobrazení relativní cesty zapnuta pro každou novou instanci aplikace, kde je povoleno rozhraní návrháře elektronického výkaznictví (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service). Implementovali jsme parametr relativní cesty, aby uživatelé mohli používat úplnou cestu při práci s touto prezentací vazeb elektronického výkaznictví.

[![Parametry uživatele](./media/relative-path-01.png)](./media/relative-path-01.png)

 
Je-li zapnut parametr použití relativní cesty, nahradí jeden znak @ cestu k nadřazené položce ve vazbě aktuálního prvku modelu. Celá cesta vazby se stane kratší, takže celé mapování bude přehlednější a bude snazší pochopit. Ve většině případů se v návrháři elektronického výkaznictví nevyžaduje žádné další posouvání, aby se zobrazily všechny vazby datového modelu.

[![Návrhář mapování modelu](./media/relative-path-02.png)](./media/relative-path-02.png)
 
Když začnete navrhovat nový výraz elektronického výkaznictví, je třeba zadat pouze jeden znak, který definuje vazbu k poli nadřazené položky.

[![Návrhář receptur](./media/relative-path-03.png)](./media/relative-path-03.png)
 
Pokud se rozhodnete změnit zdroj dat nadřazené položky modelu s použitím absolutní cesty, je nutné ručně znovu svázat tuto položku modelu a všechny vnořené položky s novým zdrojem dat. Je-li povoleno použití relativní cesty a vyberete nový zdroj dat, který má být svázán s nadřazenou položkou, bude vám nabídnuta možnost automatického obnovení vazby všech vnořených prvků této nadřazené položky jediným kliknutím.

[![Nahrazení existující zprávy cesty](./media/relative-path-04.png)](./media/relative-path-04.png)
 
Pokud potvrdíte opětovnou vazbu vnořených položek, nová nadřazená položka bude umístěna do cesty jednotlivých vnořených položek, které obsahují existující nadřazenou položku.
Tato funkce neruší zpětnou kompatibilitu architektury elektronického výkaznictví. Všechny dříve navržené konfigurace elektronického výkaznictví budou fungovat s touto novou funkcí a nebudou požadovány žádné upgrady ani konverze.

> [!NOTE]
> Všechny změny, které jsou zavedeny hromadnou změnou vazeb vnořených prvků v mapování modelu, jsou správně uloženy v rozdílu konfigurace (sledování změn). To umožňuje zákazníkům znovu založit odvozenou verzi mapování modelů na libovolnou novou základní verzi, která byla upravena pomocí této nové funkce.