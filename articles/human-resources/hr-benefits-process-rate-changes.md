---
title: Zpracování změn sazby
description: Toto téma vysvětluje, jak zpracovat změny sazby zaměstnanecké výhody v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1eea61df6dd5fbe0b52a21944deba69928b5125
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696119"
---
# <a name="process-rate-changes"></a>Zpracování změn sazby


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma vysvětluje, jak zpracovat změny sazeb zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti. Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování aktualizace změny sazby**.

2. V dialogovém okně **Spustit proces aktualizace sazby zaměstnanecké výhody** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Období registrace** | Období registrace, pro které mají být zpracovány změny sazeb. |

3. Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

   1. Zadejte informace pro proces.

   2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.

   3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.

   4. Vyberte **OK**. Proces bude spuštěn s nastavenými parametry.

4. Vyberte **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
