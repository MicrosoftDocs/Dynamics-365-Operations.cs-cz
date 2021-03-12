---
title: Přehled plateb odběratele
description: Tento průvodce záznamem úloh vás provede různými metodami zadání plateb odběratele.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71e1657d738f691644b6d9cc4d34f812b853934e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978856"
---
# <a name="customer-payment-overview"></a>Přehled plateb odběratele

[!include [banner](../../includes/banner.md)]

Tento průvodce záznamem úloh vás provede různými metodami zadání plateb odběratele. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte na **Podokno navigace Moduly > Pohledávky > Platby > Deník plateb**.
2. Klepněte na možnost **Nový**.
3. Vyberte deník plateb pro uložení plateb odběratele.
4. Vyberte deník nebo jej zadejte ručně.
5. V **podokně akcí** klikněte na možnost **Zadat platby odběratele**. Možnost Zadat platby odběratele se používá k záznamu jedné platby odběratele v rámci jedné operace. Zadáte informace o platbě nahoře a potom označíte faktury, které byly zaplaceny pomocí dané platby, všechny na stejné stránce.  
6. Zadejte odběratele, od kterého jste platbu obdrželi. Pokud neznáte odběratele, ale víte, která transakce byla zaplacena, můžete platbu zadat s použitím pole Transakce. Zadejte nebo vyberte fakturu v poli Transakce. Po výběru transakce se automaticky nastaví výchozí odběratel.
7. Do pole **Platební reference** zadejte platební referenci. Platební referencí může být číslo šeku odběratele nebo reference z elektronické platby odběratele. Platební reference je vyžadována, pouze pokud vyberete zahrnutí platby na vkladové složence.  
8. V poli **Vkladová složenka** vyberte, zda platby mají být zahrnuty na vkladové složence. 
9. V poli **Částka** zadejte částku platby odběratele. Pro částku platby se nenastaví výchozí hodnota. Je nutné ji zadat ručně. 
10. Označte faktury, které byly odběratelem zaplaceny. Pokud platba představuje zálohu, není nutné označit žádné faktury pro vyrovnání. Platbu lze přesto uložit a zaúčtovat. K vyrovnání faktury může dojít později.
11. Zadejte částku platby, která má vyrovnána na označené faktuře. Toto pole lze použít, když je platba určená pro částečnou platbu. Pokud nezadáte částku, bude částka k vyrovnání určena automaticky.
12. Klikněte na položku **Uložit v deníku**. Před uložením platby do deníku se ujistěte, že je definován protiúčet. Když použijete položku **Uložit v deníku**, platbu tím uložíte a přesunete ji do deníku. Poté můžete pokračovat v zadávání další platby.
13. Zavřete stránku.
14. V **podokně akcí** klikněte na možnost Řádky. Při otevírání řádků se zobrazí všechny platby zaznamenané na stránce **Zadat platby odběratele** a uložené do deníku. Na této stránce také můžete zadat nové platby odběratele nebo upravit existující platbu odběratele před zaúčtováním.
15. Klikněte na položku **Nová** a vytvořte tak další platbu. 
16. Vyberte odběratele, od kterého jste platbu obdrželi. Pokud neznáte odběratele, ale víte, která faktura byla prostřednictvím této platby uhrazena, můžete fakturu ručně zadat nebo vybrat v poli Faktura. Po výběru faktury se nastaví výchozí odběratel.  
17. Klikněte na možnost **Vyrovnat transakce** a označte faktury, které byly zaplaceny. Nemusíte vyrovnat platbu pro jakoukoli fakturu. Pokud se jedná o zálohu nebo pokud nevíte, která faktura byla uhrazena, můžete platbu zadat a zaúčtovat. Platbu pak můžete vyrovnat pomocí faktury později.  
18. Označte faktury, které byly platbou uhrazeny. 
19. V poli **Částka** zadejte částku platby, která bude na faktuře vyrovnána.
20. Klikněte na tlačítko **OK**.
21. Do pole **Platební reference** zadejte platební referenci. Platební reference je vyžadována, pouze pokud vyberete zahrnutí platby na vkladové složence.  
22. V **Podokně akcí** klikněte na **Zaúčtovat** pro zaúčtování plateb odběratelů. 

