---
title: Operace pro neshody
description: Tento článek popisuje, jak vytvářet a používat operace pro neshody.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847984"
---
# <a name="operations-for-nonconformances"></a>Operace pro neshody

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vytvářet a používat operace pro neshody.

Na stránce **Operace** můžete definovat klasifikace práce, které může být provedeny pro schválenou neshodu. Přiřadíte-li k neshodě související operaci, můžete poskytnout podrobné informace, například o přiřazeném materiálu, pracovní době a poplatcích vyžadovaných pro provedení této operace. Systém tyto informace používá k výpočtu odhadovaných nákladů na danou operaci. Podrobné informace a odhad nákladů jsou pouze informativní. Související operace pro kvalitu se liší od operací, které lze definovat ve výrobním postupu.

> [!NOTE]
> I když můžete sledovat náklady, čas a položky, které se používají v operaci související s neshodou, zadaná data jsou pouze informativní. Není automaticky integrován s hlavní knihou, podřízenou knihou inventáře nebo modulu **Čas a ducházka**.

## <a name="examples-of-operations"></a>Příklady operací

Pracujete pro výrobní společnost. Byla vytvořena a schválena neshoda pro položky, které neprošly testem kvality. Byla vytvořena oprava, která naznačuje, že problém souvisel se špatným uložením na stroji. K výměně ložiska je zapotřebí několik kroků a je sledována odpovědnost za každou operaci. Mohou být například vyžadovány následující kroky:

1. Výrobní linka je zastavena a je provedena rutina vyčištění.
1. Personál údržby vyměňte ložisko.
1. Pracovníci zajišťující kvalitu zkontrolují stroj před jeho opětovným zapnutím.

V tomto příkladu lze vytvořit následující operace představující práci, kterou je třeba provést:

- Zastavení výrobní linky.
- Vyčistění výrobní linky.
- Provedení údržby stroje.
- Zkontrolování stroje.

## <a name="create-an-operation"></a>Vytvoření operace

1. Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Operace**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Operace** - Zadejte jedinečné ID nebo název operace.
    - **Popis** - Zadejte podrobný popis operace.
    - **Typ** - Pokud lze operaci použít pouze u neshod, které souvisejí s konkrétním typem objednávky, vyberte typ objednávky (*Nákupní objednávka* nebo *Zakázka odběratele*).

1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Vytvoření a zpracování neshod](tasks/create-process-non-conformance.md)
- [Zaměstnanci odpovědní za schvalování neshod](quality-responsible-workers.md)
- [Karanténní zóny pro neshody](quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](quality-diagnostic-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Typy problémů pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
