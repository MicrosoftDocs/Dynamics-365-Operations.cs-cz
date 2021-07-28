---
title: Odkaz na přihlášení přesměruje zpět na web elektronického obchodování
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se přihlašovací odkaz přesměruje zpět na web elektronického obchodování, místo aby přešel na přihlašovací stránku.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e83b381e73d28dce0a438a37d5f8ed23b4957adf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350371"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Odkaz na přihlášení přesměruje zpět na web elektronického obchodování

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se přihlašovací odkaz přesměruje zpět na web elektronického obchodování, místo aby přešel na přihlašovací stránku.

## <a name="description"></a>popis

Po konfiguraci nového tenanta Microsoft Azure Active Directory B2C (Azure AD B2C)v nástroji pro tvorbu webů Connect uživatelé, kteří vyberou odkaz **Přihlásit se**, jsou přesměrováni zpět na hlavní vstupní stránku elektronického obchodu, aniž by přešli na přihlašovací stránku.

## <a name="resolution"></a>Rozlišení

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Zkontrolujte, zda je adresa URL odpovědi správně nakonfigurována v aplikaci Azure AD B2C

Pro kontrolu, zda je adresa URL odpovědi správně nakonfigurována v aplikaci Azure AD B2C, postupujte následovně.

1. Přejděte na [portál Azure](https://portal.azure.com/).
1. Vyberte aplikaci Azure AD B2C, kterou jste vytvořili pro přístup na web.
1. Vyberte aplikaci, kterou jste vytvořili během nastavení Azure AD B2C.
1. V poli **URL pro odpověď** zkontrolujte, že seznam obsahuje položky pro adresu URL domény webu i adresu URL generovanou elektronickým obchodem, jak je znázorněno v příkladu na následujícím obrázku.

    ![Záznamy adresy URL pro odpověď Azure AD B2C.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Adresa URL domény webu i adresa generovaná elektronickým obchodem musí být v platném formátu adresy URL, který neobsahuje úvodní ani koncová lomítka.

## <a name="additional-resources"></a>Další prostředky

[Registrace připojené aplikace v Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Nastavení klienta B2C v Commerce](../set-up-b2c-tenant.md)