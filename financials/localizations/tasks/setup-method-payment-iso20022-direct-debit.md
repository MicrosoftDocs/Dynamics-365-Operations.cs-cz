--- 
title: "Nastavení způsobu platby pro přímý debet ve formátu ISO20022"
description: "Tento postup ukazuje, jak nastavit metodu platby odběratele pro převedení přímého debetu ISO20022 nebo jakýkoli jiný typ platby pomocí elektronických sestav k vygenerování souboru."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Nastavení způsobu platby pro přímý debet ve formátu ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


