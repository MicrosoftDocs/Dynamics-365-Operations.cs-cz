---
title: Nastavení maloobchodních produktů
description: Tento článek popisuje nastavení produktů v Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2c5a8976973203a943a2cec7658a2998c54f279
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410860"
---
# <a name="set-up-retail-products"></a>Nastavení maloobchodních produktů

[!include [banner](includes/banner.md)]

Tento článek popisuje nastavení produktů v Dynamics 365 Commerce.

Než bude možné nabídnout produkty k přeprodeji ve vašich obchodních kanálech, budete muset vytvořit a nastavit produkty v modulu Retail. Aplikace Commerce vytváří produkty pro celou organizaci v základním produktu. Pokud chcete vytvořit produkty, definujte vlastnosti produktu a atributy a přiřaďte produkty k hierarchiím kategorií velkoobchodu. Pokud chcete zpřístupnit produkty pro vaše velkoobchodní kanály a přidat je do aktivního sortimentu, musíte produkty uvolnit pro právnické osoby, kde jsou k dispozici. K nastavení výrobků, které prodáváte pomocí velkoobchodní sítě, proveďte následující úkoly.

1. **Definujte hierarchii produktů.** Pomocí funkcí hierarchie kategorií v aplikaci Commerce můžete definovat hierarchie maloobchodních kategorií pro seskupení a zařazení produktů, které distribuujete mezi maloobchodní kanály. Uživatelské a systémové atributy lze definovat na úrovni kategorie. Poté všechny produkty, které jsou přiřazeny ke kategorii, zdědí tyto atributy. Lze definovat více hierarchií kategorií, a každý výrobek může být přiřazen do více hierarchií. Avšak v jediné hierarchii lze každý výrobek přiřadit pouze k jedné kategorii.
2. **Přidejte produkty a jejich varianty do základního produktu.** Produkty, které jsou přidány do základního produktu, představují globální seznam produktů. Produkty lze přidávat ručně, postupně, nebo lze importovat data produktu od vašich dodavatelů.
3. **Uvolněte produkty pro právnické osoby.** Pouze produkty, které byly uvolněny pro právnické osoby, mohou být přidány do vašich kanálů. Při prvním definování produktu je nutné definovat jej na úrovni celé organizace. Můžete vybrat jednu nebo více právnických osob pro uvolnění produktu. Produkt pak bude k dispozici pro více sítí v rámci organizace. Tato funkce slouží k jednorázovému vytvoření produktu, přidání a aktualizaci atributů produktu a vlastností na jednom místě, a poté jejich distribuování z vaší organizace do kanálů, kde je tato možnost k dispozici.
4. **Přidejte produkty do sortimentu.** Sortiment představuje kolekci produktů, které nabízíte ve vašich kanálech. Můžete definovat jeden nebo více sortimentů, a každý produkt může být přiřazen do jednoho nebo více sortimentů. Pokud chcete přiřadit produkty do kanálů, přiřaďte sortimenty do těchto kanálů. Při vytváření sortimentu můžete přidat produkty, které ještě nebyly uvolněny pro právnickou osobu. Nicméně dokud produkty nebudou uvolněny pro právnické osoby, nemohou být přidány do kanálů.
5. **Přidejte produkty do hierarchií navigací.** Než bude možné výrobky procházet online nebo na pokladním místě, musí být rozděleny v hierarchii navigace aplikace Commerce.
6. **Přidejte produkty do katalogu.** I když je tento krok volitelný pro pokladní místo, online obchody vyžadují, aby byly produkty zahrnuty v alespoň jednom katalogu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]