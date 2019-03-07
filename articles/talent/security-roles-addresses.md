---
title: Přístup k soukromým adresám podle role zabezpečení
description: Toto téma vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303529"
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
