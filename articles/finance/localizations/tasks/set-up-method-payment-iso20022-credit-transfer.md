---
title: Nastavení způsobu platby pro převody kreditu ve formátu ISO20022
description: Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d60502cd7f749b71cf39cc38d8a39dcbb7b108
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441003"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Nastavení způsobu platby pro převody kreditu ve formátu ISO20022

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak nastavit metodu platby dodavatele pro převedení kreditu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru. 

Před provedením tohoto úkolu musíte exportovat konfigurace formátu a nastavit platební účty.

Tento úkol byl vytvořen pomocí ukázkových dat společnosti DEMF.

Toto je třetí z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]