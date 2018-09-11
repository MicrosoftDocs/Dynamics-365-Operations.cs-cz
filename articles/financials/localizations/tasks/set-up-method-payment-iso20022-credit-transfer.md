--- 
title: "Nastavení způsobu platby pro převody kreditu ve formátu ISO20022"
description: "Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Nastavení způsobu platby pro převody kreditu ve formátu ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru. 

Před provedením tohoto úkolu musíte exportovat konfigurace formátu a nastavit platební účty.

Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.

Toto je třetí z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.

1. Přejděte do nabídky Závazky > Nastavení platby > Metody platby.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Metody platby pomocí hodnoty „SEPA CT“.
3. Klikněte na možnost Upravit.
4. Vyberte položku Celkem v poli Období.
5. V poli Typ platby vyberte „Elektronická platba“.
6. Rozbalte oddíl Formáty souborů.
7. Vyberte možnost Ano v poli Obecné elektronické výkaznictví.
8. V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.
    * V seznamu vyberte hodnotu ISO20022 – Převedení kreditu (DE). Pokud je seznam prázdný, nejsou žádné importované a aktivní konfigurace formátu exportu platby dodavatele.  
9. V poli Typ účtu vyberte „Banka“.
10. Zadejte hodnoty DEMF OPER do pole Platební účet.
11. Klikněte na položku Uložit.


