---
title: Moduly a stránky správy obchodního vztahu
description: Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206624"
---
# <a name="account-management-pages-and-modules"></a>Moduly a stránky správy obchodního vztahu

[!include [banner](includes/banner.md)]

Toto téma popisuje stránky a moduly správy účtů v řešení Microsoft Dynamics 365 Commerce.

Správa účtů představuje skupinu stránek, které se používají ke správě informací o uživatelských účtech v řešení Dynamics 365 Commerce. Stránky správy účtů zahrnují cílovou stránku správy účtu, stránku uživatelského profilu, stránku uživatelské adresy, stránku historie objednávek, stránku podrobností objednávky, věrnostní stránku a seznam přání.

### <a name="account-management-landing-page"></a>Cílová stránka správy obchodního vztahu

Cílová stránka správy účtu používá následující moduly:

- **Kontejner** – všechny moduly cílových stránek správy účtů by měly být umístěny v rámci kontejneru. 
- **Dlaždicce přivítání v účtu** – Tento modul slouží k poskytnutí uvítací zprávy na stránce správy účtu. Obsahuje vlastnosti pro záhlaví.
- **Obecná dlaždice účtu** – Tento modul lze použít k zadání záhlaví a odkazů na stránky pro správu účtů, jako jsou například stránky "Historie objednávek" nebo "Můj profil". Pomocí generického modulu dlaždice lze konfigurovat dlaždici pro libovolnou stránku. Ve společnosti Fabrikam se tento modul používá pro odkazy na stránce Historie objednávek a můj profil na cílové stránce správy účtů.
- **Dlaždice požadovanýcg položek účtu** – Tento modul slouží k poskytnutí souhrnu položek v seznamu přání zákazníka. Může například udávat „V seznamu přání máte 10 položek“. Zahrnuje vlastnosti pro záhlaví a odkaz „Zobrazit podrobnosti“. Odkaz „Zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku seznamu přání. 
- **Dlaždice adresy účtu** – Tento modul slouží k poskytnutí souhrnu adres uživatele. Může například udávat „Ve vašem účtu byly přidány 2 adresy“. Zahrnuje vlastnosti pro záhlaví a odkaz „Zobrazit podrobnosti“. Odkaz „Zobrazit podrobnosti“ by měl být nakonfigurován pro přesměrování na stránku adresy uživatele.
- **Věrnostní dlaždice účtu** – Tento modul slouží k zobrazení informací o věrnostních programech a odkazování na ně. Tato dlaždice má dva stavy: jeden z těchto stavů obsahuje odkazy na připojení k věrnostnímu programu, pokud uživatel již není členem. Pokud je uživatel již členem, zobrazí se v poli jiný stav odkazy na stránku věrnostní podrobnosti. Vlastnosti zahrnují nadpis, odkaz "Registrace" a odkaz "Zobrazit věrnostní program". Odkaz „Zobrazit věrnostní program“ by měl být nakonfigurován pro přesměrování na věrnostní stránku. Odkaz "Registrace" by měl být nakonfigurován pro přesměrování na stránku, na které se uživatelé mohou připojit k věrnostnímu programu. 

### <a name="order-history-page"></a>Stránka historie objednávek

Stránka historie objednávek využívá modul historie objednávek k zobrazení všech nedávných objednávek, které uživatel podal.

### <a name="order-details-page"></a>Stránka podrobností objednávky

Stránka podrobností objednávky poskytuje podrobné informace pro každou objednávku a je přístupná ze stránky historie objednávek. Používá modul podrobností objednávek, který vyžaduje ID prodeje nebo ID transakce k načtení podrobností objednávky.

### <a name="user-profile-page"></a>Stránka profilu uživatele

Na stránce profilu uživatele se zobrazují podrobnosti o účtu uživatele, jako je jméno nebo e-mailová adresa uživatele. Používá podrobnosti profilu uživatele a moduly úprav profilu uživatele. Ačkoli e-mailovou adresu nelze odebrat, je možné ji upravit. Stránka profilu uživatele také zobrazuje uživatelské předvolby, které umožňují uživateli přihlásit nebo odhlásit odběr některých funkcí, jako je přizpůsobení seznamů doporučení. 

### <a name="user-address-page"></a>Stránka adresy uživatele

Stránka adresy uživatele zobrazuje seznam adres, které jsou přidruženy k danému uživatelskému účtu. Uživatel buď tyto adresy poskytl na pokladně, nebo je přidal přímo na tuto stránku. Modul adresy uživatele se používá k přidávání a úpravám adres, k nastavení primární adresy a k vykreslení existujících adres na stránce.

### <a name="wish-list-page"></a>Stránka seznamu přání

Na stránce seznamu přání se zobrazují položky, které byly přidány do seznamu přání zákazníků. Pomocí modulu seznamu přání lze vykreslit položky v seznamu přání.

### <a name="loyalty-page"></a>Stránka věrnostního programu

Věrnostní stránka umožňuje zákazníkům zobrazit podrobnosti věrnostního programu v případě, že již jsou členy věrnostního programu. Mohou také zobrazit body, které získali a které byly uplatněny v posledních transakcích. Stránka využívá modul podrobnosti věrnostního programu k předvedení podrobností věrnostního programu. 

Chcete-li se připojit k věrnostnímu programu, můžete vytvořit marketingovou stránku s moduly věrnostních zápisů a věrnostních podmínek. Pokud uživatel není členem věrnostního programu, tyto moduly umožní uživateli, aby se přihlásil.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]