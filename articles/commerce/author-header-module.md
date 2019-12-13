---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697268"
---
# <a name="header-module"></a>Modul záhlaví

[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]

Toto téma popisuje moduly záhlaví a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul záhlaví je speciální kontejner, který se používá k hostování všech modulů, které budou zobrazeny v záhlaví stránky. Může například obsahovat logo webu, odkazy na hierarchii navigace, odkazy na další stránky na webu a vyhledávací panel.

Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (tj. desktopové nebo mobilní zařízení). Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).

## <a name="properties-of-a-header"></a>Vlastnosti záhlaví

Podobně jako běžné kontejnery podporuje modul záhlaví vlastnosti **nadpis** a **šířka**.

Modul záhlaví obsahuje více pozic. Obsahuje například pozice pro informační zprávu, navigační nabídku, logo, vyhledávací panel, ikonu vozíku, ikonu seznamu přání a informace o účtu. Každá pozice podporuje určitou sadu modulů.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduly, které jsou k dispozici v modulu záhlaví

Následující moduly lze použít v modulu záhlaví:

- **Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy. Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Retail. Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví. Kromě toho lze konfigurovat statické navigační odkazy a poskytnout relativní odkazy na jiné stránky na webu elektronického obchodování. Samotné záhlaví lze zarovnat doleva, doprava nebo na střed.
- **Ikona košíku** – Ikona košíku je speciální ikona, která představuje košík. Je zobrazena v záhlaví a udává počet položek v vozíku. Odkaz na stránku košíku by měl doprovázet ikonu košíku, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku košíku.
- **Ikona seznamu přání** – V záhlaví je zobrazena ikona seznamu přání a udává počet přidaných položek do seznamu přání zákazníka. Odkaz na stránku seznamu přání by měl doprovázet tuto ikonu, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku seznamu přání.
- **Přihlašovací modul** – V záhlaví se zobrazí přihlašovací modul. Odběratelé se mohou přihlásit nebo registrovat k účtu. Pokud je zákazník již přihlášen, lze tento modul nakonfigurovat tak, aby zobrazoval odkazy na stránku účtu, stránku historie objednávek nebo jinou stránku.
- **Modul loga** – Tento modul zobrazuje logo, které představuje maloobchodníka a značku. Jedná se o obrázek s odkazem. Odkaz je obvykle konfigurován tak, že přesměruje na domovskou stránku. Zákazníci se tedy mohou rychle vrátit na domovskou stránku z libovolné stránky na webu.
- **Výstraha** – V záhlaví se zobrazí výstraha, která slouží k zobrazení vložené zprávy, která se vztahuje na všechny stránky na webu. Výstraha může například zobrazovat zprávu, že „Výroční výprodej končí za 2 dny“.
- **Vyhledávací panel** – Vyhledávací panel umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty. Modul musí být konfigurován s adresou URL stránky výsledků hledání. Parametr řetězce dotazu lze nakonfigurovat (výchozí hodnota je **„q“**). Vyhledávací panel obsahuje pozici automatických návrhů, kam by měl být přidán modul automatických návrhů.
- **Automatické návrhy** – Modul automatických návrhů zobrazuje automaticky navrhované výsledky. Může se jednat o tyto výsledky: klíčová slova, produkty nebo kategorie, ve kterých je hledaný výraz nalezen.

## <a name="create-a-header-module"></a>Vytvoření modulu záhlaví

Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.

1. Vytvořte fragment stránky, který obsahuje modul záhlaví.
1. Přidejte moduly do pozic v modulu záhlaví.
1. Aktualizujte nastavení pro každý modul.
1. Uložte fragment stránky. 
1. Vraťte stránku se změnami a publikujte ji.

Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.

1. Na výchozí stránce přidejte do hlavní pozice záhlaví fragment stránky obsahující modul záhlaví.
1. Uložte šablonu. 
1. Vraťte šablonu se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
