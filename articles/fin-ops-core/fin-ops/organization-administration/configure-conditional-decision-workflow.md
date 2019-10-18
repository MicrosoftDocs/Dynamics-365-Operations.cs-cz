---
title: Konfigurace podmíněných rozhodnutí ve workflow
description: Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 278773a5ad8be35f9b6dcd1ec0d0a35e32222bb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176881"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Konfigurace podmíněných rozhodnutí ve workflow

[!include [banner](../includes/banner.md)]

Následně nakonfigurujte vlastnosti podmíněného rozhodnutí pomocí následujícího postupu.

Podmíněné rozhodnutí je bod, ve kterém se workflow dělí na dvě větve. Pokud budete chtít nakonfigurovat podmíněné rozhodnutí v editoru workflowu, klikněte pravým tlačítkem myši na podmíněné rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete formulář **Vlastnosti**.

## <a name="name-a-decision"></a>Pojmenování rozhodnutí

Pomocí následujících kroků zadejte název podmíněného rozhodnutí.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. V poli **Název** zadejte jedinečný podmíněného rozhodnutí.

## <a name="set-conditions"></a> Stanovení podmínek

V tomto okamžiku systém určí, která větev se použije, vyhodnocením odeslaného dokumentu k určení, zda vyhovuje konkrétním podmínkám.

1. V levém podokně klepněte na tlačítko **Základní nastavení**.
2. Klikněte na možnost **Přidat podmínku**.
3. Zadání podmínky
4. Zadejte všechny další podmínky, pokud jsou požadovány.
5. Chcete-li ověřit, zda jsou zadané podmínky nastaveny správně, postupujte následovně:

    1. Klepnutím na tlačítko **Test** otevřete formulář **Podmínka testovacího workflowu**.
    2. Vyberte v oblasti **Ověřit podmínku** formuláře záznam.
    3. Klepněte na možnost **Test**. Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.
    4. Kliknutím na tlačítko **OK** nebo **Zrušit** se vraťte do formuláře **Vlastnosti**.
