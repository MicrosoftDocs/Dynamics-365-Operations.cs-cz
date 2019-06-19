---
title: EUR-00002 Zadání adresy nakládky pro intrakomunitární transakci
description: Tato procedura ukazuje, jak zadat adresu nakládky pro interní obchodní transakci.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db22444bee1590770a47ca5946941b530ae85ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564409"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 Zadání adresy nakládky pro intrakomunitární transakci

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura ukazuje, jak zadat adresu nakládky pro interní obchodní transakci. Německá firma si například objedná zboží od dodavatele s firemní adresou v Německu. Tento dodavatel má sklad v Itálii a odtud dodává zboží. Tato dodávka musí být vykázána v Intrastatu. Stejné chování platí pro vrácené položky odběratele.
Postup se vztahuje na všechny evropské země/oblasti. Úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu. Před dokončením této procedury je nutné nakonfigurovat výkaznictví Intrastat. Tento postup je určen pouze pro účetní. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.

1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. Zadání nebo výběr hodnoty
    * Vyberte například DE-001. Tento dodavatel má adresu firmy v Německu.  
4. Klikněte na tlačítko OK.
5. Označte v seznamu vybraný řádek.
6. V poli Číslo zboží zadejte nebo vyberte hodnotu D0001.
7. Klepněte na tlačítko Uložit.
8. V podokně akcí klikněte na možnost Přijmout.
9. Klikněte na Podrobnosti přepravy.
10. Do pole Datum a čas nakládky zadejte datum a čas.
11. Klikněte na Přidat adresu.
12. Klepněte na tlačítko Nový a vytvořte novou adresu s účelem Nakládka.
13. Do pole Název nebo popis zadejte Italština.
14. Vyberte Nakládka jako hodnotu.
    * Všimněte si, že účel adresy musí být Nakládka.  
15. V poli Země/oblast zadejte nebo vyberte hodnotu ITA.
16. Klikněte na položku Uložit.
17. Zavřete stránku.
18. Klikněte na položku Uložit.
    * Ověřte správnost adresy nakládky.  
19. Zavřete stránku.
20. V podokně akcí klikněte na položku Nákup.
21. Klikněte na tlačítko Potvrdit.
22. V podokně akcí klikněte na položku Faktura.
23. Klikněte na položku Faktura.
24. Zadejte hodnotu do pole Číslo.
25. Do pole Datum faktury zadejte datum.
26. Kliknutím na Výchozí od: Množství v příjemce produktu otevřete dialogové okno.
27. V poli Výchozí množství pro řádky vyberte Objednané množství.
28. Klikněte na tlačítko OK.
29. Klikněte na Podrobnosti přepravy.
    * Ověřte, že zboží bylo dodáno z Itálie. V případě potřeby můžete upravit podrobnosti o nakládce.  
30. Zavřete stránku.
31. Klikněte na položku Zaúčtovat.
32. Zavřete stránku.
33. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
34. Klepněte na položku Převod.
35. Vyberte možnost Ano v poli Tisk faktury dodavatele.
36. Klikněte na tlačítko OK.
37. Klikněte na záložku Obecné.
    * Vyhledejte nově vytvořený řádek a ověřte, že odesílatel dodal zboží z Itálie.  

