---
title: Zpracování změn sazby
description: Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008313"
---
# <a name="process-rate-changes"></a>Zpracování změn sazby

[!include [banner](includes/preview-feature.md)]

Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti. Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování aktualizace změny sazby**.

2. V dialogovém okně **Spustit proces aktualizace sazby zaměstnanecké výhody** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | Období registrace | Období registrace, pro které mají být zpracovány změny sazeb. |

3. Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

   1. Zadejte informace pro proces.

   2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.

   3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.

   4. Vyberte **OK**. Proces bude spuštěn s nastavenými parametry.

4. Vyberte **OK**.
