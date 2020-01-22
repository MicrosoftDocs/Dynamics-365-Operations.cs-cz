---
title: Přístup k soukromým adresám podle role zabezpečení
description: Toto téma vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897090"
---
# <a name="access-to-private-addresses-by-security-role"></a>Přístup k soukromým adresám podle role zabezpečení

**Problém**

Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.

**Řešení**

Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.

1. Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.
2. Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.
3. Zvolte **Uložit**.

![Stránka parametrů globálního adresáře](media/GAD-parameters.png)
