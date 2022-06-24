---
title: Povolit prognózu cashflow
description: Tento článek vysvětluje, jak zapnout funkci prognózy cashflow ve Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859850"
---
# <a name="enable-cash-flow-forecasting"></a>Povolit prognózu cashflow

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak zapnout funkci prognózy cashflow ve Finance Insights.

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

> [!NOTE]
> Trénink modelu **Předpověď peněžních toků** vyžaduje data se 100 nebo více transakcemi, která pokrývají více než jeden rok. Doporučujeme mít alespoň dva roky dat s více než 1 000 transakcemi.

Další informace o funkci prognózy cashflow naleznete v tématu [Prognóza cashflow](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
