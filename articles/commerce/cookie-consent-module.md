---
title: Modul souhlasu se soubory cookie
description: Tohle téma se zabývá moduly souhlasu se soubory cookie a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817275"
---
# <a name="cookie-consent-module"></a>Modul souhlasu se soubory cookie

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly souhlasu se soubory cookie a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul souhlasu se soubory cookie vyzve uživatele webu, aby výslovně poskytli souhlas s povolením souborů cookie pro veškeré funkce nebo moduly, které sledují soubory cookie prohlížeče. Souhlas je vyžadován při prvním procházení webu uživatelem v nové relaci prohlížeče. Po obdržení souhlasu je soubor cookie sledován a uživatel webu již není žádán o souhlas. Další informace viz [Zásady zacházení se soubory cookie](cookie-compliance.md).

Pokud není obdržen souhlas uživatele se soubory cookie na webu, nebudou se na stránce vykreslovat žádné funkce nebo moduly, které vyžadují souhlas se soubory cookie. Například modul pokladny, modul sdílení na sociálních sítích a preferovaná funkce obchodu vyžadují souhlas se soubory cookie a nebudou zobrazeny, pokud nebude přijat souhlas uživatele webu. 

Modul souhlasu se soubory cookie lze nakonfigurovat ve fragmentu záhlaví stránky, takže jej lze vynutit při načtení stránky. Modul souhlasu se soubory cookie by měl obsahovat jasnou zprávu informující uživatele webu o používání souborů cookie na webu a měl by poskytovat odkaz na stránku ochrany osobních údajů webu.

Následující obrázek znázorňuje příklad zprávy o souhlasu se soubory cookie s odkazem na stránku zásad ochrany osobních údajů webu zobrazeným v záhlaví stránky webu.
![Příklad modulu souhlasu se soubory cookie](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Vlastnosti modulu souhlasu se soubory cookie

| Název vlastnosti             | Hodnota                 | popis |
|---------------------------|-----------------------|-------------|
| Formátovaný text                  | Formátovaný text | Zde lze zadat oznámení ve formátu RTF zobrazené uživatelům webu, že web používá soubory cookie prohlížeče a že uživatelé by měli přijmout použití souborů cookie, aby byl web plně funkční. |
| Odkazy | Adresa URL | Na stránku ochrany osobních údajů webu, která popisuje typy souborů cookie, které jsou na webu sledovány, lze přidat jeden nebo více odkazů. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Přidání modul souhlasu se soubory cookie na stránky webu

Aby bylo možné efektivně přidat modul souhlasu se soubory cookie na více stránek webu, lze jej přidat do sdíleného fragmentu záhlaví stránky. Po přidání fragmentu záhlaví na všechny stránky webu se oznámení o souhlasu se soubory cookie automaticky vykreslí při první návštěvě libovolné stránky webu.

Další informace o fragmentech záhlaví a modulech viz [Modul záhlaví](author-header-module.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul záhlaví](author-header-module.md) 

[Zásady zacházení se soubory cookie](cookie-compliance.md)
