---
title: Nastavení způsobu platby pro přímý debet ISO20022
description: Tento postup ukazuje, jak nastavit metodu platby odběratele pro převedení přímého debetu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2ce4e1e960e04c0033990f99eb71897c7ea730f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208400"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Nastavení způsobu platby pro přímý debet ISO20022

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak nastavit metodu platby odběratele pro převedení přímého debetu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru. 



Před provedením tohoto úkolu musíte exportovat konfigurace formátu a nastavit platební účty.



Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.



Toto je třetí z pěti postupů, které společně popisují proces platby odběratele pomocí konfigurací elektronického výkaznictví.

1. Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Metody platby pomocí hodnoty „ELECTRONIC“.
3. Klikněte na možnost Upravit.
4. Zadejte hodnoty DEMF OPER do pole Platební účet.
5. Rozbalte oddíl Formáty souborů.
6. Vyberte možnost Ano v poli Obecné elektronické výkaznictví.
7. V poli Exportovat konfiguraci formátu zadejte nebo vyberte hodnotu.
    * V seznamu vyberte ISO20022 – přímý debet (DE).  Pokud je seznam prázdný, nejsou žádné importované a aktivní konfigurace formátu exportu platby odběratele.  
8. Vyberte možnost Ano v poli Požadovat zmocnění.
    * Pro vlastní formáty platby vyberte parametr Požadovat zmocnění, který vyžaduje zahrnutí informací o zmocnění do zprávy o platbě, jako je přímý debet SEPA.  
9. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]