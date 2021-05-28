---
title: Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1
description: Toto téma vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.
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
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019439"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Nastavení vývojového prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit vývojové prostředí elektronického obchodování pro ladění proti virtuálnímu počítači maloobchodního serveru úrovně 1.

## <a name="description"></a>popis

Microsoft Dynamics 365 Commerce úrovně 1 se obvykle nasazuje pro Commerce Runtime (CRT) a vývoj rozšíření pokladního místa (POS). Jsou to samostatná prostředí. Vzhledem k povaze architektury softwaru jako služby (SaaS) neobsahují komponenty elektronického obchodování.

V některých scénářích můžete chtít otestovat volání rozšíření v prostředí úrovně 1, abyste mohli ladit rozšíření z komponent elektronického obchodování. Obecné pokyny naleznete v části [Ladění proti vývojovému prostředí Commerce úrovně 1](../e-commerce-extensibility/debug-tier-1.md).

Když ladíte proti prostředí úrovně 1, protože web nyní volá jiný maloobchodní server, volání mezi servery mohou způsobit různé chyby související se zásadami zabezpečení obsahu.

Následující obrázek ukazuje příklad chyby, ke které může dojít při výběru varianty na stránce s podrobnostmi o produktu.

![Chyba při výběru varianty na stránce s podrobnostmi o produktu](media/unhandled-rejection-error.jpg)

Následující obrázek ukazuje příklad podobné chyby v ladicích nástrojích prohlížeče (Vývojářské nástroje F12). Chybová zpráva zmiňuje porušení směrnice o zásadách zabezpečení obsahu.

![Chyba nástrojů ladicího programu](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Rozlišení

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
