---
title: "Přístup k soukromým adresám podle role zabezpečení"
description: "Toto téma vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a>Přístup k soukromým adresám podle role zabezpečení

[!include [banner](includes/banner.md)]

**Problém**

Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.

**Řešení**

Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.

1. Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.
2. Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.
3. Zvolte **Uložit**.

![Stránka parametrů globálního adresáře](media/GAD-parameters.png)

