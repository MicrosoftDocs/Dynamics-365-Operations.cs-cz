---
title: Instalace řešení Invoice Capture
description: Tento článek poskytuje informace o tom, jak nainstalovat řešení Invoice Capture a jak je integrovat s Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691143"
---
# <a name="install-the-invoice-capture-solution"></a>Instalace řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Pokud jste nainstalovali řešení v private preview, musíte před pokračováním odinstalovat staré řešení.

## <a name="prerequisites"></a>Předpoklady

Před tím, než budete moci nainstalovat řešení Invoice Capture, je třeba splnit následující předpoklady:

1. Zaregistrujte aplikaci a přidejte tajný kód klienta do Microsoft Azure Active Directory (Azure AD) v rámci vašeho předplatného Azure. Další informace naleznete v tématu [Registrace webové aplikace pomocí AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Poznamenejte si **ID aplikace (klienta)**, **Tajný kód klienta** a **ID klienta**, protože je budete později potřebovat.

2. Zaregistrujte aplikaci Azure v prostředí Dynamics 365 Finance. Další informace naleznete v tématu [Registrace externí aplikace](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Instalace a nastavení řešení

Chcete-li nainstalovat řešení Invoice Capture, přejděte na AppSource a vyberte odkaz na verzi preview [Dynamics 365 Invoice capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Po dokončení instalace uvidíte řešení nainstalované ve vybraném prostředí v Power Apps.

Abyste dokončili nastavení, postupujte takto.

1. Stáhněte [asistenční řešení](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) pro nastavení následujících podrobností:

    - Komunikace mezi Microsoft Power Platform a prostředím Finance
    - Informace o připojení pro Dataverse a Office 365 Outlook, který bude kanál používat

2. V Power Apps přejděte do svého prostředí a vyberte **Import řešení**.
3. Vyberte **Procházet**, vyberte balíček asistenčního řešení, který jste si stáhli, a poté vyberte **Další**.
4. Zvolte **Další**.
5. Přiřaďte existující připojení nebo vytvořte nové výběrem **Nové připojení**.
6. Po úspěšném importu balíčku otevřete **Dynamics 365 Invoice capture – instalační nástroje**.
7. Spusťte cloudový tok a nastavte propojení mezi řešením pro zachycení faktur v Microsoft Power Platform a Finance.
8. Vyberte **Spustit** a zadejte následující parametry:

    - **Adresa URL Dynamics 365 Finance** – URL finančního prostředí, se kterým se chcete integrovat.
    - **ID tenanta** – ID tenanta pro prostředí Finance.
    - **ID klienta** – ID aplikace Azure, která byla zaregistrována.
    - **Tajný klíč klienta** – Tajný klíč klienta, který byl generován pro aplikace Azure.
