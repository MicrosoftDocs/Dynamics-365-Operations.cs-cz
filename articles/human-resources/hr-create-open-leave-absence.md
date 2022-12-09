---
title: Vytvoření pracovního volna s otevřeným koncem
description: Tento článek vysvětluje, jak vytvořit pracovní volno s otevřeným koncem v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805335"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Vytvoření pracovního volna s otevřeným koncem

> [!IMPORTANT]
> Funkce, která je popsaná v tomto článku, bude dostupná jako součást budoucího vydání na infrastruktury Finance po vydání Microsoft Dynamics 365 Finance 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete podat žádost o pracovní volno s otevřeným koncem a zobrazit stav svých žádostí o volno v Dynamics 365 Human Resources.

## <a name="prerequisites"></a>Předpoklady

1. V části **Správa funkcí** se ujistěte, že je zapnutá funkce **Pracovní volno s otevřeným koncem** .

    > [!IMPORTANT]
    > Poté, co tuto funkci zapnete, ji nelze vypnout.

2. Vytvořte typ dovolené pracovního volna.
3. Zadejte údaje, jako je typ dovolené, popis a ID pracovního postupu.
4. V poli **Typ požadavku** vyberte **Pracovní volno**.
5. V sekci podrobností pro dovolené s otevřeným koncem nastavte možnost **S otevřeným koncem** na **Ano**.
6. Nastavte možnost **Oznámení o návratu do práce** na **Ano** nebo **Ne**.
7. U žádostí o pracovní volno s otevřeným koncem lze volitelně vyžadovat oznámení o návratu do práce.

> [!NOTE]
> Po zapnutí této funkce bude zapnut také funkce **Je požadována příloha**.

## <a name="request-an-open-ended-leave-of-absence"></a>Vyžádání pracovního volna s otevřeným koncem

1. V pracovním prostoru **Samoobsluha pro zaměstnance** na **Zůstatky volna** vyberte **Více (…)**.
2. Chcete-li odeslat žádost o volno, vyberte **Žádost o pracovní volno**.
3. Zadejte informace do polí **Typ pracovního volna** a **Počáteční datum**. Do pole **Koncové datum** zadejte nezávazné koncové datum.
4. Potřebujete-li odeslat jakoukoli podpůrnou dokumentaci, v části **Přílohy** vyberte možnost **Odeslat**.
5. Jakmile budete připravení žádost odeslat, vyberte **Odeslat**. Jinak vyberte **Uložit koncept**.
6. Chcete-li aktualizovat žádost o pracovní volno s otevřeným koncem, vyberte žádost, zadejte datum ukončení do pole **Datum ukončení**, nastavte možnost **Potvrdit datum ukončení** na **Ano** a nahrajte dokumentaci.
7. Pokud je možnost **Oznámení o návratu do práce** nastaveno na **Ano**, vyberte **Nahrát** a poté zaškrtnutím políčka potvrďte, že bylo nahráno platné oznámení o návratu do práce.
8. Po zadání všech údajů vyberte **Odeslat**.
