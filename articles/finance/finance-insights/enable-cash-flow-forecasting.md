---
title: Povolit prognózu cashflow
description: Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d968f28126cf205a487d84301aa28f1251713386
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752681"
---
# <a name="enable-cash-flow-forecasting"></a>Povolit prognózu cashflow

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve Finance Insights.

> [!NOTE]
> Chcete-li použít předpovědi plateb v cashflow, musíte nastavit funkci předpovědí plateb zákazníků, jak je popsáno v části [Povolení předpovědí plateb zákazníka](enable-cust-paymnt-prediction.md).
  
1. Otevřete pracovní prostor **Správa funkcí** a postupujte takto:

    1. Vyberte možnost **Zkontrolovat aktualizace**.
    2. Na kartě **Vše** vyhledejte **Předpovědi cashflow**. Pokud tuto funkci nemůžete najít, vyhledejte **(Preview) Návrh cashflow**. 
    3. Zapnutí funkce.

2. Přejděte na **Pokladna a banka \> Nastavení prognózy cashflow** a přidejte účty likvidity, které by měly být zahrnuty do prognóz. Nastavte také účet likvidity pro platby na kartách **Pohledávky** a **Závazky**. Nezapomeňte přepočítat prognózu cashflow.

    > [!NOTE]
    > Pokud nejsou zřízeny účty likvidity, nelze generovat cashflow.
    >
    > Další informace o nastavení prognóz cashflow naleznete v tématu [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md).

3. Jděte na **Pokladna a banka \> Nastavení \> Finanční přehledy (Preview) \> Prognózy cashflow (Preview)** a postupujte takto:

    1. Na kartě **Prognózy cashflow** vyberte **Povolit funkci**.
    2. Vyberte **Vytvořit predikční model**.

Další informace o funkci prognózy cashflow naleznete v tématu [Prognóza cashflow](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
