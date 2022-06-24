---
title: Přeřazení krátkodobé části leasingového závazku
description: Tento článek vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886335"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Přeřazení krátkodobé části leasingového závazku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého. Když je plán, který je vybrán v dávkovém procesu, **Přeřazení závazků z krátkodobého pronájmu**, je vytvořena položka deníku. Tato položka se používá k zaúčtování aktuální části závazku z leasingu k poslednímu dni měsíce. Současně je zaúčtována položka storna od prvního dne následujícího měsíce.

Krátkodobá část závazku z leasingu je uvedena v plánu amortizace závazků. Když je zaúčtována položka deníku, bude k dispozici sloupec **Vytvořen deník reklasifikace odpovědnosti** a v plánu se vyplní také ID deníku.

Chcete-li vytvořit a zaúčtovat záznam deníku reklasifikace krátkodobých závazků, postupujte takto.

1. Jděte na **Leasing majetku \> Periodicky \> Vytvoření dávkového deníku**.
2. V dialogovém okně **Dávkové vytvoření deníku** v poli **Vybrat plán** vyberte **Přeřazení závazků z krátkodobého pronájmu**.
3. V poli **Leasingová skupina** vyberte leasingovou skupinu. Případně v poli **ID knihy** vyberte ID knihy.
4. Zapněte parametr **Zaúčtovat**. Případně, pokud by měl být záznam vytvořen, ale ne zaúčtován, ponechte tento parametr vypnutý.
5. Vyberte **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
