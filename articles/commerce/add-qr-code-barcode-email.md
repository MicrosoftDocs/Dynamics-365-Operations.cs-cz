---
title: Přidání QR kódu nebo čárového kód do transakčních a přijímacích e-mailů
description: Tento článek vysvětluje, jak vložit QR kódy a čárové kódy, které představují ID objednávky, do transakčních a příjmových e-mailů v Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ffa0009c55b5322b209b19692952c2e0704f65c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872877"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Přidání QR kódu nebo čárového kód do transakčních a přijímacích e-mailů

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak vložit QR kódy a čárové kódy, které představují ID objednávky, do transakčních a příjmových e-mailů v Microsoft Dynamics 365 Commerce.

Do transakčních e-mailů můžete snadno zahrnout QR kódy a čárové kódy, které vám pomohou urychlit proces vyhledávání objednávek v maloobchodním prostředí. K vkládání QR kódů a čárových kódů do e-mailů používáte HTML značku **\<img\>**, která si vyžádá obrázek QR kódu nebo čárového kódu ze služby generování a vykreslování. Společnost Microsoft tuto službu neposkytuje. Existuje však mnoho bezplatných nebo levných služeb, které mohou obsluhovat QR kódy nebo čárové kódy, které se dynamicky generují na základě hodnoty předané v řetězci dotazu.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Přidání QR kódu nebo čárového kód do transakčního e-mailu

Chcete-li vložit QR kód nebo čárový kód do transakčního e-mailu, který je odeslán jako součást nákupu v elektronickém obchodu, postupujte takto.

1. Otevřete zdrojový kód HTML pro šablonu transakčního e-mailu a přidejte značku HTML **\<img\>**, která odkazuje na vaši službu QR kódu nebo čárového kódu. Následuje příklad.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Následuje vysvětlení předchozího příkladu:

    - **VAŠE\_SLUŽBA\_QR\_KÓDU\_ČÁROVÉHO\_KÓDU** představuje doménu vaší služby QR kódu nebo čárových kódů.
    - **data** představuje parametr, který služba QR kódu nebo čárového kódu používá k přijetí obsahu, který by měl být vykreslen jako QR kód nebo čárový kód.

        Hodnota **%salesid%** musí být tomuto parametru přiřazena. V tomto příkladu si všimněte, že hodnota se také používá jako alternativní text pro obrázek.

    - **param1** a **param2** představují další volitelné parametry.

1. Přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> E-mailové šablony organizace** a nahrajte aktualizovaný HTML do příslušné šablony transakčního e-mailu.

> [!NOTE]
> U poskytovatelů služeb QR kódu a čárových kódů se parametry mohou lišit. Nezapomeňte proto kontaktovat svého poskytovatele služeb a potvrdit parametry, kterým musíte hodnoty přiřadit.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Přidání QR kódu nebo čárového kód do příjmového e-mailu 

Chcete-li vložit QR kód nebo čárový kód do e-mailu s potvrzením, který lze odeslat po provedení nákupu v místě prodeje (POS), postupujte takto.

1. Otevřete zdrojový kód HTML pro šablonu e-mailu potvrzení a přidejte značku HTML **\<img\>**, která odkazuje na vaši službu QR kódu nebo čárového kódu. Zde je příklad.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Následuje vysvětlení předchozího příkladu:

    - **VAŠE\_SLUŽBA\_QR\_KÓDU\_ČÁROVÉHO\_KÓDU** představuje doménu vaší služby QR kódu nebo čárových kódů.
    - **data** představuje parametr, který služba QR kódu nebo čárového kódu používá k přijetí obsahu, který by měl být vykreslen jako QR kód nebo čárový kód.

        Hodnota **%receiptid%** musí být tomuto parametru přiřazena. V tomto příkladu si všimněte, že hodnota se také používá jako alternativní text pro obrázek.

    - **param1** a **param2** představují další volitelné parametry.

1. Přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> E-mailové šablony organizace** a nahrajte aktualizovaný HTML do šablony e-mailu, která má ID e-mailu **emailrecpt**.

> [!NOTE]
> U poskytovatelů služeb QR kódu a čárových kódů se parametry mohou lišit. Nezapomeňte proto kontaktovat svého poskytovatele služeb a potvrdit parametry, kterým musíte hodnoty přiřadit.

## <a name="additional-resources"></a>Další prostředky

[Odesílání účtenek e-mailem z Modern POS (MPOS)](email-receipts.md)

[Vytvoření e-mailových šablon pro transakční události](email-templates-transactions.md)
