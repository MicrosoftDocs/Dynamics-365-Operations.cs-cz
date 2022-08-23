---
title: Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1
description: Tento článek vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 64e03c742f7095e2e485f32ad534f2a755ddd062
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277872"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.

## <a name="description"></a>popis

Microsoft Dynamics 365 Commerce úrovně 1 se obvykle nasazuje pro Commerce Runtime (CRT) a vývoj rozšíření pokladního místa (POS). Jsou to samostatná prostředí. Vzhledem k povaze architektury softwaru jako služby (SaaS) neobsahují komponenty elektronického obchodování.

V některých scénářích můžete chtít otestovat volání rozšíření v prostředí úrovně 1, abyste mohli ladit rozšíření z komponent elektronického obchodování. Obecné pokyny naleznete v části [Ladění proti vývojovému prostředí Commerce úrovně 1](../e-commerce-extensibility/debug-tier-1.md).

Když ladíte proti prostředí úrovně 1, protože web nyní volá jiný maloobchodní server, volání mezi servery mohou způsobit různé chyby související se zásadami zabezpečení obsahu.

Následující obrázek ukazuje příklad chyby, ke které může dojít při výběru varianty na stránce s podrobnostmi o produktu.

![Chyba při výběru varianty na stránce s podrobnostmi o produktu.](media/unhandled-rejection-error.jpg)

Následující obrázek ukazuje příklad podobné chyby v ladicích nástrojích prohlížeče (Vývojářské nástroje F12). Chybová zpráva zmiňuje porušení směrnice o zásadách zabezpečení obsahu.

![Chyba nástrojů ladicího programu.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Řešení

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Deaktivace zásad zabezpečení obsahu pro web v nástroji pro tvorbu webů Commerce

1. Vyberte web, na kterém pracujete.
1. Vyberte **Nastavení** a pak vyberte **Rozšíření**.
1. Na kartě **Zásady zabezpečení obsahu** vyberte **Deaktivovat zásady zabezpečení obsahu**.
1. Vyberte možnost **Uložit a publikovat**.

> [!NOTE]
> Přihlášení mezi podniky a spotřebitelem (B2C) nebude fungovat v místním vývojovém prostředí. Můžete však použít pokladny hosta nebo vytvořit falešné stránky k simulaci přihlášení uživatele podle potřeby.

## <a name="additional-resources"></a>Další prostředky

[Začněte s online vývojem rozšiřitelnosti elektronického obchodu](../e-commerce-extensibility/sdk-getting-started.md)

[Správa zásady zabezpečení obsahu (CSP) na webu elektronického obchodování](../manage-csp.md)
