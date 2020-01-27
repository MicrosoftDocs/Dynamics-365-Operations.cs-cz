---
title: Stránky a moduly správy účtů
description: Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885802"
---
# <a name="account-management-pages-and-modules"></a>Stránky a moduly správy účtů

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Správa účtů představuje skupinu stránek, které se používají ke správě informací o uživatelských účtech v řešení Dynamics 365 Commerce. Stránky správy účtů zahrnují cílovou stránku správy účtu, stránku uživatelského profilu, stránku uživatelské adresy, stránku historie objednávek, stránku podrobností objednávky, věrnostní stránku a seznam přání.

### <a name="account-management-landing-page"></a>Cílová stránka správy obchodního vztahu

Cílová stránka správy účtu používá následující moduly:

- **Umístění obsahu** – Jedná se o modul kontejneru, který obsahuje všechny moduly na cílové stránce správy účtu.
- **Položka přivítání v účtu**– Tento modul slouží k poskytnutí uvítací zprávy na stránce správy účtu. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice. Vlastnost **Velikost dlaždice** definuje šířku modulu v modulu umístění obsahu. Hodnoty jsou v rozsahu **1** až **12**, kde **12** představuje celou šířku kontejneru umístění obsahu.
- **Položka podání objednávky účtu** – Tento modul se používá k vytvoření souhrnu počtu objednávek, které byly podány uživatelským účtem. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“. Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku historie objednávek.
- **Položka umístění profilu účtu** – Tento modul slouží k poskytnutí souhrnu profilu uživatele. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“. Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku profilu uživatele.
- **Požadovaná položka účtu** – Tento modul slouží k poskytnutí souhrnu položek v seznamu přání zákazníka. Může například udávat „V seznamu přání máte 10 položek“. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“. Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku seznamu přání.
- **Položka adresy účtu** – Tento modul slouží k poskytnutí souhrnu adres uživatele. Může například udávat „Ve vašem účtu byly přidány 2 adresy“. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“. Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku adresy uživatele.
- **Věrnostní položka účtu** – Tento modul slouží k zobrazení informací o věrnostních programech a odkazování na ně. Zahrnuje vlastnosti pro záhlaví a velikost dlaždice, a odkaz „zobrazit podrobnosti“ a další odkaz „stát se členem“. Odkaz „zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na věrnostní stránku. Odkaz "stát se členem" by měl být nakonfigurován pro přesměrování na stránku, na které se uživatelé mohou připojit k věrnostnímu programu.

### <a name="order-history-page"></a>Stránka historie objednávek

Stránka historie objednávek využívá modul historie objednávek k zobrazení všech nedávných objednávek, které uživatel podal.

### <a name="order-details-page"></a>Stránka podrobností objednávky

Stránka podrobností objednávky poskytuje podrobné informace pro každou objednávku a je přístupná ze stránky historie objednávek. Používá modul podrobností objednávek, který vyžaduje ID prodeje nebo ID transakce k načtení podrobností objednávky.

### <a name="user-profile-page"></a>Stránka profilu uživatele

Na stránce profilu uživatele se zobrazují podrobnosti o účtu uživatele, jako je jméno nebo e-mailová adresa uživatele. Používá modul profilu uživatele. Ačkoli e-mailovou adresu nelze odebrat, je možné ji upravit. Stránka profilu uživatele také zobrazuje uživatelské předvolby, které umožňují uživateli přihlásit nebo odhlásit odběr některých funkcí, jako je přizpůsobení seznamů doporučení. 

### <a name="user-address-page"></a>Stránka adresy uživatele

Stránka adresy uživatele zobrazuje seznam adres, které jsou přidruženy k danému uživatelskému účtu. Uživatel buď tyto adresy poskytl na pokladně, nebo je přidal přímo na tuto stránku. Modul adresy uživatele se používá k přidávání a úpravám adres, k nastavení primární adresy a k vykreslení existujících adres na stránce.

### <a name="wish-list-page"></a>Stránka seznamu přání

Na stránce seznamu přání se zobrazují položky, které byly přidány do seznamu přání zákazníků. Pomocí modulu seznamu přání lze vykreslit položky v seznamu přání.

### <a name="loyalty-page"></a>Stránka věrnostního programu

Věrnostní stránka umožňuje zákazníkům připojit se k věrnostnímu programu, nebo v případě, že již jsou členy věrnostního programu, zobrazit podrobné informace o programu. Mohou také zobrazit body, které získali a které byly uplatněny v posledních transakcích.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
