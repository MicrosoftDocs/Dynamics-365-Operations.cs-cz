---
title: Použití externích katalogů pro funkci PunchOut eProcurement
description: Toto téma vysvětluje, jak lze použít externí katalogy k vytvoření a odeslání požadavků.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c45f89bd8115fe614aed557b760983fd95a87615
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226044"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Použití externích katalogů pro funkci PunchOut eProcurement

[!include [banner](../includes/banner.md)]

Díky externím katalogům elektronického nákupu PunchOut nemusíte spravovat informace o produktech svých dodavatelů ve svých hlavních datech. Místo toho je nákupní košík na webu dodavatele převeden na řádky požadavku, které mají správné informace o produktu. 

Měli byste se vyhnout udržování popisů a cen produktů svých dodavatelů v hlavních datech svých produktů. Místo toho použijte externí katalogy pro funkci PunchOut eProcurement Když potom zaměstnanci vytvářejí žádanky, mohou „proniknout“ na web externího katalogu dodavatele (jinými slovy - odejdou z vašeho systému a přejdou na web dodavatele). Produkty, které jsou přidány do nákupního košíku na webu dodavatele, lze poté převést na řádky požadavků. Proto získáte správné informace o produktu správné: ID produktu, název, cena a podobně.

Aby bylo možné použít externí katalogy, zaměstnanec musí vytvořit požadavek na stránce **Moje nákupní žádanky**.

Zaměstnanec, který vytvoří žádanku, se označuje jako pořizovatel žádanky. Jako pořizovatel můžete provést následující úlohy:

Můžete použít akci na řádku **Externí katalogy** k otevření stránky, která zahrnuje všechny externí katalogy, které jsou k dispozici pro zadaného žadatele, kupující právnickou osobu a přijímající provozní jednotku.

V závislosti na svých oprávněních změňte žadatele, kupující právnickou osobu a přijímající provozní jednotku. Změna těchto hodnot může změnit seznam externích katalogů, které jsou k dispozici žadateli. Externí katalogy, které jsou k dispozici, závisí na aktuálních aktivních zásadách nákupu pro kupující právnickou osobu nebo přijímající provozní jednotku. Tyto zásady mohou povolit nebo zakázat přístup k určité kategorii zásobování. Z tohoto důvodu může být ovlivněn seznam externích katalogů, které jsou mapovány na tyto kategorie zásobování.

Další informace o způsobech nastavení zásad naleznete v tématu [Přehled zásad nákupu](../procurement/purchase-policies.md).

- Pokud chcete vyhledat externí katalogy pro konkrétní kategorie zásobování, zadejte text v poli pro vyhledávání katalogu.
- Pokud chcete přidat produkty z externího katalogu dodavatele na web dodavatele, klikněte na externí katalog. Poté přidejte produkty do nákupního košíku a přejděte k pokladně. Řádky nákupního košíku se přesunou do aplikace Microsoft Dynamics 365.

Pokud existuje několik možností pro kategorie nákupu, vyberte kategorii nákupu před přidáním řádků do žádanky.
Po přidání řádků do žádanky můžete přidat další řádky bez použití externích katalogů. Případně můžete dále pokračovat v používání externích katalogů k přidávání řádků.

Jakmile je žádanka připravena, použijte akci **Workflow** > **Odeslat** pro předložení ke schválení.

### <a name="additional-resources"></a>Další prostředky

- [Nastavení externího katalogu pro funkci PunchOut eProcurement](set-up-external-catalog-for-punchout.md)
- [cXML vylepšení nákupu](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]