---
title: Povolit ověřování Azure Active Directory pro přihlášení POS
description: V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro Microsoft Dynamics 365 Commerce pokladní místo (POS) tak, aby používalo ověřování Azure Active Directory.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 6946cb5f8bc8aa451f72d1eebcd324f408ad5f7a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975064"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Povolit ověřování Azure Active Directory pro přihlášení POS
[!include [banner](includes/banner.md)]


Mnozí zákazníci, kteří používají Microsoft Dynamics 365 Commerce také používají jiné cloudové služby Microsoft Cloud Service a mohou používat Azure Active Directory (Azure AD) ke správě uživatelských pověření pro tyto služby. V těchto případech mohou zákazníci chtít použít stejný Azure AD účet napříč aplikacemi. V tomto tématu je vysvětleno, jak nakonfigurovat přihlašovací prostředí pro pokladní místo (POS) Commerce tak, aby používalo ověřování Azure AD.

## <a name="configure-azure-ad-authentication"></a>Konfigurace ověřování Azure AD

Chcete-li použít Azure AD pro ověřování přihlášení POS pro obchod, je nutné nakonfigurovat nastavení funkčního profilu obchodu a pak tato nastavení aplikovat na klienty POS.

Při konfiguraci nového funkčního profilu postupujte takto.

1. Přejděte na **Maloobchodní a velkoobchodní prodej** \> **Nastavení kanálu** \> **Nastavení POS** \> **Profily POS** \> **Funkční profily** .
1. Vyberte funkční profil, který chcete změnit.
1. Na pevné záložce **Funkce** v části **přihlášení zaměstnance POS** změňte hodnotu pole **Metoda ověření přihlášení** z **ID a heslo personálu** na **Azure Active Directory** .

Všechny funkční profily standardně používají jako metodu ověřování POS **ID a heslo personálu** . Chcete-li tedy použít Azure AD, je nutné změnit hodnotu pole **Metoda ověření přihlášení** . Tato změna ovlivní všechny maloobchodní obchody propojené s vybraným profilem funkčnosti.

Chcete-li použít změny POS, postupujte podle následujících kroků.

1. Přejděte na **Retail a Commerce** \> **IT pro Retail a Commerce** \> **Plán distribuce** .
1. Spusťte plán distribuce **1070** ( **Konfigurace kanálu** ).

> [!NOTE]
> Ověření Azure AD vyžaduje připojení k Internetu. Pokud je POS v offline režimu, nebude fungovat.
> 
> V současné době funkce **Přepsání manažerem** nepodporuje Azure AD jako metodu ověřování. ID operátora a heslo jsou povinné, i když je řešení Azure AD nakonfigurováno jako metoda ověřování pro přihlášení do POS.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Přiřazení účtu Azure AD k pracovníkovi

Dříve, než může pracovník obchodu použít účet Azure AD pro přihlášení k aplikaci POS, musí být tento účet Azure AD přidružen k danému pracovníkovi.

Chcete-li účet Azure AD přidružit k pracovníkovi, postupujte podle následujících kroků.

1. Přejděte na **Retail a Commerce** \> **Zaměstnanci** \> **Pracovníci** .
1. Otevře stránku podrobností pro pracovníka.
1. V podokně akcí na kartě **Commerce** ve skupině **Externí identita** zvolte **Přidružit existující identitu** .
1. V dialogovém okně **Použít existující externí identitu** vyberte možnost **Hledat pomocí e-mailu** , zadejte e-mailovou adresu Azure AD a pak vyberte možnost **Hledat** .
1. Vyberte požadovaný účet Azure AD a poté vyberte tlačítko **OK** .

Pole **Alias** , **UPN** a **Externí dílčí identifikátor** na kartě **Commerce** na stránce Podrobnosti pracovníka budou vyplněna.

> [!NOTE]
> Po aktualizaci záznamu pracovníka, například pokud je nový Azure AD účet přidružen, změněno heslo nebo aktualizován adresář zaměstnance, doporučujeme spustit rozvrh distribuce **1060** ( **Personál** ) pro synchronizaci nejnovějších informací o personálu s kanálem. Aplikace POS tak může načíst správná data pro ověření uživatele a kontrolu autorizace.

## <a name="additional-resources"></a>Další prostředky

[Nastavení funkce rozšířeného přihlášení pro MPOS a Cloud POS](extended-logon.md)

[Vytvoření funkčního profilu maloobchodu](retail-functionality-profile.md)

[ Konfigurace pracovníka](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
