---
title: "Refundace odběratelům"
description: "Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3201166eb7054205647a54ed80f98968fcfda6e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="reimburse-customers"></a>Refundace odběratelům

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele. 

Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

| Předpoklad                                                            | Popis                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Určete minimální částku refundace pro právnickou osobu.          | Na stránce **Parametry pohledávek** v části **Hlavní** v poli **Minimální refundace** zadejte minimální množství, které může být vráceno u přeplatků odběratele. |
| Volitelné: přidejte účet dodavatele pro každého odběratele, kterému lze refundovat. | Na stránce **Odběratelé** na pevné záložce **Různé podrobnosti** v poli **Účet dodavatele** vyberte účet dodavatele pro odběratele.                                           |

Při vytváření transakcí refundace bude vytvořena faktura dodavatele s částkou kreditního zůstatku. Proces refundace odstraní kreditní zůstatek účtu odběratele a vytvoří zůstatek splatnosti pro účet dodavatele, který odpovídá odběrateli.

1.  V modulu Pohledávky můžete spustit proces **Refundace**.
2.  Proveďte jeden z následujících kroků:
    -   Chcete-li provést refundaci pro konkrétní účty odběratele, klikněte na volbu **Zvolit** a zadejte do dotazu požadované účty odběratele.
    -   Chcete-li provést refundaci pro všechny účty odběratele, klepněte na volbu **OK**.

    Částky úvěru jsou převedeny na účty dodavatelů daných odběratelů a jsou zpracovány jako běžné platby. Pokud některý odběratel nemá účet dodavatele, automaticky se pro odběratele vytvoří jednorázový účet dodavatele.
3.  K zobrazení transakcí refundace, které byly vytvořeny pomocí periodické úlohy, použijte stránku **Refundace**.
4.  V části Závazky vytvořte platbu pro faktury dodavatele, které byly vytvořeny procesem refundace.





