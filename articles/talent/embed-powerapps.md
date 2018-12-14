---
title: "Integrace aplikací PowerApps v Core HR"
description: "Toto téma vysvětluje, jak vyřešit problém, kdy položka nabídky PowerApps zmizela z modulu správy systému."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a>Integrace aplikací PowerApps v Core HR

[!include [banner](includes/banner.md)]

**Problém**

Položka nabídky **PowerApps** zmizela z modulu **Správa systému**.

**Příčina**

Došlo ke změně návrhu uživatelského rozhraní a Microsoft PowerApps je nyní zahrnuta v standardním modelu přizpůsobení.

**Rozlišení**

Způsob integrace PowerApps se změnil. Aplikace PowerApps jsou nyní přidávány prostřednictvím modelu přizpůsobení. Aplikace PowerApps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 for Talent.

Podrobné informace o tom, jak integrovat aplikace PowerApps do aplikace Talent, najdete v tématu [Integrace aplikací PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Všichni zákazníci PowerApps, kteří integrovali aplikace před změnou, by měli být upgradováni na nový model.

Tlačítko **PowerApps** je v pravém horním rohu téměř každé stránky v aplikaci Talent. Toto tlačítko můžete použít pro vložení aplikace PowerApps.

Následuje příklad.

1. Přejděte na **Správa zaměstnanců \> Odkazy \> Pracovníci \> Zaměstnanci**.
2. Vyberte tlačítko **PowerApps** a pak vyberte **Vložit PowerApp**.

    ![Tlačítko PowerApps](media/png.png)

3. Vyplňte pole v dialogovém okně **Vložit PowerApp**.

    ![Vložení dialogového okna PowerApp](media/insert-powerapp.png)

Popřípadě postupujte následovně.

1. V podokně akcí stránky na kartě **Možnosti** ve skupině **Přizpůsobit** zvolte **Přizpůsobit tento formulář**.

    ![Přizpůsobení skupiny na kartě Možnosti](media/options.png)

    Zobrazí se panel nástrojů individuálních nastavení.

2. Na panelu nástrojů zvolte **Vložit \> PowerApp**.

    ![Vložení aplikace PowerApps pomocí panelu nástrojů individuálního nastavení](media/powerapp-bar.png)

