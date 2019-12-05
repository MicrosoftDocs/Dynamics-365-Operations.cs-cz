---
title: Integrace aplikací Power Apps v Dynamics 365 - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830202"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Integrace aplikací Power Apps v Dynamics 365 - Core HR

[!include [banner](includes/banner.md)]

**Vydání**

Položka nabídky **Power Apps** zmizela z modulu **Správa systému**.

**Příčina**

Došlo ke změně návrhu uživatelského rozhraní a Microsoft Power Apps je nyní zahrnuta v standardním modelu přizpůsobení.

**Rozlišení**

Způsob integrace aplikací Power Apps se změnil. Aplikace Power Apps jsou nyní přidávány prostřednictvím modelu přizpůsobení. Aplikace Power Apps můžete přidat téměř na všechny stránky aplikace Microsoft Dynamics 365 Talent.

Podrobné informace o tom, jak integrovat aplikace Power Apps do aplikace Talent, najdete v tématu [Integrace Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Všichni zákazníci Power Apps, kteří integrovali aplikace před změnou, by měli být upgradováni na nový model.

Tlačítko **Power Apps** je v pravém horním rohu téměř každé stránky v aplikaci Talent. Toto tlačítko můžete použít pro vložení aplikace Power Apps.

Následuje příklad.

1. Přejděte na **Správa zaměstnanců \> Odkazy \> Pracovníci \> Zaměstnanci**.
2. Vyberte tlačítko **Power Apps** a pak vyberte **Vložit PowerApp**.

    ![Tlačítko Power Apps](media/png.png)

3. Vyplňte pole v dialogovém okně **Vložit PowerApp**.

    ![Vložení dialogového okna PowerApp](media/insert-powerapp.png)

Popřípadě postupujte následovně.

1. V podokně akcí stránky na kartě **Možnosti** ve skupině **Přizpůsobit** zvolte **Přizpůsobit tento formulář**.

    ![Přizpůsobení skupiny na kartě Možnosti](media/options.png)

    Zobrazí se panel nástrojů individuálních nastavení.

2. Na panelu nástrojů zvolte **Vložit \> PowerApp**.

    ![Vložení aplikace Power Apps pomocí panelu nástrojů individuálního nastavení](media/powerapp-bar.png)
