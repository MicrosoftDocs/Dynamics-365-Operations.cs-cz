---
title: Refundace odběratelům
description: Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644530"
---
# <a name="reimburse-customers"></a>Refundace odběratelům

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak lze vytvořit transakce refundace pro skupinu odběratelů. Jestliže u odběratele figuruje kreditní zůstatek, můžete refundovat kladné zůstatky množství zůstatku odběratele. 

Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

| Předpoklad                                                            | Popis |
|-------------------------------------------------------------------------|-------------|
| Určete minimální částku refundace pro právnickou osobu.          | Na stránce **Parametry pohledávek** v části **Hlavní** v poli **Minimální refundace** zadejte minimální množství, které může být vráceno u přeplatků odběratele. |
| Volitelné: přidejte účet dodavatele pro každého odběratele, kterému lze refundovat. | Na stránce **Odběratelé** na pevné záložce **Různé podrobnosti** v poli **Účet dodavatele** vyberte účet dodavatele pro odběratele. |

Při vytváření transakcí refundace bude vytvořena faktura dodavatele s částkou kreditního zůstatku. Proces refundace odstraní kreditní zůstatek účtu odběratele a vytvoří zůstatek splatnosti pro účet dodavatele, který odpovídá odběrateli.

1. V Pohledávkách spusťte proces **Úhrada** proces (**Pohledávky \> Pravidelné úkoly \> Úhrada**).
2. Chcete-li seskupit všechny transakce, bez ohledu na dimenze hlavní knihy, nastavte možnost **Souhrn zákazníka** na **Ano**. Chcete-li seskupit pouze transakce, které mají podobné dimenze hlavní knihy, nastavte možnost na **Ne**.
3. Vyberte **Zahrnout zákazníky s nevyřízenými debetními transakcemi**, pokud chcete vybrat zákazníky, kteří mají nevyrovnané částky debetu.
4. K úhradě konkrétních zákaznických účtů na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a poté v dotazu zadejte zákaznické účty.

    Částky úvěru jsou převedeny na účty dodavatelů daných odběratelů a jsou zpracovány jako běžné platby. Pokud některý odběratel nemá účet dodavatele, automaticky se pro odběratele vytvoří jednorázový účet dodavatele.

5. Chcete-li zobrazit transakce úhrad, které byly vytvořeny, použijte sestavu **Úhrada** (**Pohledávky \> Dotazy a sestavy \> Sestava úhrady**).
6. V části Závazky vytvořte platbu pro faktury dodavatele, které byly vytvořeny procesem refundace. Informace o tom, jak platit dodavatelům, najdete na stránce [Přehled plateb dodavatele](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]