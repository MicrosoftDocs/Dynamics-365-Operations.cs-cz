---
title: Hierarchie maloobchodu
description: Tento článek popisuje hierarchie maloobchodu v aplikaci Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "341895"
---
# <a name="retail-hierarchies"></a>Hierarchie maloobchodu

[!include [banner](includes/banner.md)]

Tento článek popisuje hierarchie maloobchodu v aplikaci Microsoft Dynamics 365 for Retail.

Můžete vytvořit hierarchii kategorií maloobchodu a uspořádat produkty, které prodáváte prostřednictvím prodejních kanálů. Hierarchie maloobchodních produktů můžete použít k uspořádání produktů do kategorií nebo k jejich seskupení. Potom můžete tyto produkty použít k vytvoření sortimentu produktů a věrnostních programů pro odběratele. Lze také přiřadit atributy a vlastnosti produktu, přiřadit cenové struktury, zahrnout produkty do promoakcí produktů a použít produkty k vykazování. Můžete vytvořit jednu hierarchii kategorií maloobchodu představující všechny produkty a kategorie v rámci organizace a potom tuto hierarchii kategorií můžete použít pro více účelů. Alternativně můžete vytvořit více hierarchií kategorií maloobchodu pro zvláštní účely, jako je propagace produktu. Při vytváření hierarchie maloobchodních produktů je nutné přiřadit typ kategorie hierarchie k identifikaci účelu hierarchie kategorií. Například pouze hierarchie produktů, kterým je přiřazen typ **Hierarchie navigace maloobchodu**, jsou odkazovány při procházení produktů podle kategorie online nebo na pokladním místě (POS).

## <a name="retail-hierarchy-types"></a>Typy hierarchie maloobchodu

V následující tabulce jsou uvedeny dostupné typy hierarchií kategorií maloobchodu a obecný účel každého typu.

| Typ hierarchie kategorií       | Účel |
|-------------------------------|---------|
| Hierarchie maloobchodních produktů      | Použijte tento typ hierarchie, chcete-li definovat celkovou hierarchii produktů pro organizaci. Tento typ hierarchie lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu. Tento typ hierarchie může být přiřazen pouze jedné hierarchii maloobchodních produktů. |
| Hierarchie doplňkového maloobchodu | Použijte tento typ hierarchie pro jakékoli další hierarchie kategorií maloobchodu, které chcete vytvořit. Například na jaře máte promoakci na plavky. Proto zahrnete plavky do samostatnou hierarchie kategorií a použijete propagační cenové kalkulace pro různé kategorie produktu. |
| Hierarchie navigace maloobchodu   | Použijte tento typu hierarchie pro seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v POS. |

Pomocí hierarchie kategorií maloobchodu k vytvoření struktury produktů můžete nastavit a spravovat atributy a vlastnosti produktů na úrovni kategorie. Tyto atributy a vlastnosti zahrnují nastavení pro dimenze produktu a nastavení POS. Všechny produkty, které přiřadíte k těmto kategoriím, automaticky zdědí atributy a vlastnosti, které definujete. Můžete také zkopírovat nastavení vlastností pro jakýkoli produkt do více produktů ve vybrané kategorii současně.
