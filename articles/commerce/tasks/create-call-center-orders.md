---
title: " Vytváření objednávek v kontaktním středisku"
description: Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964837"
---
# <a name="create-call-center-orders"></a> Vytváření objednávek v kontaktním středisku

[!include [banner](../includes/banner.md)]

Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele. Tato procedura používá ukázková data USRT společnosti a je určena pro úředníka prodejní objednávky. Předpoklady: Uživatelé provádějící proceduru jsou nastaveni jako uživatelé kontaktního střediska a pololetní katalog společnosti Fabrikam je publikovaném s alespoň jedním zdrojovým kódem.

1. Přejděte na **Retail a Commerce \> Odběratelé \> Služby odběratele**.
2. V poli **SearchText** zadejte kritéria vyhledávání pro vyhledávání odběratele.
    * Pro tuto vzorovou proceduru zadejte text „karen“ a vyberte **Tab**.  
3. Vyberte Vyhledat.
    * Jelikož v ukázkových datech existuje pouze jeden odběratel se jménem Karen, bude výsledek vybrán automaticky.  
4. Vyberte **Nová prodejní objednávka**.
5. Rozbalte nebo sbalte oddíl záhlaví **prodejní objednávky**.
6. Vyberte typ zdrojového kódu pro katalog.
    * Pokud neexistují žádné aktivní zdrojové kódy, můžete tento krok vynechat.  
7. Vyberte **Přidat řádek**.
8. Do **Čísla položky** zadejte hledaný výraz položky.
    * U této vzorové procedury zadejte číslo dílčí položky „8111“ a stiskněte tabulátor. Objeví se místní okno hledání položky.  
9. Vyberte produkt, který chcete přidat do prodejní objednávky.
10. Zadejte prodejní množství.
11. Vyberte **Vytvořit**.
12. Výběrem **Dokončit** zachytíte platbu odběratele.
13. Vyberte **přidat**.
    * Odkaz Přidat se nachází na kartě Platby. Pokud je sbalena karta Platby, rozbalte ji.  
14. Vyberte způsob platby.
    * V této proceduře vyberte hotovostní způsob platby.  
15. Zavřete stránku.
16. Zadejte částku.
    * V této proceduře zadejte částku odpovídající výši zůstatku objednávky, který lze zobrazit na stránce Souhrn prodejní objednávky vlevo od pole Částka. Díky této akci budete moci ukončit objednávku jako plně zaplacenou.  
17. Vyberte **OK**.
18. Vyberte **Odeslat**.

## <a name="additional-resources"></a>Další prostředky

[Přizpůsobení transakčních e-mailů podle způsobu doručení](../customize-email-delivery-mode.md)

[Změna způsobu dodání v POS](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]