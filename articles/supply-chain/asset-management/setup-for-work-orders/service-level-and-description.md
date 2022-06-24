---
title: Úroveň a popis služby
description: V tomto článku jsou vysvětleny úrovně a popis služby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879185"
---
# <a name="service-level-and-description"></a>Úroveň a popis služby

[!include [banner](../../includes/banner.md)]

 

Při vytvoření pracovního příkazu můžete pro něj definovat úrovně služeb a přidat do něj obecný popis. Na stránce **Úrovně služeb pracovního příkazu** můžete vytvářet úrovně služeb a na stránce **Popis pracovního příkazu** můžete vytvářet popis.

## <a name="create-a-service-level"></a>Vytvoření úrovně služeb

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Úroveň služeb**.
2. Zvolte **Nové**.
3. V poli **Úroveň služeb** zadejte úroveň služeb (například číslo).
4. Do pole **Název** zadejte název.

    Na pevné záložce **Pracovní příkazy** můžete definovat očekávaná počáteční a koncová data a časy. Pole na této pevné záložce definují období, v průběhu kterého by měly být pracovní příkazy zahájeny a ukončeny. Používají se pro ručně vytvořené pracovní příkazy a pracovní příkazy vytvořené na základě požadavků na údržbu. 

5. Do pole **Počáteční den** zadejte počet dní určující období, během kterého má být pracovní příkaz zahájen. Počet dnů se vypočítá od data vytvoření pracovního příkazu. Má-li být například pracovní příkaz zahájen při vytvoření, zadejte hodnotu **0**. Má-li být pracovní příkaz zahájen v průběhu jednoho týdne po vytvoření, zadejte hodnotu **7**.
6. Chcete-li nastavit i čas zahájení pro pracovní příkaz kromě počátečního data, nastavte volbu **Nastavit počáteční čas** na hodnotu **Ano**. Poté zadejte počáteční čas do pole **Čas zahájní**. Pokud nastavíte možnost na **Ne**, použije se aktuální čas dne.
7. Do pole **Koncový den** zadejte počet dní určující období, během kterého má být pracovní příkaz ukončen. Počet dnů se vypočítá od počátečního data pracovního příkazu. Má-li například pracovní příkaz končit během jednoho týdne od počátečního data, zadejte **7**.
8. Chcete-li nastavit i čas ukončení pro pracovní příkaz kromě koncového data, nastavte volbu **Nastavit koncový čas** na hodnotu **Ano**. Poté zadejte čas ukončení do pole **Čas ukončení**. Pokud nastavíte možnost na **Ne**, použije se aktuální čas dne.
9. Zvolte možnost **Uložit**.

![Stránka Úroveň služby pracovních příkazů.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Vytvořit popis

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Popisy**.
2. Zvolte **Nové**.
3. Zadejte popis do pole **Popis**.
4. Zvolte **Uložit**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]