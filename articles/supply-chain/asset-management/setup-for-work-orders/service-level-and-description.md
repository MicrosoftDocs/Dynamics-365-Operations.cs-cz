---
title: Úroveň a popis služby
description: V tomto tématu jsou vysvětleny úrovně a popis služby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874640"
---
# <a name="service-level-and-description"></a>Úroveň a popis služby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

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
9. Zvolte **Uložit**.

![Obrázek č. 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Vytvořit popis

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Popisy**.
2. Zvolte **Nové**.
3. Zadejte popis do pole **Popis**.
4. Zvolte **Uložit**.