---
title: Zpracování změn sazby
description: Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803818"
---
# <a name="process-rate-changes"></a>Zpracování změn sazby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti. Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku. 

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