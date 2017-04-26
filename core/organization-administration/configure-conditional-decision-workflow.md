---
title: "Konfigurace podmíněného rozhodnutí v pracovním postupu"
description: "Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 3bba3d849d02cd84c2c0e0c5c15f7b649b3e125c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurace podmíněného rozhodnutí v pracovním postupu

[!include[banner](../includes/banner.md)]


Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.

Podmíněné rozhodnutí je bod, ve kterém se workflow dělí na dvě větve. Pokud budete chtít nakonfigurovat podmíněné rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na podmíněné rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.

## <a name="name-a-decision"></a>Pojmenování rozhodnutí
Pomocí následujících kroků zadejte název podmíněného rozhodnutí.
1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  V poli **Název** zadejte jedinečný podmíněného rozhodnutí.

## <a name="set-conditions"></a> Stanovení podmínek
V tomto okamžiku systém určí, která větev se použije, vyhodnocením odeslaného dokumentu k určení, zda vyhovuje konkrétním podmínkám.
1.  V levém podokně klepněte na tlačítko **Základní nastavení**.
2.  Click **Add condition**.
3.  Zadání podmínky
4.  Zadejte všechny další podmínky, pokud jsou požadovány.
5.  Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:
    1.  Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.
    2.  Vyberte v oblasti **Ověřit podmínku** formuláře záznam.
    3.  Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.
    4.  Klepněte na tlačítko **OK** nebo **zrušení** se vraťte **vlastnosti** formulář.






