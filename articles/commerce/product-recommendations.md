---
title: Přehled doporučení produktu
description: V tomto tématu jsou obecné informace o doporučování produktů. Doporučení produktů umožňují zákazníkům snadno a rychle vyhledat produkty, které chtějí, a také produkty, které původně nechtěly nakupovat.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664875"
---
# <a name="product-recommendations-overview"></a>Přehled doporučení produktu

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce lze použít k zobrazení doporučení produktů na webu e-Commerce a v zařízení pro prodej na místě (POS). Doporučení produktu jsou položky, o které se může zákazník zajímat. Doporučení jsou založena na trendech nákupu ostatních zákazníků v online i kamených obchodech.

Doporučení produktů umožňují zákazníkům snadno a rychle najít produkty, které chtějí, a u toho mají pozitivní zkušenosti. Křížový prodej a návazný prodej může dokonce zákazníkům pomoci najít další produkty, než které původně nakupují. Pokud se při zjišťování produktů používají doporučení, mohou vytvářet více možností převodu, pomoci zvýšit výnosy z prodeje a dokonce také zvýšit spokojenost a uchování zákazníků.

V platformě e-Commerce doporučení produktů využívají technologie strojového učení Microsoft Recommendations ve velkém měřítku.

## <a name="recommendation-service"></a>Služba doporučení

Služba doporučení produktů používá technologie umělé inteligence a strojového učení (AI-ML) následujícím způsobem:

- Data ve formátu vyžadovaném službami Recommendation jsou extrahována z pracovní databáze Commerce a odeslána do Azure Data Lake Storage nebo úložiště entit.
- Služba doporučení používá tato uložená data k trénování modelů doporučení pro seznamy **Lidem se také líbí**, **Často zakoupené společně**, **Nový**, **Nejprodávanější** a **Trendující**.

## <a name="scenarios"></a>Scénáře

Doporučení produktu jsou dostupná pro následující scénáře:

- **Na libovolné stránce obchodu pro procházení nebo cílovou stránku v e-Commerce:** Pokud zákazníci nebo pracovníci obchodu navštíví stránku obchodu, může modul doporučení navrhovat produkty v seznamech **Nový**, **Nejprodávanější**a **Trendující**.
- **Na stránce Podrobnosti produktu:** Pokud zákaznící nebo pracovníci obchodu navštíví stránku **Podrobnosti produktu**, nabídne modul doporučení další položky, které se také mohou nakoupit. Tyto položky se zobrazí v seznamu **Lidem se také líbí**.
- **Na stránce transakce nebo na stránce s pokladnou:** modul doporučení navrhuje položky na základě celého seznamu položek v nákupním košíku. Tyto položky se zobrazí v seznamu **Často zakoupené společně**.
- **Přizpůsobená doporučení:** Maloobchodníci mohou poskytnout přihlášeným zákazníkům seznam **přizpůsobených možností** a také nové funkce, které umožňují, aby byly existující scénáře seznamu přizpůsobeny na základě tohoto odběratele. Chcete-li zjistit více, přečtěte si téma [Povolení přizpůsobených doporučení](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Typy doporučení produktů

V následující tabulce jsou popsány různé typy automatických doporučení produktů, které jsou k dispozici pro maloobchodní prodejce k implementaci do řešení Dynamics 365 Commerce prostřednictvím [modulu kolekce produktů](product-collection-module-overview.md). Maloobchodníci mohou také zobrazit individuální výsledky pro přihlášeného uživatele, pokud tuto možnost zvolí autor webu.

| Modul kolekce produktů  | Typ | popis |
|----------------------------|------|-------------|
| Nová                        | Algoritmický | Tento modul zobrazuje seznam nejnovějších produktů, které byly nedávno roztříděny do kanálů a katalogů. |
| Nejprodávanější               | Algoritmický | Tento modul zobrazuje seznam produktů, které jsou seřazeny podle nejvyššího počtu prodejů. |
| Trendy                   | Algoritmický | Tento modul zobrazuje seznam nejprodávanějších produktů za dané období seřazených podle nejvyššího počtu prodejů.  |
| Často nakupované společně | AI-ML | Tento modul doporučuje seznam produktů, které jsou běžně kupovány dohromady, spolu s obsahem aktuálního vozíku spotřebitele. |
| Lidem se též líbí           | AI-ML | Tento modul doporučuje produkty pro daný produkt typu seed na základě zákaznických vzorů nákupů. |
| Výběry pro vás              | AI-ML | Tento modul doporučuje individuální seznam produktů na základě zákaznických vzorů nákupů. Pro uživatele typu host bude tento seznam sbalen. |

## <a name="additional-resources"></a>Další prostředky

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)
