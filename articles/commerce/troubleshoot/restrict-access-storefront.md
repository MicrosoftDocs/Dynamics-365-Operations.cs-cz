---
title: Omezení přístupu k výloze během testování nebo vývoje
description: Tento článek vysvětluje, jak omezit přístup k výloze Microsoft Dynamics 365 Commerce, zatímco probíhá interní testování nebo vývoj.
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
ms.openlocfilehash: 77b652aafa6aea807ab11fe02209bc7de43fa446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898877"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Omezení přístupu k výloze během testování nebo vývoje

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak omezit přístup k výloze Microsoft Dynamics 365 Commerce, zatímco probíhá interní testování nebo vývoj.

## <a name="description"></a>popis

Během interního testování nebo aktivního vývoje možná budete chtít omezit přístup na svůj web, abyste zabránili externím uživatelům v přístupu k publikovaným stránkám výlohy.

## <a name="resolution"></a>Rozlišení

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Nastavení Azure AD B2C pomocí standardních toků uživatelů

Informace o konfiguraci Azure Active Directory B2C (Azure AD B2C) pro váš web elektronického obchodování, viz [Nastavení tenanta B2C v Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Omezení přístupu uživatelů na hlavní stránky obchodu a zablokování vytváření nových uživatelů

Chcete-li omezit přístup uživatele na stránky výlohy v nástroji pro tvorbu webů Commerce, postupujte takto.

1. Přejděte na svůj web.
1. Vyberte **Stránky** a poté vyberte stránku, na kterou chcete omezit přístup uživatelů.
1. Vyberte slot modulu nebo fragmentu a poté vyberte **Upravit**.
1. V podokně vlastností vyberte **Vyžaduje přihlášení?** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

Chcete-li blokovat vytváření nových uživatelů v Azure AD, postupujte následovně.

1. Přejděte na [portál Azure](https://portal.azure.com/).
1. Vyberte aplikaci Azure AD B2C, kterou jste vytvořili pro přístup na web.
1. V levém navigačním podokně vyberte položku **Toky uživatelů**.
1. V horní části stránky **Toky uživatelů** vyberte možnost **Nový tok uživatele**.
1. Na stránce **Vybrat typ toku uživatele** vyberte **Náhled**.
1. Uprostřed stránky vyberte **Přihlásit se v2**. Poté postupujte podle pokynů v [Nastavení tenanta B2C v Commerce](../set-up-b2c-tenant.md) ke konfiguraci toku jako standardního toku uživatelů vašeho webu Azure AD B2C během testování nebo vývoje.

## <a name="additional-resources"></a>Další prostředky

[Nastavení klienta B2C v Commerce](../set-up-b2c-tenant.md)

[Nastavení vlastních stránek pro přihlášení uživatelů](../custom-pages-user-logins.md)
