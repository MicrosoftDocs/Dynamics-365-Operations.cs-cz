---
title: Integrace aplikací PowerApps v Dynamics 365 - Core HR
description: Toto téma vysvětluje, jak vyřešit problém, kdy položka nabídky PowerApps zmizela z modulu správy systému.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008423"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Integrace aplikací PowerApps v Core HR

[!include [banner](includes/banner.md)]

**Vydání**

Položka nabídky **PowerApps** zmizela z modulu **Správa systému**.

**Příčina**

Došlo ke změně návrhu uživatelského rozhraní a Microsoft PowerApps je nyní zahrnuta v standardním modelu přizpůsobení.

**Rozlišení**

Způsob integrace PowerApps se změnil. Aplikace PowerApps jsou nyní přidávány prostřednictvím modelu přizpůsobení. Aplikace PowerApps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 Talent.

Podrobné informace o tom, jak integrovat aplikace PowerApps do aplikace Talent, najdete v tématu [Integrace aplikací PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

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
