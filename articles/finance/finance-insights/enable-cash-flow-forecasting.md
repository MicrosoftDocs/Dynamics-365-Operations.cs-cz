---
title: Povolení prognózy cashflow (Preview)
description: Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: 29118557a1de4d3521f8125395b26471f7f48f3e
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638614"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Povolení prognózy cashflow (Preview)

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.

> [!NOTE]
> Chcete-li použít předpovědi plateb v cashflow, musíte nastavit funkci předpovědí plateb zákazníků, jak je popsáno v části [Povolení předpovědí plateb zákazníka](enable-cust-paymnt-prediction.md).

1. Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí. Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu. (Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Tento krok přeskočte, pokud používáte verzi 10.0.20 nebo novější nebo pokud používáte nasazení Service Fabric. Tým finančních přehledů už měl testování zapnout za vás. Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.
  
2. Otevřete pracovní prostor **Správa funkcí** a postupujte takto:

    1. Vyberte možnost **Zkontrolovat aktualizace**.
    2. Zapněte následující funkce:

        - Nový ovládací prvek mřížky
        - Seskupování do mřížek (Preview) 
        - Předpovědi plateb odběratelů (Preview)
        - Prognózy cashflow (Preview)

3. Přejděte na **Pokladna a banka \> Nastavení prognózy cashflow** a přidejte účty likvidity, které by měly být zahrnuty do prognóz.

    > [!NOTE]
    > Pokud nejsou zřízeny účty likvidity, nelze generovat cashflow.

4. Jděte na **Pokladna a banka \> Nastavení \> Finanční přehledy (Preview) \> Prognózy cashflow (Preview)** a postupujte takto:

    1. Na kartě **Prognózy cashflow** vyberte **Povolit funkci**.
    2. Vyberte **Vytvořit predikční model**.

Další informace o funkci prognózy cashflow naleznete v tématu [Prognóza cashflow](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
