---
title: "Přehled online obchodu"
description: "Tento článek obsahuje informace o online obchodech a jejich nastavení v aplikaci Microsoft Dynamics 365 for Retail."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3814e5a4a88f439c89981f191e8896afb2ced68b
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="online-store-overview"></a>Přehled online obchodu

[!INCLUDE [banner](includes/banner.md)]

Tento článek obsahuje informace o online obchodech a jejich nastavení v aplikaci Microsoft Dynamics 365 for Retail.

Maloobchodní prodej v aplikaci Dynamics 365 for Retail podporuje více maloobchodních kanálů. Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody). Online obchody nabízí maloobchodnímu prodejci možnost být online, aby zákazníci mohli zakoupit produkty prodejce online i v maloobchodě. Pokud zákazníci zakoupí produkty z online obchodu, mohou tyto produkty nechat zaslat nebo si je vyzvednout v místním maloobchodě. Online obchod lze vytvořit v rámci klienta Dynamics 365 for Retail. Tento online obchod je pak publikován v online obchodě třetí strany, která je integrována v aplikaci Dynamics 365 for Retail. Online obchod třetí strany slouží jako výkladní skříň (uživatelské rozhraní) pro online obchod, a poskytuje nabídku ze systémů pro správu odběratele a možností uživatelského rozhraní. Několik integrace tohoto typu je k dispozici pro aplikaci Dynamics 365 for Retail. Vlastnosti, které definujete pro online obchod řídí chování online obchodu. Například můžete definovat hierarchii navigační kategorie v rámci aplikace Dynamics 365 for Retail a přiřadit ji k online obchodu. Při publikování online obchodu do online obchodu třetí strany se v online verzi obchodu zobrazí hierarchie navigační kategorie. Zákazníci používají hierarchii navigační kategorie pro procházení online obchodu a hledání produktů. Pokud chcete vytvořit online obchod, nastavte součásti, které umožňují zpracování transakcí pro obchod. Například musíte přidat sortimenty, použít atributy a nastavit platební metody a způsoby dodání. Můžete také definovat ceny, promoakce, slevy, obchodní smlouvy a dodací podmínky, které jsou specifické pro online obchod. Po publikování online obchodu do online obchodu třetí strany můžete vytvořit prodejní katalogy produktů pro online obchod. Produkty v katalogu se stanou výpisem produktů v online obchodu. Poté, co zákazník zakoupí produkty v online obchodě, dojde k aktualizaci a synchronizaci zásob v rámci klienta. Dále se vygenerují prodejní objednávky pro nákupy a odešlou se do klienta pro potřeby splnění objednávky a zpracování.

## <a name="set-up-an-online-store"></a>Nastavení obchodu online
K nastavení online obchodu je třeba dokončit následující úlohy.

1.  Vytvořte online obchod.
2.  Přidejte online obchod do příslušné organizační hierarchie.
3.  Přidejte sortiment s dostupnými produkty v online obchodu.
4.  Přiřaďte nebo vytvořte cenové skupiny pro online obchod.
5.  Nastavte dostupné způsoby dodání do online obchodu.
6.  Přiřaďte metody platby, které byly přijaty pro online obchod.
7.  Jestliže povolíte zákazníkům objednávat produkty online, a následný výdej v místním obchodě, přiřaďte k online obchodu skupiny lokátoru obchodu.
8.  Přiřaďte atributy pro kanály, produkty a prodejní objednávky k online obchodu. Atributy kanálu platí pro celý online obchod, atributy produktů pro produkty, které jsou k dispozici v online obchodu, a atributy prodejní objednávky pro prodejní objednávky, které jsou generovány z online obchodu.
9.  Namapujte atributy k sadě vlastností, které určují chování atributů v online obchodě. Můžete například nastavit atributy tak, aby byly požadovány, nebo aby je bylo možné dohledat.
10. Publikujte online obchod a vygenerujte tak strukturu úložiště pro online obchod třetí strany dle vašeho výběru. **Důležité:** Před publikováním online obchodu musíte pro něj nastavit distribuční místo.

## <a name="retail-channel-navigation-hierarchies"></a>Hierarchie navigací maloobchodní sítě
Před vytvořením online obchodu musíte definovat navigační hierarchii maloobchodního kanálu, kterou chcete použít v něm. Navigační hierarchie maloobchodního kanálu představuje hierarchii kategorií, která se zobrazí v online obchodu po publikování obchodu. Při publikování katalogu maloobchodních produktů v online obchodu se produkty v katalogu namapují v navigační hierarchii maloobchodní sítě. Hierarchii poté používají nakupující pro navigaci v online obchodu.

## <a name="organization-hierarchies"></a>Organizační hierarchie
Hierarchie organizace se používá pro strukturování maloobchodních kanálů. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik. Při nastavování online obchodů je můžete přidat do organizační hierarchie. Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování. Při vytváření organizační hierarchie je nutné přiřadit účel k hierarchii. Účel označuje použití hierarchie v organizační struktuře. Můžete vytvořit jednu organizační hierarchii pro operace obchodu a použít danou hierarchii pro sortimenty, doplnění a vykazování. Alternativně můžete vytvořit samostatnou organizační hierarchii pro každý účel. Také můžete vytvořit více hierarchií se stejným účelem a přiřadit ke každé z nich kanál. Chcete-li publikovat katalogy maloobchodních produktů v online obchodu, je nutné přinejmenším přidat online obchody do organizační hierarchie pro potřeby vytvoření sortimentů. Produkty v katalogu jsou vybrány ze sortimentu přiřazeného k online obchodu. Při publikování katalogu se během procesu publikování porovnávají data platnosti sortimentu přiřazeného k online obchodu s produkty zahrnutými v katalogu, a určují se tak produkty, které budou k dispozici v online obchodu.




