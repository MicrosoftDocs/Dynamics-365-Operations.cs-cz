---
title: Aktivace nastavení typu směnného kurzu měny globální srážkové daně a typu data
description: Tento článek vysvětluje, jak aktivovat globální nastavení typu směnného kurzu měny srážkové daně a typu data.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229953"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Aktivace nastavení typu směnného kurzu měny globální srážkové daně a typu data

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Tento článek vysvětluje, jak aktivovat globální nastavení typu směnného kurzu měny srážkové daně a typu data. Nyní můžete vybrat vyhrazený typ směnného kurzu a typ data výpočtu směnného kurzu pro měnu srážkové daně. Tyto výběry určují směnný kurz cizí měny, který se použije pro výpočet částky srážkové daně v měně srážkové daně v platebních transakcích.

Tato funkce je k dispozici v Microsoft Dynamics 365 Finance verze 10.0.29 a novější.

1. Přejděte na **Daně** \> **Nastavení** \> **Parametry** \> **Parametry hlavní knihy**.
2. Na kartě **Srážková daň** nastavte možnost **Aktivovat pokročilou měnu srážkové daně** na **Ano**.
3. V poli **Typ směnného kurzu** vyberte typ směnného kurzu pro měnu srážkové daně.
4. Do pole **Typ data výpočtu** vyberte typ data výpočtu, který určuje směnný kurz srážkové daně:

    - **Datum platby** – Určete směnný kurz na základě data účtování deníku plateb.
    - **Datum faktury** – Určete směnný kurz na základě data fakturace deníku faktur. Pokud je datum faktury dokladu prázdné, použije se datum zaúčtování faktury. 
    - **Datum dokumentu** – Určete směnný kurz na základě data dokumentu deníku plateb. Pokud je datum dokumentu prázdné, použije se datum platby.

5. Zvolte možnost **Uložit**.

Pokud se měna transakce liší od měny srážkové daně, která je definována v kódu srážkové daně, bude částka v měně srážkové daně vypočítána z měny transakce na základě předchozího nastavení a bude zaznamenána v zaúčtovaných transakcích srážkové daně.
