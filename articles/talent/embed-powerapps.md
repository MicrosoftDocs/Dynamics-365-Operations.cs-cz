---
title: Vložení aplikací Power Apps do Dynamics 365 Human Resources
description: Toto téma vysvětluje, jak vyřešit problém, kdy položka nabídky Microsoft Power Apps zmizela z modulu správy systému.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017866"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Vložení aplikací Power Apps do Dynamics 365 Human Resources

**Vydání**

Položka nabídky **Power Apps** zmizela z modulu **Správa systému**.

**Příčina**

Došlo ke změně návrhu uživatelského rozhraní a Microsoft Power Apps je nyní zahrnuta v standardním modelu přizpůsobení.

**Rozlišení**

Způsob integrace aplikací Power Apps se změnil. Aplikace Power Apps jsou nyní přidávány prostřednictvím modelu přizpůsobení. Aplikace Power Apps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 Talent.

Podrobné informace o tom, jak integrovat aplikace Power Apps do aplikace Talent, najdete v tématu [Integrace Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Všichni zákazníci Power Apps, kteří integrovali aplikace před změnou, by měli být upgradováni na nový model.

Tlačítko **Power Apps** je v pravém horním rohu téměř každé stránky v aplikaci Talent. Toto tlačítko můžete použít pro vložení aplikací.

Následuje příklad.

1. Přejděte na **Správa zaměstnanců \> Odkazy \> Pracovníci \> Zaměstnanci**.
2. Vyberte tlačítko **Power Apps** a poté vyberte možnost **Přidat aplikaci z Power Apps**.

    ![Tlačítko Power Apps](media/png.png)

3. Vyplňte pole v dialogovém okně **Přidat aplikaci z Power Apps**.

    ![Přidání aplikace z dialogového okna Power Apps](media/insert-powerapp.png)

Popřípadě postupujte následovně.

1. V podokně akcí stránky na kartě **Možnosti** ve skupině **Přizpůsobit** zvolte **Přizpůsobit tuto stránku**.

    ![Přizpůsobení skupiny na kartě Možnosti](media/options.png)

    Zobrazí se panel nástrojů individuálních nastavení.

2. Na panelu nástrojů vyberte možnost **Přidat aplikaci z Power Apps**.

    ![Přidání aplikace z Power Apps pomocí panelu nástrojů individuálního nastavení](media/powerapp-bar.png)
