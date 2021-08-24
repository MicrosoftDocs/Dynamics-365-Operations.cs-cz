---
title: Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních
description: Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele.
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
ms.openlocfilehash: e5b429badcbcc0e9829d82785a6e1f1a2504f5ec9b9ac74d249032f272dea103
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747240"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví (ER). Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace. V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.

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