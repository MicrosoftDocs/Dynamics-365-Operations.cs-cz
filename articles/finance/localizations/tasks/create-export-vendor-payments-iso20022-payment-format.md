---
title: Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022
description: Tento postup ukazuje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822698"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Vytváření a export plateb dodavatelů s použitím formátu platby ISO20022

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit platební řádky pro platbu dodavateli v deníku, a generovat soubor pro platbu dodavateli pomocí příkladu převodu kreditu ISO2022.

Toto je pátý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. K dokončení tohoto příkladu použijte ukázková data DEMF.

## <a name="example"></a>Příklad

1.    Přejděte na **Závazky > Platby > Deník plateb**.
2.    Klepněte na možnost **Nový**.
3.    V poli **Název** zadejte nebo vyberte hodnotu.
4.    Klikněte na **Řádky > Návrh platby -> Vytvořit návrh platby**.
5.    Rozbalte oddíl **Záznamy k zahrnutí**.
6.    Klikněte na tlačítko **Filtr**.
7.    V seznamu vyberte řádek pro **tabulku dodavatelů** a pole **Účet dodavatele**.
8.    V poli **Kritéria** zadejte nebo vyberte hodnotu. Můžete použít všechna kritéria pro výběr transakcí dodavatele k zaplacení. Pro tento příklad použijte DE-001 jako účet dodavatele.
12.    Klikněte na tlačítko **OK**.
13.    Klikněte na tlačítko **OK**.
14.    Klikněte na **Vytvořit platby**.
15. Vygenerujte soubor platby ISO20022.
    1.    Klikněte na **Generovat platby**.
    2.    V poli **Metody platby** zadejte nebo vyberte hodnotu.
    3.    Zadejte hodnotu do pole **Název souboru**. Z důvodu platby v EUR bude v tomto příkladu vygenerovaný soubor kompatibilní se SEPA. Převod kreditu ISO20022, jakož i jiné formáty plateb dodavatelů, lze také použít k vytváření plateb v jiných měnách.
    4.    V poli **Bankovní účet** zadejte nebo vyberte hodnotu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]