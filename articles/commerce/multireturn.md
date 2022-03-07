---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251252"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Vrácení položek napříč vícero objednávkami odběratele a fakturami

[!include [banner](includes/banner.md)]


Tento článek popisuje dvě funkce, které optimalizují vratky zákazníků na více fakturách. 

## <a name="enable-refunds-over-multiple-captures"></a>Povolit refundace přes více záznamů

Tato funkce umožňuje více propojených refundací proti stejné objednávce zákazníka. 

1. Přejděte do pracovního prostoru **Správa funkcí** a vyhledejte možnost **Povolit refundace na vícero záznamech**.
2. Vyberte **Povolit refundace na vícero objednávkách** a poté klikněte na **Povolit**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Povolení správného výpočtu daně pro vrácení s částečným množstvím

Tato funkce zajišťuje, že při vrácení objednávky s použitím více faktur se daně nakonec budou rovnat původně účtované částce daně. 

1. Přejděte do pracovního prostoru **Správa funkcí** a vyhledejte možnost **Povolení správného výpočtu daně pro vrácení s částečným množstvím**.
2. Vyberte **Povolení správného výpočtu daně pro vrácení s částečným množstvím** a poté klikněte na **Povolit**. 


## <a name="process-returns"></a>Zpracování vracení

Poté, co jsou zapnuty tyto funkce a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.

Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky. Pokladník může poté zvolit produkty, které mají být vráceny. Pro všechny zvolené produkty bude vytvořena jediná vratka.

Pokud je objednávka plně vrácena, částka daní vrácená zákazníkovi se bude rovnat částce původně účtované daně.



[!INCLUDE[footer-include](../includes/footer-banner.md)]