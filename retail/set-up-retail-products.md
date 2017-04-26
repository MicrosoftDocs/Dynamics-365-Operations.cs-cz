---
title: "Nastavení maloobchodních produktů"
description: "Tento článek popisuje, jak nastavit maloobchodní produkty v Microsoft Dynamics 365 pro operace - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Nastavení maloobchodních produktů

[!include[banner](includes/banner.md)]


Tento článek popisuje, jak nastavit maloobchodní produkty v Microsoft Dynamics 365 pro operace - Retail.

Nabídnout produkty k prodeji v maloobchodní sítě, vytvořte a konfigurovat produkty v Dynamics 365 pro operace AX - Retail. Maloobchod používá k vytvoření produktů pro celou organizaci ve výrobku hlavního funkce produktu Dynamics 365 pro operace. Pokud chcete vytvořit produkty, definujte vlastnosti produktu a atributy a přiřaďte produkty k hierarchiím kategorií maloobchodu. Pokud chcete zpřístupnit produkty pro vaše maloobchodní kanály a přidat je do aktivního sortimentu, musíte uvolnit produkty pro právnické osoby, kde jsou k dispozici. K nastavení výrobků, které prodáváte pomocí maloobchodní sítě, proveďte následující úkoly.

1.  Definujte hierarchii maloobchodních produktů. Pomocí funkce hierarchie kategorií v Dynamics 365 pro operace můžete definovat maloobchodní kategorie hierarchie skupin a kategorií výrobků, které distribuujete maloobchodní sítě. Uživatelské a systémové atributy lze definovat na úrovni kategorie. Poté všechny produkty, které jsou přiřazeny ke kategorii, zdědí tyto atributy. Lze definovat více hierarchií kategorií, a každý výrobek může být přiřazen do více hierarchií. Avšak v jediné hierarchii lze každý výrobek přiřadit pouze k jedné kategorii.
2.  Přidejte produkty a jejich varianty do základního produktu. Produkty, které jsou přidány do základního produktu, představují globální seznam produktů. Produkty lze přidávat ručně, postupně, nebo lze importovat data produktu od vašich dodavatelů.
3.  Uvolněte produkty pro právnické osoby. Pouze produkty, které byly uvolněny pro právnické osoby, mohou být přidány do maloobchodních sítí. Při prvním definování produktu je nutné definovat jej na úrovni celé organizace. Můžete vybrat jednu nebo více právnických osob pro uvolnění produktu. Produkt pak bude k dispozici pro více maloobchodních sítí v rámci organizace. Tato funkce slouží k jednorázovému vytvoření produktu, přidání a aktualizaci atributů produktu a vlastností na jednom místě, a poté jejich distribuování z vaší organizace do maloobchodních sítí, které je tato možnost k dispozici.
4.  Přidejte produkty do sortimentu. Sortiment představuje kolekci produktů, které nabízíte ve vašich maloobchodních kanálech. Můžete definovat jeden nebo více sortimentů, a každý produkt může být přiřazen do jednoho nebo více sortimentů. Pokud chcete přiřadit produkty do maloobchodní sítě, přiřaďte sortimenty do těchto maloobchodních kanálů. Při vytváření sortimentu můžete přidat produkty, které ještě nebyly uvolněny pro právnickou osobu. Nicméně dokud produkty nebudou uvolněny pro právnické osoby, nemohou být přidány do maloobchodních sítí.
5.  Přidáte produkty do hierarchie navigací. Před produkty mohou procházet online nebo bod 8.2 prodeje (POS), musí být uspořádány v navigační hierarchii maloobchodní.
6.  Přidáte produkty do katalogů. Přestože tento krok je volitelný pro POS, online obchody vyžadují, že alespoň jeden katalog zahrnuty produkty.





