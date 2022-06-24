---
title: Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních
description: Tento článek vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93c2e114c97290347b71e94d87ea5339688791cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883589"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví (ER). Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace. V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.

## <a name="create-a-provider"></a>Vytvoření poskytovatele
1. Přejděte do **navigačního podokna** v levém horním rohu a vyberte možnost **Správa organizace**.
2. Přejděte na **Pracovní prostory > Elektronické sestavy**.
3. Přejděte na **Související odkazy > Poskytovatelé konfigurace**.
4. Zvolte **Nové**.
    - Záznam poskytovatele má jedinečný název a adresu URL. Pokud již záznam pro společnosti Litware, Inc. (https://www.litware.com) existuje, zkontrolujte obsah této stránky a přeskočte tuto proceduru.  
5. Do pole Název zadejte `Litware, Inc.`.
6. Do pole Internetová adresa zadejte `https://www.litware.com`.
7. Zvolte **Uložit**.
8. Zavřete stránku.

## <a name="select-as-an-active-provider"></a>Výběr ve formě aktivního poskytovatele
1. Vyberte poskytovatele Litware, Inc.
2. Vyberte **Nastavit jako aktivní**.

![Stránka pracovního prostoru elektronického vykazování.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]