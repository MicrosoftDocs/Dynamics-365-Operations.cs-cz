---
title: Přístup k soukromým adresám podle role zabezpečení
description: Toto téma vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 213aada51a477257df0b079c95e74610854b5a4f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689571"
---
# <a name="access-to-private-addresses-by-security-role"></a>Přístup k soukromým adresám podle role zabezpečení


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problém**

Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.

**Řešení**

Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.

1. Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.
2. Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.
3. Zvolte možnost **Uložit**.

![Stránka parametrů globálního adresáře.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
