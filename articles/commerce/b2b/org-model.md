---
title: Vytvářejte hierarchie modelování org pro organizace B2B
description: Toto téma popisuje, jak vytvořit hierarchie organizačního modelování pro organizace business-to-business (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035880"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Vytvářejte hierarchie modelování org pro organizace B2B

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak vytvořit hierarchie organizačního modelování pro organizace business-to-business (B2B) v Microsoft Dynamics 365 Commerce.

V centrále Commerce jsou organizace obchodních partnerů reprezentovány entitami zákazníků a entitami hierarchie zákazníků. Organizace obchodního partnera a její uživatelé jsou reprezentováni jako zákazníci a hierarchie zákazníků se používají k přidružení těchto zákazníků k sobě navzájem.

Po schválení požadavku obchodního partnera na připojení k webu elektronického obchodování B2B se provedou následující akce:

- V systému jsou vytvořeny dva nové záznamy o zákaznících: záznam zákazníka **Typ organizace** pro organizaci obchodního partnera a **Typ osoba** pro žadatele (tzn. obchodního partnera, který podal žádost).
- Nový záznam hierarchie zákazníků je vytvořen v **Zákazník \> Hierarchie zákazníků**. Tento záznam má následující vlastnosti záhlaví:

    - **ID hierarchie zákazníků** - Jedinečné ID pro hierarchii zákazníků. Toto ID používá číselnou sekvenci, která je definována ve sdílených parametrech Commerce v centrále Commerce.
    - **Název** - Název organizace obchodního partnera, jak je uveden v žádosti o přihlášení.
    - **Účel** - Tato vlastnost je nastavena na předdefinovanou hodnotu **B2B organizace**.
    - **Organizace** - zákaznické ID obchodního partnera.

Zde jsou podrobnosti záznamu hierarchie zákazníků:

- Záznam zákazníka - žadatele - je spojen s hierarchií zákazníků.
- Role správce je přidružena k žadateli.

Když správce přidá více uživatelů do organizace obchodního partnera na webu B2B, vytvoří se v centrále Commerce nový záznam zákazníka pro každého uživatele. Tento záznam zákazníka je také přidán do příslušného záznamu hierarchie zákazníků obchodního partnera a má roli „uživatele“.

> [!NOTE]
> Ve většině případů by se měly odpovídající hodnoty vlastností všech záznamů zákazníků v hierarchii shodovat. Například proto, že všichni uživatelé obchodních partnerů by měli získat podobné ceny produktů, jejich cenová skupina a související konfigurace by se měly shodovat. Systém však tuto konzistenci nevynucuje. Příslušní uživatelé centrály Commerce jsou proto zodpovědní za zajištění shody hodnot vlastností a konfigurací pro všechny zákazníky v dané hierarchii.

Uživatelé centrály Commerce se mohou podívat na hodnoty vlastností pro všechny záznamy zákazníků v hierarchii v souběžném zobrazení. Vyberte příslušné vlastnosti záznamu zákazníka výběrem názvů karet v rozevírací nabídce. Uživatelé mohou přímo prohlížet a upravovat hodnoty vlastností z tohoto zobrazení. Alternativně, pokud chcete použít všechny hodnoty ze záznamu zákazníka správce na všechny záznamy zákazníků uživatele, vyberte **Přepsat** v podrobnostech hierarchie zákazníků.

## <a name="additional-resources"></a>Další prostředky

[Nastavení webu elektronického obchodování B2B](set-up-b2b-site.md)

[Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování](manage-b2b-users.md)

[Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B](payment-method.md)

[Nastavte limity množství produktů pro weby B2B elektronického obchodování](quantity-limits.md)
