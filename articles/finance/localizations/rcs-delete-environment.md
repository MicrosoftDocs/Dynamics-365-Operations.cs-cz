---
title: Regulatory Configuration Service (RCS) – Odstranění prostředí RCS
description: Tento článek vysvětluje, jak může správce systému Regulatory Configuration Service (RCS) odstranit prostředí RCS a související data.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277201"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Odstranění prostředí RCS

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak může správce systému Regulatory Configuration Service (RCS) odstranit prostředí RCS a související data.

Než budete moci dokončit postup uvedené v tomto článku, musí být splněny následující předpoklady:

- Musíte mít přidělenou roli **Systémový administrátor** pro prostředí RCS.
- Role **Správce systému** musí mít přiřazenou roli **RCSDeleteEnvironmentDuty**.

## <a name="delete-an-rcs-environment"></a>Ostraňte prostředí RCS

1. Otevřete RCS a vyberte dlaždici pracovního prostoru **Elektronické výkaznictví**.
2. V části **Související odkazy** vyberte **Odstranit prostředí RCS**.

    ![V části Související odkazy vyberte Odstranit prostředí RCS.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. V zobrazeném dialogovém okně zkontrolujte zprávy o rozsahu odstranění prostředí.

    ![Zprávy v dialogovém okně Odstranit prostředí RCS.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Odstranění prostředí RCS nelze vrátit zpět.
    >
    > Operace odstraní vybrané prostředí RCS a veškerá související data, včetně funkcí a konfigurací, které jsou uloženy v globálním úložišti. Funkce a konfigurace sdílené s jinými organizacemi budou sdíleny a odstraněny, pokud nemají žádné závislosti. Funkce a konfigurace, které mají závislosti, budou označeny jako ukončené.

4. Do pole, které je k dispozici, zadejte globálně jedinečný identifikátor (GUID) prostředí RCS a potvrďte, že jej chcete odstranit. GUID prostředí je součástí zprávy o odstranění.
5. Zvolte **Odstranit prostředí**.
    
Vaše prostředí RCS a veškerá související data jsou nyní odstraněna.

> [!IMPORTANT]
> Po odstranění prostředí RCS není možné data obnovit. Nové prostředí RCS lze vytvořit v jakékoli dostupné oblasti RCS.
