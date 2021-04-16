---
title: Přeřazení krátkodobé části leasingového závazku
description: Toto téma vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d98d66b5fe9d32a86eb75d937fedfdca6773ac4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823088"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Přeřazení krátkodobé části leasingového závazku

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit měsíční zápis do deníku k reklasifikaci části závazku z leasingu jako krátkodobého. Když je plán, který je vybrán v dávkovém procesu, **Přeřazení závazků z krátkodobého pronájmu**, je vytvořena položka deníku. Tato položka se používá k zaúčtování aktuální části závazku z leasingu k poslednímu dni měsíce. Současně je zaúčtována položka storna od prvního dne následujícího měsíce.

Krátkodobá část závazku z leasingu je uvedena v plánu amortizace závazků. Když je zaúčtována položka deníku, bude k dispozici sloupec **Vytvořen deník reklasifikace odpovědnosti** a v plánu se vyplní také ID deníku.

Chcete-li vytvořit a zaúčtovat záznam deníku reklasifikace krátkodobých závazků, postupujte takto.

1. Jděte na **Leasing majetku \> Periodicky \> Vytvoření dávkového deníku**.
2. V dialogovém okně **Dávkové vytvoření deníku** v poli **Vybrat plán** vyberte **Přeřazení závazků z krátkodobého pronájmu**.
3. V poli **Leasingová skupina** vyberte leasingovou skupinu. Případně v poli **ID knihy** vyberte ID knihy.
4. Zapněte parametr **Zaúčtovat**. Případně, pokud by měl být záznam vytvořen, ale ne zaúčtován, ponechte tento parametr vypnutý.
5. Vyberte **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
