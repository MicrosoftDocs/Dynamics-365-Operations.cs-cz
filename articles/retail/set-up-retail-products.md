---
title: "Nastavení maloobchodních produktů"
description: "Tento článek popisuje způsob nastavení maloobchodních produktů v aplikaci Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0906d83ea00edcbd4c04a1f21cc0911828286607
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-retail-products"></a>Nastavení maloobchodních produktů

[!include [banner](includes/banner.md)]

Tento článek popisuje způsob nastavení maloobchodních produktů v aplikaci Microsoft Dynamics 365 for Retail.

Než bude možné nabídnout produkty k prodeji ve vaší maloobchodní síti, je nutné vytvořit a nastavit produkty v aplikaci Dynamics 365 for Retail. Maloobchodní prodej používá k vytvoření celoorganizačních produktů v základním produktu funkce aplikace Microsoft Dynamics 365 for Retail. Pokud chcete vytvořit produkty, definujte vlastnosti produktu a atributy a přiřaďte produkty k hierarchiím kategorií maloobchodu. Pokud chcete zpřístupnit produkty pro vaše maloobchodní kanály a přidat je do aktivního sortimentu, musíte uvolnit produkty pro právnické osoby, kde jsou k dispozici. K nastavení výrobků, které prodáváte pomocí maloobchodní sítě, proveďte následující úkoly.

1.  Definujte hierarchii maloobchodních produktů. Pomocí funkcí hierarchie kategorií v aplikaci Dynamics 365 for Retail můžete definovat hierarchie maloobchodních kategorií pro seskupení a zařazení produktů, které distribuujete mezi maloobchodní kanály. Uživatelské a systémové atributy lze definovat na úrovni kategorie. Poté všechny produkty, které jsou přiřazeny ke kategorii, zdědí tyto atributy. Lze definovat více hierarchií kategorií, a každý výrobek může být přiřazen do více hierarchií. Avšak v jediné hierarchii lze každý výrobek přiřadit pouze k jedné kategorii.
2.  Přidejte produkty a jejich varianty do základního produktu. Produkty, které jsou přidány do základního produktu, představují globální seznam produktů. Produkty lze přidávat ručně, postupně, nebo lze importovat data produktu od vašich dodavatelů.
3.  Uvolněte produkty pro právnické osoby. Pouze produkty, které byly uvolněny pro právnické osoby, mohou být přidány do maloobchodních sítí. Při prvním definování produktu je nutné definovat jej na úrovni celé organizace. Můžete vybrat jednu nebo více právnických osob pro uvolnění produktu. Produkt pak bude k dispozici pro více maloobchodních sítí v rámci organizace. Tato funkce slouží k jednorázovému vytvoření produktu, přidání a aktualizaci atributů produktu a vlastností na jednom místě, a poté jejich distribuování z vaší organizace do maloobchodních sítí, které je tato možnost k dispozici.
4.  Přidejte produkty do sortimentu. Sortiment představuje kolekci produktů, které nabízíte ve vašich maloobchodních kanálech. Můžete definovat jeden nebo více sortimentů, a každý produkt může být přiřazen do jednoho nebo více sortimentů. Pokud chcete přiřadit produkty do maloobchodní sítě, přiřaďte sortimenty do těchto maloobchodních kanálů. Při vytváření sortimentu můžete přidat produkty, které ještě nebyly uvolněny pro právnickou osobu. Nicméně dokud produkty nebudou uvolněny pro právnické osoby, nemohou být přidány do maloobchodních sítí.
5.  Přidejte produkty do hierarchií navigací. Než bude možné výrobky procházet online nebo na pokladním místě, musí být rozděleny v hierarchii maloobchodní navigace.
6.  Přidejte produkty do katalogu. I když je tento krok volitelný pro pokladní místo, online obchody vyžadují, aby byly produkty zahrnuty v alespoň jednom katalogu.





