---
title: Hierarchie Commerce
description: Tento článek popisuje hierarchie v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.industry: Retail
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
ms.openlocfilehash: ce196acc8c4bced865b983b12d72f8bc6e4d02a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271870"
---
# <a name="commerce-hierarchies"></a>Hierarchie Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje hierarchie v aplikaci Dynamics 365 Commerce.

Můžete vytvořit hierarchii kategorií a uspořádat produkty, které prodáváte prostřednictvím prodejních kanálů. Hierarchie produktů můžete použít k uspořádání produktů do kategorií nebo k jejich seskupení. Potom můžete tyto produkty použít k vytvoření sortimentu produktů a věrnostních programů pro odběratele. Lze také přiřadit atributy a vlastnosti produktu, přiřadit cenové struktury, zahrnout produkty do promoakcí produktů a použít produkty k vykazování. Můžete vytvořit jednu hierarchii kategorie představující všechny produkty a kategorie v rámci organizace a potom tuto hierarchii kategorií použít pro více účelů. Alternativně můžete vytvořit více hierarchií kategorií pro zvláštní účely, jako je propagace výrobku. Při vytváření hierarchie produktů je nutné přiřadit typ kategorie hierarchie k identifikaci účelu hierarchie kategorií. Například pouze hierarchie produktů, kterým je přiřazen typ **Hierarchie navigace velkoobchodu**, jsou odkazovány při procházení produktů podle kategorie online nebo na pokladním místě (POS).

## <a name="hierarchy-types"></a>Typy hierarchie

V následující tabulce jsou uvedeny dostupné typy hierarchií kategorie a obecný účel každého typu.

| Typ hierarchie kategorií       | Účel |
|-------------------------------|---------|
| Hierarchie výrobků      | Použijte tento typ hierarchie, chcete-li definovat celkovou hierarchii produktů pro organizaci. Tento typ hierarchie lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu. Tento typ hierarchie může být přiřazen pouze jedné hierarchii produktů. |
| Doplňková hierarchie | Použijte tento typ hierarchie pro jakékoli další hierarchie kategorií, které chcete vytvořit. Například na jaře máte promoakci na plavky. Proto zahrnete plavky do samostatnou hierarchie kategorií a použijete propagační cenové kalkulace pro různé kategorie produktu. |
| Hierarchie navigace   | Použijte tento typu hierarchie pro seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v POS. |

Pomocí hierarchie kategorií k vytvoření struktury produktů můžete nastavit a spravovat atributy a vlastnosti produktů na úrovni kategorie. Tyto atributy a vlastnosti zahrnují nastavení pro dimenze produktu a nastavení POS. Všechny produkty, které přiřadíte k těmto kategoriím, automaticky zdědí atributy a vlastnosti, které definujete. Můžete také zkopírovat nastavení vlastností pro jakýkoli produkt do více produktů ve vybrané kategorii současně.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
