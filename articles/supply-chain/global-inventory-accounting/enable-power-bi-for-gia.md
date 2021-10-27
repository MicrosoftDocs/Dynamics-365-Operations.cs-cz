---
title: Povolit Power BI pro globální účetnictví zásob
description: Toto téma popisuje, jak povolit Microsoft Power BI pro globální účtování zásob.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0b00de29a4f12719e469c063861b52e0fc20c5f1
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641104"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Povolit Power BI pro globální účetnictví zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Můžete připnout dlaždice, řídicí panely a zprávy ze svého účtu [PowerBI.com](https://powerbi.com/) do pracovního prostoru aplikace Microsoft Dynamics 365.

## <a name="prerequisites"></a>Předpoklady

Než budete moci povolit výkaznicktví Power BI, musí být splněny následující předpoklady:

- V aplikaci Dynamics 365 musíte být správcem systému.
- Musíte mít účet [PowerBI.com](https://powerbi.com/).
- Musíte mít alespoň jeden řídicí panel a jednu sestavu ve svém účtu Power BI.
- Musíte být správcem svého účtu Azure Active Directory (Azure AD).
- Doména Azure AD musí být stejná doména, kterou jste použili pro svůj účet [PowerBI.com](https://powerbi.com/).

## <a name="setup"></a>Nastavení

Pro nastavení integrace Power BI postupujte následujícím způsobem.

1. Přihlaste se do [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Přčejděte na **Knihovnu sdíleného majetku**, vyberte **model vykazování Power BI** jako typ majetku a stáhněte balíček **Globální účtování zásob**. 
1. Přihláste se do [PowerBI.com](https://app.powerbi.com/) a nahrajte soubor sestavy **Globální účtování zásob** Power BI pomocí následujících kroků:

    1. Zvolte **Nové**.
    1. Vyberte **Odeslat soubor**.
    1. Vyberte soubor sestavy **Globální účtování zásob** Power BI.

1. Nakonfigurujte sestavu **Globální účtování zásob** Power BI podle těchto kroků:

    1. Přejděte do **Můj pracovní prostor**, vyhledejte datovou sadu pro Globální účetnictví zásob a poté v nabídce **Možnosti** vyberte **Nastavení**.
    1. V **Nastavení pro globální účtování zásob** rozbalte **Parametry** a podle potřeby aktualizujte všechny parametry. Zkontrolujte zejména následující nastavení:
        1. Přepište výchozí hodnoty **Dataverse Url** a **ID prostředí** za hodnoty nalezené na stránce **Podrobnosti o prostředí** v LCS (v části **Integrace Power Platform**).
        1. Vyberte odkaz **Upravit přihlašovací údaje** vedle štítku **CD** v části **Přihlašovací údaje ke zdroji dat**. Poté se přihlaste do svého účtu Dataverse pomocí metody ověřování **OAuth2**.
    1. Ověřte, že zprávy Power BI nalezené v části **Můj pracovní prostor \> Zprávy \> Globální účetnictví zásob** nyní fungují správně a zobrazují obsah z vašeho systému.

1. Zaregistrujte aplikaci podle popisu v [Konfigurace integrace PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).
1. Integrujte soubor sestavy **Globální účtování zásob** Power BI do Dynamics 365 Supply Chain Management podle těchto kroků:

    1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace PowerBI.com**.
    1. Vyberte možnost **Upravit**.
    1. Vyberte **Povolit integraci PowerBI.Com**.
    1. V poli **ID aplikace** zadejte ID aplikace.
    1. V poli **Klíč aplikace** zadejte klíč aplikace.
    1. Zvolte možnost **Uložit**.

1. Obnovte stránku tak, aby se zobrazilo přihlašovací dialogové okno Power BI.
1. Na kartě **Možnosti** vyberte **Otevřít katalog sestav** a potom vyberte soubor sestavy **Globální účtování zásob** Power BI, který jste nahráli dříve.
1. Aktualizujte stránku. Měli byste vidět, že vaše zpráva byla přidána.
1. V nabídce **Sestavy Power BI** vyberte odkaz **Globální účtování zásob**.

Další informace naleznete v tématu [Konfigurace integrace PowerBI.com](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
