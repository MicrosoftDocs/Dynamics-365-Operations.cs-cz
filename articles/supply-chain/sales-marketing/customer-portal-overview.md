---
title: Přehled zákaznického portálu pro Dynamics 365 Supply Chain Management (obsahuje video)
description: Tento článek představuje zákaznický portál a vysvětluje, kdo by ho měl používat a jak to funguje.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7f34acd78966cc9f26242653e9d0d16fdf22e0b2
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103823"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Přehled zákaznického portálu pro Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>Co je zákaznický portál?

Moderní systémy dodavatelského řetězce spoléhají na integraci. Vyžadují, aby místo oddělení v samostatných silách byly integrovány zásoby, poptávka zákazníků a prodejní oddělení. Zákaznický portál pomáhá organizacím, které provozují Microsoft Dynamics 365 Supply Chain Management, zlepšit tuto integraci a efektivněji informovat své zákazníky.

Zákaznický portál je šablona [portálů Power Apps](/powerapps/maker/portals/overview), která umožňuje společnostem vytvořit externě orientovaný web business-to-business (B2B) pro scénáře související se zpracováním prodejních objednávek. Šablona používá [dvojí zápis](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md), Supply Chain Management a portály Power Apps umožňující externím podnikovým zákazníkům prohlížet a vytvářet data z prostředí společnosti Dynamics 365.

Šablona zákaznického portálu má všechny možnosti přizpůsobení, které funkce portálů Power Apps nabízí. Šablonu lze snadno upravit tak, aby představovala značku společnosti, přidala zvýšenou funkčnost a změnila uživatelské prostředí. Veškeré funkce, které šablona nabízí, mohou být podle potřeby upraveny.

> [!IMPORTANT]
> U samotné šablona se neočekává, že bude zcela funkční. Slouží pouze jako aktivační prostředek pro zákazníky, kteří chtějí vytvořit externě orientovaný web, aby se firemní zákazníci mohli zapojit do dat ze Supply Chain Management.

> [!NOTE]
> Dokumentace zákaznického portálu je určena administrátorům, přizpůsobitelům a systémovým integrátorům, kteří nastaví zákaznický portál pro instalaci Supply Chain Management. Používá výrazy _zákazník_ a _uživatel_, avy popsal lidi, kteří jsou zákazníky organizace provozující Supply Chain Management a kteří budou používat samotný finální portál.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Video [Přehled šablony zákaznického portálu v Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (viz výše) je součástí [seznamu skladeb financí a provozu](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) k dispozici na YouTube.

## <a name="who-should-use-it"></a>Kdo by to měl použít?

Zákaznický portál je určen pro společnosti, které provozují Supply Chain Management a mají tyto vlastnosti:

- Chtějí vytvořit externě orientovaný web, který komunikuje informace o zpracování objednávek (jako je stav objednávky nebo informace o účtu) přímo z jejich systému Supply Chain Management svým podnikovým zákazníkům.
- Přecházejí z Dynamics AX 2012 na Supply Chain Management a dříve používali [Samoobslužný portál zákazníka AX 2012](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Následující typy organizací **nejsou** dobrými kandidáty na implementaci zákaznického portálu:

- Společnosti, které chtějí vytvořit web pro nepodnikající zákazníky. Tyto společnosti by měly zvážit vytvoření [webu elektronického obchodu Dynamics 365 Commerce](../../commerce/create-ecommerce-site.md).
- Společnosti, které již používají stávající web portálů Power Apps za podobným účelem. Tyto společnosti nezískají žádné další výhody ze zákaznického portálu. Zákaznický portál je dodáván jako šablona, která slouží jako vodítko a výchozí bod pro zákazníky, kteří chtějí propojit dvojí zápis, Supply Chain Management a portály Power Apps. Pokud jste již nastavili web, který slouží tomuto účelu, pravděpodobně nebudete mít z využití šablony zákaznického portálu příliš velkou hodnotu pro opětovné poskytnutí tohoto webu.

## <a name="how-does-it-work"></a>Jak to funguje?

Zákaznický portál je poskytován jako šablona portálů Power Apps. Závisí na portálech Power Apps a dvojím zápisu.

[Portály Power Apps](/powerapps/maker/portals/overview) je funkce, která umožňuje uživatelům vytvořit web navenek orientovaný, ke kterému se mohou přihlásit lidé mimo organizaci. Pro výrobu portálů je zapotřebí jen málo kódů. Zákaznický portál je jedním z mnoha [Šablon portálu Dynamics 365](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), které jsou k dispozici od společnosti Microsoft.

[Dvojí zapisování](/powerapps/maker/portals/overview) je předpřipravený produkt infrastruktury poskytující prakticky v reálném čase mezi aplikacemi pro zapojení zákazníků a finančními a provozními aplikacemi. Dvojí zapisování poskytuje obousměrnou integraci mezi finančními a provozními aplikacemi a Microsoft Dataverse. Proto poskytuje integrované uživatelské prostředí pro celé aplikace. Zákaznický portál závisí na tabulkách, které jsou synchronizovány s duálním zápisem. Předtím, než se na zákaznickém portálu mohou objevit data z Supply Chain Management, musí být pro všechny příslušné tabulky povoleny duální zápisy.

![Závislosti zákaznického portálu.](media/customer-portal-elements.png "Závislosti zákaznického portálu")

Zákaznický portál slouží jako výchozí bod pro organizace, které chtějí používat portály Power Apps k vytvoření externě orientovaného webu, který používá data z instalace Supply Chain Management. Pomáhá organizacím propojit dvojí zápis, Supply Chain Management a portály Power Apps.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
