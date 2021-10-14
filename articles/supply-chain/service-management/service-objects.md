---
title: Přehled předmětů servisu
description: Toto téma poskytuje přehled práce s předměty servisu.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cf5e146bb7eab4df5807c6a55f773bfb31a4c5e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571370"
---
# <a name="service-objects-overview"></a>Přehled předmětů servisu

[!include [banner](../includes/banner.md)]

Předměty servisu jsou majetek a produkty odběratele, u kterých je možné provádět servisní úkony. V závislosti na typu poskytované služby se může jednat o hmotné či nehmotné předměty:

-  Hmotnými předměty se rozumí věci jako například stroje, zařízení nebo budovy, pro které lze provádět fyzické servisní úkony.

    Hmotným předmětem servisu může být také skladová položka vytvořená ve formuláři Podrobnosti o uvolněném produktu. V závislosti na skupině dimenzí zásob připojené k dané položce můžete vytvořit předmět servisu až na úroveň podrobností zahrnující sériové číslo položky. To je užitečné v případech, kdy je třeba sledovat přesnou položku, kterou předmět servisu reprezentuje.

    Hmotným předmětem servisu však může být také položka, která přímo nesouvisí s produkty dané společnosti ani s řetězcem dodavatelů. Například sada nástrojů používaná pro opravy v rámci servisní zakázky může být předmětem servisu, který není zahrnut v zásobách. V takovém případě ji není nutné zaregistrovat jako skladovou položku.

-  Nehmotnými předměty se rozumí nefyzické objekty, jako je například soubor účtů nebo právní dokument, u kterého lze provádět servisní úkony.

## <a name="example-of-an-intangible-service-object"></a>Příklady nehmotných předmětů služby

Společnost A spravuje finanční záznamy několika malých společností. Jedním z klientů společnosti A je místní fotbalový klub, pro který tato společnost A provádí týdenní úkony účetnictví a také výroční audit klubových účtů. Účty klubu jsou konfigurovány ve formuláři Předměty servisu a v servisní smlouvě jsou uvedeny jako předmět servisu. U objektu existují dva řádky servisní smlouvy. Řádek 1 obsahuje úkony účetnictví v týdenním intervalu, které jsou přiřazeny k řádku, a řádek 2 obsahuje výroční audit, ke kterému je přidělen roční rozsah.

## <a name="related-topics"></a>Související témata

[Tvorba předmětů servisu](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]