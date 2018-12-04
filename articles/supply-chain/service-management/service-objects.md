---
title: "Servisní objekty"
description: "Servisní předměty jsou majetek a produkty zákazníka, u kterých je lze provádět servisní úkony."
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: a69fd6a1b07683383d88c7f5c7986529c7bb1875
ms.contentlocale: cs-cz
ms.lasthandoff: 02/21/2018

---

# <a name="service-objects"></a>Servisní objekty 

[!include [banner](../includes/banner.md)]

Servisní předměty jsou majetek a produkty zákazníka, u kterých je lze provádět servisní úkony. V závislosti na typu poskytované služby se může jednat o hmotné či nehmotné předměty:

-  Hmotnými předměty se rozumí věci jako například stroje, zařízení nebo budovy, pro které lze provádět fyzické servisní úkony.

    Hmotným předmětem servisu může být také skladová položka vytvořená ve formuláři Podrobnosti o uvolněném produktu. V závislosti na skupině dimenzí zásob připojené k dané položce můžete vytvořit předmět servisu až na úroveň podrobností zahrnující sériové číslo položky. To je užitečné v případech, kdy je třeba sledovat přesnou položku, kterou předmět servisu reprezentuje.

    Hmotným předmětem servisu však může být také položka, která přímo nesouvisí s produkty dané společnosti ani s řetězcem dodavatelů. Například sada nástrojů používaná pro opravy v rámci servisní zakázky může být předmětem servisu, který není zahrnut v zásobách. V takovém případě ji není nutné zaregistrovat jako skladovou položku.

-  Nehmotnými předměty se rozumí nefyzické objekty, jako je například soubor účtů nebo právní dokument, u kterého lze provádět servisní úkony.

## <a name="example-of-an-intangible-service-object"></a>Příklady nehmotných předmětů služby

Společnost A spravuje finanční záznamy několika malých společností. Jedním z klientů společnosti A je místní fotbalový klub, pro který tato společnost A provádí týdenní úkony účetnictví a také výroční audit klubových účtů. Účty klubu jsou konfigurovány ve formuláři Předměty servisu a v servisní smlouvě jsou uvedeny jako předmět servisu. U objektu existují dva řádky servisní smlouvy. Řádek 1 obsahuje úkony účetnictví v týdenním intervalu, které jsou přiřazeny k řádku, a řádek 2 obsahuje výroční audit, ke kterému je přidělen roční rozsah.

## <a name="related-topics"></a>Související témata

[Tvorba předmětů servisu](create-service-objects.md)


