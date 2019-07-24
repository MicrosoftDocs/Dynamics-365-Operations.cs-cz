---
title: Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních
description: Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví (ER) v aplikaci Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e02cd51478528db56a4f50b134fabf7f9e1dc8ea
ms.sourcegitcommit: a1354c6218b328d4d7dcc149d1339a7af10c48bf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2019
ms.locfileid: "1723113"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví (ER) v aplikaci Dynamics 365 for Finance and Operations. Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace. V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.

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

