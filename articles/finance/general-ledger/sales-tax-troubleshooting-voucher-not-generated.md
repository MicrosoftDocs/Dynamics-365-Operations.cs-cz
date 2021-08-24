---
title: Doklad se negeneruje
description: Toto téma poskytuje informace o řešení potíží, které mohou pomoci, když se má generovat doklad, ale negeneruje.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1fbd5b5bb4a1d2a0c498b2abac82bd6f5ff3f1d2ed9960885eb8f44cbb17884d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759865"
---
# <a name="voucher-isnt-generated"></a>Doklad se negeneruje

[!include [banner](../includes/banner.md)]

Pokud má být vygenerován poukaz, ale stránka **Transakce dokladu** nezobrazuje žádné doklady, při řešení tohoto problému postupujte podle pokynů v následujících částech.

[![Stránka Transakce dokladu, která neobsahuje žádné doklady.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Kontrola uplatnění daně

1. Přejděte k nabídce **Daň** \> **Periodické úkoly** \> **Položky dílčí hlavní knihy, které ještě nebyly přeneseny**.
2. Pokud existuje záznam v deníku, vyberte jej a poté vyberte možnost **Převést nyní**.

    [![Tlačítko Převést nyní na stránce Položky dílčí hlavní knihy, které ještě nebyly přeneseny.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Otevřete stránku **Transakce dokladu** znovu, abyste zjistili, zda byl poukaz vygenerován.

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení

Pokud jste dokončili kroky v předchozí části, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
