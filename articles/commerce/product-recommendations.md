---
title: Přehled doporučení produktu
description: V tomto tématu jsou obecné informace o doporučování produktů. Doporučení produktů umožňují zákazníkům snadno a rychle vyhledat produkty, které chtějí, a také produkty, které původně nechtěly nakupovat.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024972"
---
# <a name="product-recommendations-overview"></a>Přehled doporučení produktu

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce lze použít k zobrazení doporučení produktů na webu e-Commerce a v zařízení pro prodej na místě (POS). Doporučení produktu jsou položky, o které se může zákazník zajímat. Doporučení jsou založena na trendech nákupu ostatních zákazníků v online i kamených obchodech.

Doporučení produktů umožňují zákazníkům snadno a rychle najít produkty, které chtějí, a u toho mají pozitivní zkušenosti. Křížový prodej a návazný prodej může dokonce zákazníkům pomoci najít další produkty, než které původně nakupují. Pokud se při zjišťování produktů používají doporučení, mohou vytvářet více možností převodu, pomoci zvýšit výnosy z prodeje a dokonce také zvýšit spokojenost a uchování zákazníků.

V aplikaci Commerce doporučení produktů využívají technologie strojového učení Microsoft Recommendations ve velkém měřítku.


## <a name="scenarios"></a>Scénáře

Doporučení produktu jsou dostupná pro následující scénáře:

- **Na libovolné stránce obchodu pro procházení nebo cílovou stránku v e-Commerce:** Pokud zákazníci nebo pracovníci obchodu navštíví stránku obchodu, může modul doporučení navrhovat produkty v seznamech **Nový**, **Nejprodávanější**a **Trendující**.
- **Na stránce Podrobnosti produktu:** Pokud zákaznící nebo pracovníci obchodu navštíví stránku **Podrobnosti produktu**, nabídne modul doporučení další položky, které se také mohou nakoupit. Tyto položky se zobrazí v seznamu **Lidem se také líbí**.
- **Na stránce transakce nebo na stránce s pokladnou:** modul doporučení navrhuje položky na základě celého seznamu položek v nákupním košíku. Tyto položky se zobrazí v seznamu **Často zakoupené společně**.
- **Přizpůsobená doporučení:** Maloobchodníci mohou poskytnout přihlášeným zákazníkům seznam **přizpůsobených možností** a také nové funkce, které umožňují, aby byly existující scénáře seznamu přizpůsobeny na základě tohoto odběratele. Další informace naleznete v dokumentaci k funkcím: [povolení přizpůsobených doporučení.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Služba doporučení

Doporučení produktu používají technologie strojového učení Recommendations následujícím způsobem:

- Data ve formátu vyžadovaném službami Recommendation jsou extrahována z pracovní databáze Commerce a odeslána do úložiště entit.
- Služba doporučení používá data k trénování modelů doporučení pro seznamy **Lidem se také líbí**, **Často zakoupené společně**, **Nový**, **Nejprodávanější** a **Trendující**.

## <a name="additional-resources"></a>Další zdroje

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Přehled modulu kolekce produktů](product-collection-module-overview.md)

[Vytvoření seznamů doporučení vybraných produktů](create-editorial-recommendation-lists.md)

[Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md)

[Přidání seznamů doporučení produktu na stránky](add-reco-list-to-page.md)
